# Grundlagen
Dokumenttyp inkl. Sprachen festlegen

    \documentclass[type]{name}

Typ festlegen -> Dokument

    \begin{document} 

Tex Datei einbinden

    \include{file}

Deutsche Umlaute
    
    \usepackage{german}

UTF-8 mit allen Umlauten
 
    \usepackage{utf8}

Package für Tabellenausrichtung
 
    \usepackage{array} 

€

    \euro{}

Bibtex - Package für Zitate

    \usepackage{bibgerm}

Package für Querverweise

    \usepackage{hyperref} 

Package für Stichworte

    \usepackage{makeidx}

Packages für Formeln 

    \usepackage{amsmath, amsthm, amssymb}

Package für Farben

    \usepackage{color} 

Package für Tabellenfarben

    \usepackage{colortbl}

Package für Schriftstil

    \usepackage[normalem]{ulem}

Package für externe Bilder

    \usepackage{graphicx}

Package für Größenangaben

    \usepackage{etex}


## Beispiel
srcreport = Einseitig -> Bachelor-Arbeiten

srcbook = Doppelseitig -> Master-Arbeiten

    \documentclass[a4paper, 10pt]{scrbook}
    
# Gliederung
Absatz 1

    \section{...}

Absatz 2
    
    \subsection{...}

Absatz 3

    \subsubsection{...}

Paragraph 1

    \paragraph{...}

Paragraph 2

    \subparagraph{...}


Seitennummerierung mit Buchstaben
    
    \appendix


Kapitel für book oder report

    \part{} \chapter{...}

Umbruch
    
    \\

Absatz
    
    \\[0,5cm]

Paragraph
    
    \par

Neue Seite

    \newpage

Leerzeichen mit unterschiedlichen Abständen

    \, \: \; \!


## Beispiel
### 1 - Struktur
    chapter
	
        section
		
            subsection

# Einfache Strukturelemente
Start Aufzählung (UL)
    
    \begin{itemsize}

Unterpunkt
    
    \item


Ende Aufzählung
    
    \end{itemsize}


Start Aufzählung (OL)

    \begin{enumerated}

Ende Aufzählung
    
    \end{enumerated}

Speichern des letzten Index

    \xdef\letzterwert{\the\value{enumi}} 

Setzen des gespeicherten Indexes

    \setcounter{enumi}{\letzterwert}

Start Aufzählung (Beschriftung)

    \begin{description}
    
Ende Aufzählung (Beschriftung)

    \end{description}

Unterpunkt mit eigener Beschriftung
    
    \item[erster Punkt]


## Beispiel
### 1 -  Einfache Aufzählung
    \begin{itemize}
        \item erstes
        \item zweites
        \begin{itemize
            \item zweites erstes
            \begin{itemize}
                \item und so weiter
            \end{itemize}
            \item zweites zweites
        \end{itemize}
    \end{itemize}

### 2 - Aufzählung später fortsetzen
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

Start Tabelle

    \begin{tabular}{SPALTENDEFINITION}


Ende Tabelle

    \end{tabular}


Ausrichtung Spalte (rechts, links, mittig)

    r l c


Spalte mit fixer Breite (inkl. Umbruch)

    p{6cm}

Spaltentrennung Bsp: {l|l|l}

    | &

Horizontale Linie - Doppelte horizontale Linie

    \hline \hline\hline

Felder sind vertikal zentriert 

    m{Breite}

Ausrichtung an Fußzeile

    b{Breite}

Vor jedes Element r,l,c,m,b,p

    >{Dekl} 

Hinter jedes Element r,l,c,m,b,p

    <{Dekl} 

Verbindet und zentriert Text über 3 Spalten
    
    \multicolumn{3}{c}{Text}

Zeilenummer

    \rowno

## Beispiel
### 1 - Tabellen
7 zentrierte Spalten
    
    *{7}{c}  

### 2 - Horizontal und Vertikal ausgerichtet 

    \newcolumntype{C}{>{\centering\arraybackslash}p{5cm}} 

# Querverweise

Referenz zu Stelle im Text

    \label{marker}, \ref{marker}, \pageref{marker}

Zitat Keylist = Quellenverzeichnis

    \cite[text]{key_list}

Zitat taucht NUR im Quellenverzeichnis auf

    \nocite{key_list}

Zitationsstil -> Vor begin{document} 

    \bibliographystyle{gerplain}

Literaturangaben werden generiert

    \bibliography{literatur.bib}

PDF verlinken

    \hypersetup{pdfborder={0 0 0}}

Start des Indizes für Stichworte

    \makeindex

Index benutzen

    \printindex

# Fußnoten

Text der Fußnote

    \footnote{text}

# Mathematik

Formel in Text

    $1+1=1$ 

Formel in Absatz

    \[ 1+1=1 \] 

## Beispiele und Hilfsreiche Links
https://de.wikipedia.org/wiki/Hilfe:TeX

https://en.wikibooks.org/wiki/LaTeX/Mathematics

# Aussehen

Horizontaler Einschub vor jedem Absatz

    \setlength{\parindent}{0cm}

Vertikaler Abstand zwischen den Absätzen

    \setlength{\parskip}{0.2cm}


Schriftfarbe

    \textcolor{...}

Kursiv

    \textit

Fett

    \textbf

Text medium

    \textmd

Hauptschriftart

    \textnormal 

Unterstrichen

    \uline{important} 

Doppelt Unterstrichen

    \uuline{urgend} 

Schriftgröße

    \tiny \small \normalsize \large \huge

Anführungszeichen unten und oben

    \glqq{}text\grqq{}

Serifenlose Schrift (Kopf und Fußzeile)

    \slshape

## Beispiel
Dieser Text
ist ganz *schön*
komisch ... **Und**
alle Vögel ***fliegen tief*** : −) 

    Dieser \textrm{Text}
    ist ganz \textit{schön}
    komisch ... \textbf{Und}
    alle Vögel { \rmfamily
    \itshape \bfseries
    fliegen tief $:-)$ }

# Grafiken und Figures
Bild einbinden

    \includegraphics[width=5cm]{my_image}

Trimmen

    \includegraphics[trim=0 0 2cm 0,clip,width=\textwidth]% {Kapitel08-img1}

## Beispiel
    \begin{figure}[h] -> h=fixieren
        \begin{center}
            \includegraphics[width=4cm]{ram.jpg}
            \caption{Random Access Memory}
            \label{ram_cover}
        \end{center}
    \end{figure}

# Silbentrennung
\- manuelle Silbentrennung

    Zie\-gen\-kä\-se 

# Sonstiges
Zeilenabstand

    \linespread{ZAHL}

Seitenzahl
    
    \thepage

Seitennummerierung

    \pagenumbering{arabic}

Heutiges Datum

    \today

Tag.Monat.Jahr

    \number\day.\number\month.\number\year