---
dg-publish: true
---

```dataview  
TABLE WITHOUT ID 
  link(file.name) AS "Número da sessão"
FROM "Skyfall-rep/Website/3. Sessões de jogo"
WHERE contains(file.folder, this.file.folder) 
  AND file.path != this.file.path
SORT file.mtime DESC
LIMIT 10
```