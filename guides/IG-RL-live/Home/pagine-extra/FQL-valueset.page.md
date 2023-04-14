# ValueSet

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