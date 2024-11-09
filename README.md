# LaTeX templates

Kolekce různých šablon a souborů maker pro LaTeX. Soubory v kořenovém adresáři se pouze linkují přes include.
Ve složce img jsou pak obrázky - logo ČVUT, složka templates obsahuje šablony a finální složka bibliography bibliografii.

Složku s makro soubory lze uvést v globální proměnné TEXINPUTS, nemusí se tak stále kopírovat.
Osobně mám takto linknuté i složky s bibliografií a obrázky.


## Poznámky


```tex
\documentclass[a4paper,12pt]{report}
\input{dimensions_a4}

\def\PackagesIncludeMinted{yes}
\def\DocLanguage{cs}
\input{packages}


\def\title{VAR - Vaření a rochnění}
\def\subtitle{Přednášky}
\def\author{Havránek Kryštof}
\def\institution{ČVUT FEL - EK}
\def\supervisor{Petr polévka}

\input{macros}
\input{doc_notes}

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

\begin{minted}{vhdl}

library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity RS is
port (R, S : in  std_logic;
	Q, nonQ : out std_logic);
end RS;
\end{minted}



\end{document}
```

## Protokol

```tex

\documentclass[a4paper,12pt]{report}
\input{dimensions_a4}

\def\PackagesIncludeMinted{yes}
\def\DocLanguage{cs}
\input{packages}

\def\subject{Laboratorní měření VAR}
\def\title{Měření délek brambor} % n Jméno úlohy
\def\nooftask{1} % Číslo úlohy
\def\author{Havránek Kryštof} % Jméno autora
\def\authorsyear{3} % Ročník autora
\def\authorssgroup{11} % Studijní skupina
\def\authorslgroup{12} % Laboratorní skupina
\def\studyear{2024/2025} % Studijní rok
\def\dateofm{2.11. 2024} % Datum měření
\def\dateofh{8.11. 2024} % Datum odevzdání


\input{macros}
\input{doc_protocol}

\titlep

\section{Teoretický úvod}

Brambory jsou dlouhé i krátké

\end{document}



``

