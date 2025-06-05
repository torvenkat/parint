---
date: 2025-06-05
title: Managing bibliography in Quartz
tags:
  - quartz
  - obsidian
---

Quartz has a built-in Citation plugin that is very useful for managing a uniform format for bibliographic citations across notes/articles. It appeared very straight forward, so I created a `bibliography.bib` and a single database entry in the BibTeX format.  I spent quite some time trying to troubleshoot when the citations did not work as expected.  Then I realized that the `quartz.config.ts` file did not have an entry for the plugin by default.  I added, 

```
Plugin.Citations()
```

and put the `bibliography.bib` file at the root of my content folder.  Everything worked. 


> [!tip] Converting references to BibTeX  format
> These days, almost all  journals and meta index sites have *Cite* tool.  However, not all of them provide option to get the citation in BibTeX format.  Luckily Zotero has a very useful online tool [Zoterobib](https://zbib.org/) that converts URLs to  BibTeX (_and a whole lot of other citation formats._) 
