---
dg-publish: true
---

Ao longe de suas aventuras, o intrépido grupo de aventureiros já explorou os seguintes lugares: 
```dataview  
TABLE WITHOUT ID 
  link(file.name) AS "Nome do local", 
  região AS "Região"
FROM "Skyfall-rep/Website/2. Mundo/Locais"
WHERE contains(file.folder, this.file.folder) 
  AND file.path != this.file.path
SORT file.mtime DESC
LIMIT 10
```
