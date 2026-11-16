---
{"dg-publish":true,"permalink":"/2-mundo/np-cs/visao-geral-dos-np-cs/","dg-note-properties":{}}
---


```dataview  
TABLE WITHOUT ID 
  nome AS "Personagem",
  profissão AS "Profissão",
  last-seen AS "Última vez visto em"
FROM "2. Mundo/NPCs
WHERE contains(file.folder, this.file.folder) 
  AND file.path != this.file.path
SORT file.mtime DESC
LIMIT 10
```