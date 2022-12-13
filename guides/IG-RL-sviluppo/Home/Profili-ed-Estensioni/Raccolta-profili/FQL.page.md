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
	Canonical_profilo: url
order by
	Tag, status, name
```


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