---
name: word-highlighted-changes
description: "Apply changes marked in a DOCX document to the FHIR guide pages in this repository. Use when a Word file contains yellow-highlighted text, especially yellow strikethrough text that must be deleted, and the requested changes target guide pages rather than profiles or extensions."
argument-hint: "Path to the DOCX document and, if known, the guide or page set to update"
user-invocable: true
---

# Word Highlighted Changes

Process a DOCX change document and apply only its clearly identified instructions to the guide pages under `guides/`. Use `guides/IG-RL-sviluppo/` by default when the document does not specify another guide set. Never apply this skill to FHIR profiles, extensions, examples, or terminology JSON files.

## Required Inputs

Ask for missing information before editing:

- The DOCX path or attachment. If none is provided, inspect `.github/DaProcessare/` and report the available `.docx` files. Ask which one to use if there is more than one plausible document.
- The guide set or version to update when the DOCX explicitly targets one. Otherwise use `guides/IG-RL-sviluppo/` and report that default.
- Confirm that highlighted non-strikethrough text represents an insertion. Never remove or replace surrounding unhighlighted content because of a non-strikethrough highlight.
- Whether yellow strikethrough text always means deletion, including when the text is inside a table, heading, list, header, footer, or other document region.
- Whether comments, tracked changes, unhighlighted text, images, and formatting-only changes should be considered.
- Whether the user wants preview-only or application. Default to preview-only.

## Procedure

1. Inspect the DOCX without modifying it.
   - Use a structured DOCX reader such as `python-docx`; inspect the underlying Word XML when needed for text boxes, comments, tracked changes, or highlighting not exposed by the high-level reader.
   - Enumerate paragraphs, tables, headings, lists, headers, footers, comments, and tracked changes that contain highlighted runs.
   - Detect yellow highlighting from the run's highlight property and report the detection method. Do not treat font color, shading, or a yellow page background as equivalent unless the user confirms that convention.
   - Preserve run order and combine adjacent highlighted runs only when they form one contiguous logical change.
   - Record whether every highlighted run is strikethrough. A highlighted and strikethrough run is a deletion request; a highlighted non-strikethrough run is an insertion request requiring context.

2. Build a change inventory without writing guide files.
   - For each change, record DOCX location, exact highlighted text, strikethrough state, surrounding sentence/heading, proposed operation, target guide path, target heading or anchor, and ambiguity.
   - Resolve target pages only within `guides/**/*.page.md` or other explicitly documented guide-page formats. Search by page title, profile/resource name, heading, canonical guide link, and distinctive surrounding text. Use `guides/IG-RL-sviluppo/` unless the DOCX specifies another guide set.
   - Prefer an explicit page name or guide link in the DOCX. Do not infer a page solely from a profile name when multiple guide pages match.
   - For yellow strikethrough text, locate the exact target text before proposing deletion. If it appears more than once, report all matches and ask which occurrence to remove.
   - For yellow non-strikethrough text, treat it as insertion text. Insert it at the explicitly indicated location or immediately adjacent to the matching context, preserving the existing unhighlighted content. If the insertion location cannot be determined from the document, mark it blocked rather than guessing.
   - Keep changes to different guide versions separate. Never apply a change to every matching page by default.

3. Show a preview and request approval.
   - Present a compact table with DOCX source location, operation (`delete` or `insert`), target page, target anchor, existing context, and inserted/deleted text.
   - Show the exact Markdown context or diff for every proposed change.
   - List unresolved page mappings, repeated matches, unsupported DOCX constructs, and interpretation questions separately.
   - Stop after the preview when the user asks for preview-only, dry-run, review, or approval before applying. Do not write, create, rename, or delete guide files in preview-only mode.

4. Apply approved changes to guide pages.
   - Edit only approved target pages and preserve unrelated Markdown, links, front matter, tables, indentation, and line endings as far as practical.
   - For yellow strikethrough text, remove only the exact approved text and clean up resulting whitespace or empty list/table artifacts without rewriting surrounding prose.
   - For approved insertions, preserve the intended Markdown structure and place the text at the approved anchor without deleting or replacing surrounding unhighlighted content.
   - Do not modify the source DOCX, profiles, extensions, examples, terminology, or generated artifacts.
   - If the target page changed after preview, stop and regenerate the preview instead of overwriting the newer content.

5. Validate the result.
   - Confirm every approved deletion is absent and every approved insertion is present exactly once at the intended page and anchor.
   - Check that modified Markdown pages remain readable and that front matter, links, tables, and fenced code blocks are not malformed.
   - Run any repository documentation build or link checker that is documented or configured. If none is available, perform targeted structural checks and report that a full documentation build was unavailable.
   - Report applied, unchanged, skipped, and blocked changes, including unsupported Word constructs.

## Decision Rules

- Yellow highlighting identifies candidate changes; it is not permission to guess the target page or operation.
- Yellow plus strikethrough means delete the highlighted text from the approved guide location.
- Yellow without strikethrough means insertion text. It must never replace or delete surrounding unhighlighted text.
- Unhighlighted Word text is context only unless the user explicitly says otherwise.
- Tracked deletions and comments are not applied automatically; include them in the inventory and ask for confirmation.
- Never update profiles or extensions because a guide page mentions them.
- Ambiguous mappings, duplicate target text, and conflicting instructions remain blocked until resolved.

## Completion Report

End with:

- DOCX inspected and highlighted runs detected.
- Guide set and pages inspected.
- Applied, unchanged, skipped, and blocked changes.
- Exact modified guide pages.
- Validation commands and results.
- Assumptions and unsupported DOCX features requiring follow-up.