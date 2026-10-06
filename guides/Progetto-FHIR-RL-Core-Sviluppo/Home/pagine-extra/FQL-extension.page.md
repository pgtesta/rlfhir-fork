# Estensioni 
<!--
@```
    from
	StructureDefinition
where type = 'Extension'
select
	Tag: keyword.where(system = 'https://fhir.siss.regione.lombardia.it/CodeSystem/Tag').code,
	Usato_In: keyword.where(system = 'https://fhir.siss.regione.lombardia.it/CodeSystem/Profili').code,
	Nome: name, 
	Status: status, 
	Base: context.expression,
	Tipo_variabile: differential.element.type.code,
	Descrizione: description,
	Canonical: url
order by
	Tag, name
```
-->

@```
from
	StructureDefinition
where type = 'Extension'
select
	Nome_extension: name, 
	Base: context.expression,
	Descrizione_extension: description,
	Canonical_extension: url
order by
	name
```