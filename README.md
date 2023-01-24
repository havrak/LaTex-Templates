# LaTeX templates

Kolekce různých šablon a souborů maker pro LaTeX. Soubory v kořenovém adresáři se pouze linkují přes include.
Ve složce img jsou pak obrázky - logo ČVUT, složka templates obsahuje šablony a finální složka bibliography bibliografii.

Složku s makro soubory lze uvést v globální proměnné TEXINPUTS, nemusí se tak stále kopírovat.
Osobně mám takto linknuté i složky s bibliografií a obrázky.


#### Vzorový dokumentu
Zde je použit makro soubor zaměřený na psaní poznámek


```tex
\documentclass[a4paper,12pt]{report}
\include{basic}


\def\title{}
\def\subtitle{}
\def\author{}
\def\institution{}

\include{makra}
\include{notes}

\begin{document}
\titlep
\tocp

\chapter{Chapter}

Test test test

\section{Section}

$\int (-x^2-4x-7)e^{\frac{x}{2}} \text{ d}x \eqpp \begin{vmatrix}
	u = x^2-4x-7 & u'=-2x-4\\
	v' = e^{\frac{x}{2}} & v = 2e^{\frac{x}{2}}
\end{vmatrix}$


\end{document}


```
