# Tuto Latex <br> éditer en Arabe



# Configuration requise


## Distribution Latex requise

* <a href="http://www.tug.org/texlive/" target="_blank">TexLive</a> (GNU/Linux, Windows, MacOSX)
* <a href="https://miktex.org/download/" target="_blank">MikTex</a> (GNU/Linux, Windows, MacOSX)
* <a href="http://www.tug.org/mactex/" target="_blank">MacTex</a> (MacOSX)


## Éditeur Latex requis

* <a href="https://www.texstudio.org/#download" target="_blank">Texstudio</a> (GNU/Linux, Windows, MacOSX)
* <a href="https://www.xm1math.net/texmaker/download_fr.html" target="_blank">Texmaker</a> (GNU/Linux, Windows, MacOSX)
* <a href="https://www.tug.org/texworks/#Getting_TeXworks" target="_blank">TeXworks</a> (GNU/Linux, Windows, MacOSX)
* <a href="http://www.winshell.org/#download" target="_blank">WinShell</a> (GNU/Linux, Windows, MacOSX)
* <a href="https://kile.sourceforge.io/download.php" target="_blank">Kile</a> (GNU/Linux, Windows)
* <a href="https://wiki.gnome.org/Apps/GNOME-LaTeX#Installation" target="_blank">GNOME LaTeX</a> (GNU/Linux)
* <a href="http://www.winedt.com/download.html" target="_blank">WinEdt</a> (Windows)
* <a href="https://www.texniccenter.org/download/" target="_blank">TeXnicCenter</a> (Windows)
* <a href="https://pages.uoregon.edu/koch/texshop/obtaining.html" target="_blank">TeXShop</a> (MacOSX)


## Éditeur Latex en ligne

* <a href="https://www.overleaf.com" target="_blank">Overleaf</a> (Internet Explorer, Firefox, Chrome, ...)


## Package Latex requis

* <a href="https://ctan.org/pkg/polyglossia" target="_blank">Polyglossia</a>: un package de traitement de textes multilingues pour XeLaTeX.
* <a href="https://www.ctan.org/pkg/babel" target="_blank">Babel</a>: un package de traitement de textes multilingues pour PdfLaTeX.



# Exemple minimal


## En utilisant <br> le package Polyglossia

```latex
% !TEX TS-program = XeLaTeX

\documentclass{article}

\usepackage{geometry}                                          % Package pour la mise en page
\geometry{hmargin=1.5cm,vmargin=1.5cm}                         % Modification des marges

\usepackage{amsmath,amsfonts,amssymb,fourier}                  % Packages pour les formules Maths

\usepackage{fontspec}
\setmainfont{Times New Roman}
\setsansfont{Arial}
\newfontfamily\arabicfont[Scale=1.15,Script=Arabic]{Amiri}
\newfontfamily\arabicfontsf[Scale=1.15,Script=Arabic]{Amiri}
\usepackage{polyglossia}
\setdefaultlanguage[locale=morocco]{arabic}

\addto\captionsarabic{                                         % Changement du titre du sommaire
  \renewcommand{\contentsname}{محتوى الدرس}
}
\usepackage{tocloft}                                           % Package pour la modification du sommaire
\renewcommand{\cftsecleader}{\cftdotfill{\cftdotsep}}          % Ajout des pointillés au sommaire

\begin{document}
\tableofcontents{}

\clearpage

\section{المحور الأول}
\subsection{الجزء الأول}
نص باللغة العربية
\beginL
Texte en français
\endL

\subsection{الجزء الثاني}
عبارة رياضية
$\lim\limits_{x\to+\infty}f(x)=1$

\section{المحور الثاني}
\subsection{الجزء الأول}
\subsection{الجزء الثاني}
\end{document}
```


## En utilisant <br> le package babel

```latex
% !TEX TS-program = PdfLaTeX

\documentclass{article}
\usepackage{arabtex}
\usepackage[utf8]{inputenc}
\usepackage[LFE,LAE]{fontenc}
\usepackage[french,arabic]{babel}

\begin{document}
\selectlanguage{arabic}
\tableofcontents{}

\clearpage

\section{المحور الأول}
\subsection{الجزء الأول}
نص باللغة العربية
\textLR{
  Texte en français
}

\subsection{الجزء الثاني}
عبارة رياضية
$\lim\limits_{x\to+\infty}f(x)=1$

\section{المحور الثاني}
\subsection{الجزء الأول}
\subsection{الجزء الثاني}
\end{document}
```



### External 3.1



Content 3.1


## External 3.2

Content 3.2


## External 3.3

![External Image](https://s3.amazonaws.com/static.slid.es/logo/v2/slides-symbol-512x512.png)
