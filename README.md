# README LaTexTemplate

LaTex Template für die Fachhochschule Münster - Fachbereich Wirtschaft.

## Overview

1. Master
2. Titel
3. Hauptteil
4. Eidesstattliche Erklärung

## Einrichtung Texmaker

* Master.tex muss als Masterdatei festgelegt werden

        Master.tex auswählen -> Optionen -> Aktuelle Datei zur Masterdatei erklären

* Literaturangaben und Inhaltsverzeichnisse erfordern eine zusätzliche übersetzung
    
        Master.tex auswählen -> Optionen -> Texmaker konfigurieren -> Reiter "Schnelles Übersetzen" -> "PdfLaTex + Biblatex + PdfLaTex (x2) + PDF anzeigen" auswählen (Punkt 2)

## Syntax und Beispiele

[COMMANDS.md](examples/COMMANDS.md)

## Packages

* geometry = Seitenränder / Layout
* setspace = Zeilenabstand
* hyperref = PDF Dokument Informationen
* inputenc = UTF-8
* babel = Deutsch
* fontenc = T1
* graphicsx, subfig = Grafiken
* fancyhdr = Kopf- und Fußzeile
* lmodern = Latin Schriftarten
* color = Farben
* amsfonts = Mathematik - Schriftart
* amsmath = Mathematik - Formeln
