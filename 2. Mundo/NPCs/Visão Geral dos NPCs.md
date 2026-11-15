---
dg-publish: false
---

```dataview  
TABLE WITHOUT ID 
  nome AS "Personagem",
  profissão AS "Profissão",
  last-seen AS "Última vez visto em"
FROM "Skyfall-rep/Website/2. Mundo/NPCs"
WHERE contains(file.folder, this.file.folder) 
  AND file.path != this.file.path
SORT file.mtime DESC
LIMIT 10
```