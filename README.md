# dhbw-hdh-wi-latex

LaTeX Template für wissenschaftliche Arbeiten an der DHBW Heidenheim im Studiengang Wirtschaftsinformatik (nicht offiziell, siehe [Zusatz](###Wichtig)).

## Grundlage

Die Grundlage dieses Templates bilden die [Richtlinien zur Erstellung wissenschaftlicher Arbeiten](Richtlinien_wissenschaftliche_Arbeiten.pdf) des Studiengangs Wirtschaftsinformatik an der DHBW Heidenheim (heruntergeladen von <http://www.heidenheim.dhbw.de/fileadmin/Heidenheim/Studienangebot/Bachelor_Wirtschaft/Wirtschaftsinformatik/Informationen_fuer_Studierende/Richtlinien_wissenschaftliche_Arbeiten.pdf>, Stand: März 2019)>.

## LaTeX Installation

### LaTeX-Distribution

#### Windows

[MiKTeX-Distribution](https://miktex.org/download) herunterladen und installieren (getestet mit Windows 10 Pro).

#### Linux

Tex Live-Distribution herunterladen und installieren über das Terminal mit `sudo apt-get install texlive texlive-lang-german texlive-latex-extra` (getestet mit Ubuntu 18.04).

#### Mac

[MacTeX-Distribution](http://www.tug.org/mactex/) herunterladen und installieren (nicht getestet).

### LaTeX-Editor

Zum Bearbeiten von LaTeX-Dateien wird ein LaTeX-Editor benötigt. Hier gibt es viele verschiedene Alternativen, die zum Großteil kostenlos zum Download bereitstehen. Zu den am weitesten verbreiteten und bekanntesten Editoren gehören:

- [TeXmaker](http://www.xm1math.net/texmaker/)
- [TeXstudio](http://texstudio.sourceforge.net/)
- [TeXworks](https://www.tug.org/texworks/)

*Info: Für Visual Studio Code Nutzer besteht ebenfalls die Möglichkeit, Visual Studio Code als Editor für LaTeX mit der Erweiterung LaTeX Workshop zu nutzen.*

## LaTeX lernen

Hier ein paar Resourcen, um sich besser in LaTeX einzuarbeiten:

- Online Tutorial: [LaTeX Tutorial](http://latex.hpfsc.de/content/latex_tutorial/)
- PDF der FernUniversität Hagen: [LaTeX - eine Einführung und ein bisschen mehr...](https://www.fernuni-hagen.de/imperia/md/content/zmi_2010/a026_latex_einf.pdf)
- Buch: [LaTeX für Dummies](https://www.amazon.de/LaTeX-f%C3%BCr-Dummies-Rainer-Griesbaum/dp/3527713085/ref=sr_1_1?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=LaTeX+buch&qid=1553864882&s=gateway&sr=8-1)

## Aufbau / Konfiguration des Templates

### dokument.tex

Zentrales Element des Templates ist die Datei [dokument.tex](dokument.tex). Sie inkludiert alle anderen .tex-Dateien in den Unterordnern und enthält mehrere Konfigurationsmöglichkeiten.

#### dokument.tex konfigurieren

Die Datei sollte nur an zwei Stellen konfiguriert werden:

- **Allgemeine Informationen**: Hier kann beispielsweise der Titel der Arbeit, der Name des Autors, der Gutachter und vieles mehr eingestellt werden. Die allgemeinen Informationen werden an mehreren Stellen im Dokument wiederverwendet, z.B. auf dem Titelblatt, im Sperrvermerk oder in der ehrenwörtlichen Erklärung.

- **Zusätzliche Konfiguration**: Zusätzliche Konfiguration betrifft hauptsächlich das Inkludieren oder Exkludieren von bestimmten Standardkomponenten wie z.B. den Sperrvermerk, das Vorwort oder das Abkürzungsverzeichnis. Auch kann hier eingestellt werden, ob auf dem Titelblatt das DHBW- sowie das Unternehmenslogo dargestellt werden soll (für weiter Informationen siehe [logos](###logos)).

*Die beiden konfigurierbaren Abschnitte in dokument.tex können gefunden werden, indem nach "Ändern!!!" in der Datei gesucht wird.*

#### Beispieldokument

Das Repository enthält das [Beispieldokument](dokument.pdf), das entsteht, wenn das Template ohne Änderungen zu einem PDF konvertiert wird. Es dient als Vorschau dafür, wie die finale Arbeit in etwa aussehen wird.

### standardkomponenten

Der Ordner [standardkomponenten](standardkomponenten) enthält alle in den [Richtlinien zur Erstellung wissenschaftlicher Arbeiten](Richtlinien_wissenschaftliche_Arbeiten.pdf) aufgeführten Komponenten, die eine wissenschaftliche Arbeit benötigt wie z.B. Titelblatt, Abkürzungsverzeichnis, Abbildungsverzeichnis, Anhang, etc. **An diesem Ordner sollte möglichst nichts geändert werden.**

### literatur

Der Ordner [literatur](literatur) enthält eine einzelne Datei namens `bibfile.bib`. Hier werden Literaturangaben im BibTex-Format, dem Literaturformat für LaTeX-Dokumente, gespeichert. In diese Datei muss jegliche in der Arbeit verwendete Literatur eingetragen werden, damit sie in der Arbeit zitiert werden kann.

*Literaturverwaltungsprogramme wie [Zotero](https://www.zotero.org/) bieten im Regelfall die Möglichkeit ganze Bibliotheken oder zumindest einzelne Literaturangaben im BibTex-Format als .bib-Datei zu exportieren. Auf vielen Internetseiten mit wissenschaftlichen Veröffentlichungen (siehe z.B. [sciencedirect](https://www.sciencedirect.com)) werden BibTex-Literaturangaben zu den jeweiligen Artikeln bereits bereitgestellt.*

### kapitel

Die einzelnen Kapitel der wissenschaftlichen Arbeit müssen im Unterordner [kapitel](kapitel) als .tex-Dateien abgelegt werden. Sie sollten möglichst mit einem `\chapter{Kapitelname}` starten. Die .tex-Dateien der Kapitel sind von 01-99 in der Reihenfolge durchzunummerieren, in der sie im finalen Dokument eingebunden werden sollen (siehe [kapitel](kapitel) als Beispiel). Alle .tex-Dateien werden in dieser Reihenfolge von [dokument.tex](dokument.tex) inkludiert.

### logos

Der Ordner [logos](logos) genau zwei Dateien. Das Logo der DHBW Heidenheim als `dhbw.png` sowie das Logo des Ausbildungsunternehmens als `unternehmen.png`. Die beiden Logos werden nur benötigt, wenn in [dokument.tex](dokument.tex) `logosauftitelblatt` auf `true` gesetzt ist. Die Datei `unternehmen.png` sollte dann natürlich durch das Logo des eigenen Ausbildungsunternehmens ersetzt werden.

### bilder

Der Ordner [bilder](bilder) ist der zentrale Sammelplatz für alle Bilder, die für die Arbeit benötigt werden.

## Zusatz

### LaTeX Cheatsheet

Das [LaTeX Cheatsheet](latexsheet-de.pdf) enthält nützliche Befehle, um mit LaTeX zu starten (heruntergeladen von <http://mirrors.ibiblio.org/CTAN/info/latexcheat/latexcheat-de/latexsheet-de.pdf>).

### Wichtig

Dieses Repository ist kein offizielles Repository der DHBW Heidenheim. Das LaTeX-Template ist deshalb auf eigene Verantwortung hin zu nutzen. Bitte besprechen Sie die Verwendung dieses Templates für Ihre Arbeiten mit Ihrem wissenschaftlichen und betrieblichen Betreuer und ändern Sie es, wenn nötig, ab.

*Verbesserungsvorschläge und oder Pull-Requests sind gerne willkommen.*