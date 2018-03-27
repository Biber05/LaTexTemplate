# Grundlagen
\documentclass[type]{name}
Dokumenttyp inkl. Sprachen festlegen

\begin{document} 
Typ festlegen -> Dokument

\include{file}
Tex Datei einbinden

\usepackage{german}
Deutsche Umlaute

\usepackage{utf8}
UTF-8 mit allen Umlauten

\usepackage{array} 
Package für Tabellenausrichtung

\euro{}
€

\usepackage{bibgerm}
Bibtex - Package für Zitate

\usepackage{hyperref} 
Package für Querverweise

\usepackage{makeidx}
Package für Stichworte

\usepackage{amsmath, amsthm, amssymb}
Packages für Formeln 

\usepackage{color} 
Package für Farben

\usepackage{colortbl}
Package für Tabellenfarben

\usepackage[normalem]{ulem}
Package für Schriftstil

\usepackage{graphicx}
Package für externe Bilder

\usepackage{etex}
Package für Größenangaben


## Beispiel
\documentclass[a4paper, 10pt]{scrbook}
    
# Gliederung
\section{...}
Absatz 1

\subsection{...}
Absatz 2

\subsubsection{...}
Absatz 3

\paragraph{...}
Paragraph 1

\subparagraph{...}
Paragraph 2

\appendix
Seitennummerierung mit Buchstaben

\part{} \chapter{...}
Kapitel für book oder report

\\
Umbruch

\\[0,5cm]
Absatz

\par
Paragraph

\newpage
Neue Seite

\, \: \; \!
Leerzeichen mit unterschiedlichen Abständen

## Beispiel
### 1 
chapter
	section
		subsection


# Einfache Strukturelemente
\begin{itemsize}
Start Aufzählung (UL)

\item
Unterpunkt

\end{itemsize}
Ende Aufzählung

\begin{enumerated}
Start Aufzählung (OL)

\end{enumerated}
Ende Aufzählung

\xdef\letzterwert{\the\value{enumi}} 
Speichern des letzten Index

\setcounter{enumi}{\letzterwert}
Setzen des gespeicherten Indexes

\begin{description}
Start Aufzählung (Beschriftung)

\end{description}
Ende Aufzählung (Beschriftung)

\item[erster Punkt]
Unterpunkt mit eigener Beschriftung

## Beispiel
### 1
\begin{itemize}
  \item erstes
  \item zweites
    \begin{itemize}
     \item zweites erstes
         \begin{itemize}
            \item und so weiter
         \end{itemize}
     \item zweites zweites
    \end{itemize}
\end{itemize}

### 2
\begin{enumerate}
     \item Eins.
     \item Zwei.
     \xdef\letzterwert{\the\value{enumi}}
\end{enumerate}

Unterbrechung.
     
\begin{enumerate}
     \setcounter{enumi}{\letzterwert}
     \item Drei
     \item Vier
\end{enumerate}

# Tabellen
\begin{tabular}{SPALTENDEFINITION}
Start Tabelle

\end{tabular}
Ende Tabelle

r l c
Ausrichtung Spalte (rechts, links, mittig)

p{6cm}
Spalte mit fixer Breite (inkl. Umbruch)

| &
Spaltentrennung Bsp: {l|l|l}

\hline \hline\hline
Horizontale Linie - Doppelte horizontale Linie

m{Breite}
Felder sind vertikal zentriert 

b{Breite}
Ausrichtung an Fußzeile

>{Dekl} 
Vor jedes Element r,l,c,m,b,p

<{Dekl} 
Hinter jedes Element r,l,c,m,b,p

\multicolumn{3}{c}{Text}
Verbindet und zentriert Text über 3 Spalten

\rowno
Zeilenummer

## Beispiel
### 1
*{7}{c}  
    -> 7 zentrierte Spalten
\newcolumntype{C}{>{\centering\arraybackslash}p{5cm}} 
    -> Horizontal und Vertikal ausgerichtet

# Querverweise
\label{marker}, \ref{marker}, \pageref{marker}
Referenz zu Stelle im Text

\cite[text]{key_list}
Zitat Keylist = Quellenverzeichnis

\nocite{key_list}
Zitat taucht NUR im Quellenverzeichnis auf

\bibliographystyle{gerplain}
Zitationsstil -> Vor begin{document} 

\bibliography{literatur.bib}
Literaturangaben werden generiert

\hypersetup{pdfborder={0 0 0}}
PDF verlinken

\makeindex
Start des Indizes für Stichworte

\printindex
Index benutzen

# Fußnoten
\footnote{text}
Text der Fußnote

# Mathematik
$1+1=1$ 
Formel in Text

\[ 1+1=1 \] 
Formel in Absatz

## Beispiele und Hilfsreiche Links
https://de.wikipedia.org/wiki/Hilfe:TeX
https://en.wikibooks.org/wiki/LaTeX/Mathematics

# Aussehen
\setlength{\parindent}{0cm}
Horizontaler Einschub vor jedem Absatz

\setlength{\parskip}{0.2cm}
Vertikaler Abstand zwischen den Absätzen

\textcolor{...}
Schriftfarbe

\textit
Kursiv

\textbf
Fett

\textmd
Text medium

\textnormal 
Hauptschriftart

\uline{important} 
Unterstrichen

\uuline{urgend} 
Doppelt Unterstrichen

\tiny \small \normalsize \large \huge
Schriftgröße

\glqq{}text\grqq{}
Anführungszeichen unten und oben

\slshape
Serifenlose Schrift (Kopf und Fußzeile)

## Beispiel
Dieser \textrm{Text}
ist ganz \textit{schön}
komisch ... \textbf{Und}
alle Vögel { \rmfamily
\itshape \bfseries
fliegen tief $:-)$ }

Dieser Text
ist ganz *schön*
komisch ... **Und**
alle Vögel ***fliegen tief*** : −) 

# Grafiken und Figures
\includegraphics[width=5cm]{my_image}
Bild einbinden

\includegraphics[trim=0 0 2cm 0,clip,width=\textwidth]% {Kapitel08-img1}
Trimmen

## Beispiel
\begin{figure}[h] -> h=fixieren
\begin{center}
\includegraphics[width=4cm]{ram.jpg}
\caption{Random Access Memory}
\label{ram_cover}
\end{center}
\end{figure}

# Silbentrennung
Zie\-gen\-kä\-se 
\- manuelle Silbentrennung

# Sonstiges
\linespread{ZAHL}
Zeilenabstand

\thepage
Seitenzahl

\pagenumbering{arabic}
Seitennummerierung

\today
Heutiges Datum

\number\day.\number\month.\number\year
Tag.Monat.Jahr

