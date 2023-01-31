# ValueSet

<!--
@```
from
	ValueSet
select
	Nome: name,
	URL: url,
	Descrizione: description,
	CodeSystem: compose.include.system
order by name  
```
-->

@```
from
	ValueSet
select
	Nome: name,
	Descrizione: description,
	URL: url
order by
	name 
```
