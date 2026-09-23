# Profili
<!--
@```
from
	StructureDefinition
where kind = 'resource'
select
	Tag: keyword.code,
	Nome_profilo: name, 
	Status: status,
	Risorsa_base: type, 
	Riferimenti: differential.element.type.targetProfile,
	Estensioni: differential.element.type.profile,
	Descrizione: description,
	Canonical: url
order by
	Tag, status, name
```
-->

@```
from
	StructureDefinition
where kind = 'resource'
select
	Tag: keyword.code,
	Nome_profilo: name, 
	Risorsa_base: type,
	Descrizione_profilo: description, 
	Estensioni: differential.element.type.profile,
	Canonical_profilo: url,
	status
order by
	Tag, name
```
