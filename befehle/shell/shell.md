# Shell ⚙️

## Einführung

Die Linux-Shell, auch als Terminal bekannt, ist ein leistungsfähiges Werkzeug, das Benutzer verwenden können, um mit dem Linux-Betriebssystem zu interagieren. Sie kommuniziert direkt mit dem Kernel des Computers und ermöglicht es Benutzern, Aufgaben auszuführen, das System zu verwalten und Skripte zu automatisieren. Flexibilität, Automatisierungsmöglichkeiten und Zugang zu einer Vielzahl von Dienstprogrammen und Tools werden von Shell angeboten. Obwohl die Beherrschung der Linux-Shell anfangs eine Herausforderung darstellt, erhöht sie die Produktivität und ermöglicht eine effektive Systemverwaltung, Entwicklung und Forschung.

## Common Shells

### Bourne Again SHell

- Die Bash ist die in Linux-Distributionen am häufigsten verwendete Shell. Sie bietet eine Vielzahl von Funktionen, darunter Befehlszeilenbearbeitung, Verlauf, Tabulatorvervollständigung und Skripting-Funktionen.

### Z-Shell

- Zsh ist eine erweiterte Version der Bash mit zusätzlichen Funktionen und Anpassungsmöglichkeiten. Sie bietet leistungsstarke Vervollständigungsmechanismen, Rechtschreibkorrektur, Theming und Plugin-Unterstützung.

### Friendly Interactive SHell

- Fish ist eine benutzerfreundliche Shell, die für ihre Einfachheit bekannt ist. Sie bietet eine intuitive Befehlszeilenschnittstelle mit automatischen Vorschlägen, Syntaxhervorhebung und einem integrierten Hilfesystem.

## Shell Prompt

Der Shell-Prompt ist ein angezeigtes Zeichen oder eine Reihe von Zeichen, die anzeigen, dass die Shell bereit ist, Befehle anzunehmen. Er enthält normalerweise Informationen wie den Benutzernamen, den Hostnamen und das aktuelle Verzeichnis. Der Prompt kann je nach verwendeter Shell variieren und kann angepasst werden. Er bietet Kontext und dient als visueller Hinweis für Benutzer, die mit der Shell interagieren.

## Befehlszeile

Die Befehlszeile ist eine textbasierte Schnittstelle, mit der Benutzer mit dem Betriebssystem interagieren können, indem sie Befehle eingeben. Sie bietet eine direkte und effektive Möglichkeit, Aufgaben auszuführen, Prozesse zu automatisieren und auf Systemressourcen zuzugreifen. Zu den gängigen Befehlen gehören Datei- und Verzeichnisoperationen (ls, cd, mkdir, cp, rm), Systeminformationen (uname, top, df, free), Dateimanipulation (cat, grep, head, tail) und Systemverwaltung. Durch Shell-Skripting bietet die Kommandozeile Effizienz, Automatisierungsmöglichkeiten, Flexibilität und Erweiterbarkeit.

## Grundlegende Shell-Befehle

Die fünf wichtigsten grundlegenden Shell-Befehle:

- `ls`: Listet Dateien und Verzeichnisse im aktuellen Verzeichnis auf.

- `cd`: Wechselt das aktuelle Verzeichnis.
Beispiel: cd linux-cookbook

- `mkdir`: Erstellt ein neues Verzeichnis.
Beispiel: mkdir linux-distributionen

- `cp`: Kopiert Dateien und Verzeichnisse.
Beispiel: cp debian(Datei) linux-cookbook/linux-distributionen(Zielsort)

- `rm`: Entfernt Dateien und Verzeichnisse.
Beispiel: rm debian

## Datei und Verzeichnis

### Dateisystem-Hierarchie

- Das Linux-Dateisystem ist hierarchisch aufgebaut, wobei das Wurzelverzeichnis ("/") die oberste Ebene darstellt.

- Übliche Verzeichnisse sind /bin, /etc, /home, /tmp, /var, /usr, /dev und /proc.

### Dateioperationen

- `touch`, um eine leere Datei zu erstellen.
- `cat`, um den Inhalt einer Datei anzuzeigen.
- `cp`, um Dateien zu kopieren.
- `mv`, um Dateien zu verschieben oder umzubenennen.
- `rm`, um Dateien zu löschen.
- `chmod`, um die Dateiberechtigungen zu ändern.

### Verzeichnisoperationen

- `mkdir`, um Verzeichnisse zu erstellen.
- `ls`, um den Inhalt von Verzeichnissen aufzulisten.
- `cd`, um Verzeichnisse zu wechseln.
- `rmdir`, um leere Verzeichnisse zu löschen.
- `rm -r`, um Verzeichnisse und deren Inhalt zu löschen.
