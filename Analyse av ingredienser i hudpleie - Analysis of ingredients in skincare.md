# Ingrediensanalyse

```dataview
TABLE WITHOUT ID

link(file.link, default(title, file.name)) AS "Ingrediens",
join(keywords, ", ") AS "Nøkkelord",
rating AS "Vurdering"

FROM #hudpleie OR #skincare 

WHERE icontains(this.ingredients, file.aliases[0])

SORT length(rating) DESC, file.name ASC
```
