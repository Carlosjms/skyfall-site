---
dg-publish: true
---

O **Boletim da Queda** é a gazeta mais relevante de **Alberich**, a cidade das **Mil Portas**. Publicado semanalmente, seus volumes alcançam até mesmo os buracos mais escuros do [[Continente de Opath]].

```dataviewjs
const folder = "Skyfall-rep/Website/2. Mundo/Boletim da Queda_jog";

const pngs = app.vault.getFiles()
  .filter(f => f.extension === "png" && f.parent.path === folder)
  .sort((a, b) => b.stat.mtime - a.stat.mtime)
  .slice(0, 10);

dv.table(
  ["Boletim da Queda"],
  pngs.map(f => [dv.fileLink(f.path)])
);
```