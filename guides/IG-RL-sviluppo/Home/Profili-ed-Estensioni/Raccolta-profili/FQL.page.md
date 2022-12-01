# Profili
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

# Estensioni 
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
	Link_simplifier: url
order by
	Tag, status, name
```