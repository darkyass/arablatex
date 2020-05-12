## Configuration requise
Sur votre PC:
* Distribution Latex:
  * [TexLive](http://www.tug.org/texlive/){:target="_blank"} (GNU/Linux, Windows, MacOSX)
  * [MikTex](https://miktex.org/download){:target="_blank"} (GNU/Linux, Windows, MacOSX)
  * [MacTex](http://www.tug.org/mactex/){:target="_blank"} (MacOSX).
* Éditeur Latex:
  * [Texstudio](https://www.texstudio.org/#download){:target="_blank"} (GNU/Linux, Windows, MacOSX)
  * [Texmaker](https://www.xm1math.net/texmaker/download_fr.html){:target="_blank"} (GNU/Linux, Windows, MacOSX)
  * [TeXworks](https://www.tug.org/texworks/#Getting_TeXworks){:target="_blank"} (GNU/Linux, Windows, MacOSX)
  * [Kile](https://kile.sourceforge.io/download.php){:target="_blank"} (GNU/Linux, Windows)
  * [GNOME LaTeX](https://wiki.gnome.org/Apps/GNOME-LaTeX#Installation){:target="_blank"} (GNU/Linux)
  * [WinEdt](http://www.winedt.com/download.html){:target="_blank"} (Windows)
  * [WinShell](http://www.winshell.org/download.html){:target="_blank"} (Windows)
  * [TeXnicCenter](https://www.texniccenter.org/download/){:target="_blank"} (Windows)
  * [TeXShop](https://pages.uoregon.edu/koch/texshop/obtaining.html){:target="_blank"} (MacOSX)

Ou tout simplement travailler en ligne avec l'application web [Overleaf](https://www.overleaf.com){:target="_blank"}.

\\[ \frac{1}{n^{2}} \\]

## Exemple pour l'édition en Arabe

### En utilisant le package Babel
[Babel](https://www.ctan.org/pkg/babel){:target="_blank"} est un package de traitement de textes multilingues pour PdfLaTeX.
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

### En utilisant le package Polyglossia
[Polyglossia](https://ctan.org/pkg/polyglossia){:target="_blank"} est un package de traitement de textes multilingues pour XeLaTeX.

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
Voir le résultat de la compilation sur [Overleaf](https://www.overleaf.com/4113516389mcdcrhbtwxgh){:target="_blank"}
## Fichier minimal pour l'édition en Français

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/darkyass/test/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
