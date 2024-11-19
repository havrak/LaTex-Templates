# LaTeX templates

Collection of basic tex files that I commonly include in my document. `macros.tex` and `packages.tex` define useful macros and package configuration. Rest are used to normalize style acros my documents - `doc_notes.tex` for school notes, `doc_paper` for thesis and so on.

WARNING: Enabling Tikz in packages turns on Memoize to externalize figure. However if one is using biblatex at the same time this can lead to issues with verbatim type. It is necessary to update `collargs` and `memoize` to latest version in oder to prevent this behavior.


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

