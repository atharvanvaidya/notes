# This file contains all the tweaks I found while writing and editing papers in latex

## I use texmaker for writing papers in latex and generating its pdf 

* Writing paper in twocolumn format `svjour3`

Always use `\sloppy` after the `\begin{document}` to avoid words getting out of any of the columns

* Site to write latex equations [HostMath](https://www.hostmath.com/)

* To assign caption to text

Enclose the text in verbatim and then figure to give caption

* Give annotation remark to the authors (Numbers 1 , 2 ... as superscript)

Write the following before `\begin{document}`
```
\newcommand*{\affmark}[1][*]{\textsuperscript{#1}}
```
and write this where you want to give the superscript number
```
\affmark[1]
```
Change the number as required

* Spread the table/figure across the two columns

Use `\begin{figure*}`/`\begin{table*}` instead of `\begin{figure}`/`\begin{table}`

* Spread the columns equally 

Use tabularx package 
```
\usepackage{tabularx}
```
Write this inside the table block. The syntax for the table is as follows:
```
\begin{tabularx}{\textwidth}{XlXlX}
% Columns : 2 
% X represents the space which will be distributed equally
% textwidth is the total width of the page. To make the table fit in single column (for twocolumn), use 0.5\textwidth
\end{tabularx}
```

* Table generator online
This is the best online latex table generator, which generates multirow and multicolumn tables.
[Link](https://www.latex-tables.com/)

* Writing Equations 
Use the nccmath package
```
\usepackage{nccmath}
```
For aligning the equation in the center, use the following syntax
```
\begin{ceqn}
\begin{align}
% Write equation here
\end{align}
\end{ceqn}
```
The numbering will be generated automatically

* Images conversion
Use online-convert to convert images to eps and eps to pdf
[Link](https://image.online-convert.com/)

* Latex Equation Editor
This is a good online latex equation editor. [Link](https://www.tutorialspoint.com/latex_equation_editor.htm)

* Switching from twocolumn to onecolumn and vice versa
Use the following commands to toggle between twocolumn and onecolumn mode : `\twocolumn` and `\onecolumn`

* [Wonderful tips for writing bibliography and citations](https://www.ece.ucdavis.edu/~jowens/biberrors.html)

* Word wrap in multirow
```
\multirow{NoOfColumns}{2cm} instead of \multirow{NoOfColumns}{*}
```
* Horizontal line for selected columns
\cline{3-5} for line from col 3 to 5(both inclusive)

* Changing text color
```
\usepackage[dvipsnames]{xcolor}
\textcolor{red}{the purpose of learning \LaTeX\ is great.}
```
* Decrease the gap between rows in table
Add 
``` \setlength\extrarowheight{-7pt} ``` 
to decrease. Make the pt to positive to increase the default gap. This should be added before the *tabular*
Requires to include 
```
\usepackage{array}
```

## Tips while writing paper.
* Always specify the Full Form of any acronym for it's first occurence.
* Club the Literature Survey into paragraphs which contain similar research. Reduce the no. of paragraphs.
* Always store the bibliography in a .bib database. It can be found from the google scholar site. Just search the paper there.

