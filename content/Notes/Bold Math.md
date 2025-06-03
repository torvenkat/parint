---
date: 2025-06-03
title: Bold Math in LaTeX
tags:
  - latex
---

Computer Modern Fonts in LaTeX are nice, because they are thin.  However, there is a certain elegance to old school math books with thicker fonts (see image).

![[old_school_math_typesetting.png]]

There is a way to get closer, at least with [LuaTeX](https://www.luatex.org/) and  [XeLaTex ](https://www.overleaf.com/learn/latex/XeLaTeX)  using

```
\setmainfont{texgyretermes-regular.otf}[FakeBold=1]
\setmathfont{STIXTwoMath-Regular.otf}[FakeBold=1]
```

This will give fonts that are thicker, but not as bold as \bold. 

Ref: [Stockexchange](https://tex.stackexchange.com/questions/668872/old-mathbooks-thick-font)


