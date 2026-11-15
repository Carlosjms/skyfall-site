---
dg-publish: true
---

```dataview  
TABLE WITHOUT ID 
  link(file.name) AS "Personagem",
  player AS "Jogador(a)",
  classe AS "Classe",
  antecedente AS "Antecedente",
  trilha AS "Trilha"
FROM "Skyfall-rep/Website/1. Grupo/Personagens"
WHERE contains(file.folder, this.file.folder) 
  AND file.path != this.file.path
SORT file.name ASC
LIMIT 10
```
