# KornShell vs Shell

## Kurzfassung

Die Korn Shell (KSH) wurde einige Jahre vor der SH-Shell entwickelt. Sie kombiniert Eigenschaften vieler anderer Shell-Typen wie der Bourne Shell oder der C-Shell. Obwohl sie älter ist, hat sie im Vergleich zur Bash eine begrenzte Nutzerbasis. Die SH-Shell hingegen ist weit verbreitet und findet vor allem bei Unix-Systemen Anwendung.

## Features

### Korn Shell
Die Korn Shell bietet verschiedene nützliche Features. Hier sind einige wichtige Beispiele:


**Parametererweiterung**
Die KSH unterstützt Parametererweiterung, um Variablen oder Argumente in Skripten zu manipulieren. Dies ermöglicht das Extrahieren von Teilstrings, das Ersetzen von Zeichen und vieles mehr.

**Job Control**
Die Korn Shell ermöglicht die Verwaltung von Hintergrundprozessen und die Steuerung von laufenden Jobs. Dadurch können Benutzer mehrere Aufgaben parallel ausführen und zwischen ihnen wechseln.

**Mathematische Berechnungen**
Mit der Korn Shell können mathematische Berechnungen durchgeführt werden. Dies erleichtert die Ausführung von Berechnungen in Skripten.

**Dateioperationen**
Die KSH bietet verschiedene Funktionen zur Dateiverwaltung, wie das Überprüfen von Dateieigenschaften, das Lesen und Schreiben von Dateien und das Erstellen von Verzeichnissen.

**Bedingte Anweisungen**
Die Korn Shell unterstützt bedingte Anweisungen, um verschiedene Pfade in einem Skript basierend auf bestimmten Bedingungen auszuführen.

### Shell
Die SH-Shell bietet grundlegende Funktionen für die Arbeit mit der Kommandozeile. Hier sind einige wichtige Beispiele:
Befehlsausführung
Die SH-Shell ermöglicht die Ausführung von Befehlen und das Starten von Programmen von der Kommandozeile aus.

**Pipelines**
Mit der SH-Shell können Pipelines erstellt werden, um die Ausgabe eines Befehls als Eingabe für einen anderen Befehl zu verwenden. Dies ermöglicht die Kombination mehrerer Befehle, um komplexe Aufgaben zu erledigen.

**Dateimanipulation**
Die SH-Shell bietet grundlegende Funktionen zur Dateimanipulation, wie das Kopieren, Umbenennen und Löschen von Dateien.

**Umgebungsvariablen**
Die SH-Shell ermöglicht das Setzen und Verwalten von Umgebungsvariablen, die von Programmen und Skripten verwendet werden können.

**Benutzereingabe**
Die SH-Shell ermöglicht die Interaktion mit dem Benutzer durch das Lesen von Eingaben von der Kommandozeile.

## Technische Unterschiede
Die Korn Shell (KSH) und die SH-Shell unterscheiden sich in einigen technischen Aspekten. Hier sind einige aufgelistet:

**Syntax**
Beide Shells haben unterschiedliche Syntaxregeln und Sprachkonstrukte. Die Korn Shell verwendet einen etwas älteren Syntax, der manchmal als weniger intuitiv und lesbar empfunden wird. Die SH-Shell hingegen verwendet eine einfachere und grundlegendere Syntax.

**Variablenbehandlung**
Die Korn Shell behandelt Variablen standardmäßig case-sensitive, während die SH-Shell standardmäßig case-insensitive ist. Das bedeutet, dass in der Korn Shell "VAR" und "var" als unterschiedliche Variablen betrachtet werden, während sie in der SH-Shell als dieselbe Variable gelten.

**Array-Unterstützung**
Die Korn Shell unterstützt nur eindimensionale Arrays, während die SH-Shell keine eingebaute Unterstützung für Arrays bietet. Dies kann die Datenverwaltung und -manipulation in bestimmten Szenarien einschränken.

**Kommandoerweiterung**
Die Korn Shell bietet erweiterte Kommandoerweiterungsmöglichkeiten, wie beispielsweise die Verwendung von Platzhaltern und Variablen. Die SH-Shell hingegen bietet keine solche Erweiterungsmöglichkeit.

**Erweiterbarkeit**
Beide Shells unterstützen die Möglichkeit, eigene Funktionen und Skripte zu erstellen. Die Korn Shell bietet jedoch eine breitere Palette an Erweiterungsmöglichkeiten und Add-Ons, da sie von einer größeren Community unterstützt wird.

## Direkter Vergleich

Kriterien | KSH | Shell
-------- | -------- | --------
Verbreitung  | Begrenzt   | Weit verbreitet
Verfügbarkeit   | Abhängig vom System   | Auf den meisten Unix-Systemen verfügbar
Syntax   | etwas älter  | Einfach und grundlegend
Variablenbehandlung  | Case-sensitive  | Case-insensitive
Binäre Größe   | 1.6MB  | 1.1MB
