# Bash-Scripting

Bash Scripting ist ein leistungsstarker Teil der Systemverwaltung und -entwicklung, der auf extremer Ebene eingesetzt wird. Es wird von Systemadministratoren, Netzwerkingenieuren, Entwicklern, Wissenschaftlern und allen verwendet, die das Linux/Unix-Betriebssystem verwenden. Sie verwenden Bash für die **Systemverwaltung, die Datenverarbeitung, die Bereitstellung von Webanwendungen, automatisierte Backups, die Erstellung benutzerdefinierter Scripts für verschiedene Seiten** usw.

***Script***

In der Computerprogrammierung ist ein Script eine Reihe von Befehlen für eine entsprechende Laufzeitumgebung, die zur Automatisierung der Ausführung von Aufgaben verwendet werden.

## Bash-Script:

Ein Bash-Shell-Script ist eine reine Textdatei, die eine Reihe verschiedener Befehle enthält, die wir normalerweise in die Befehlszeile eingeben. Es wird verwendet, um sich wiederholende Aufgaben im Linux-Dateisystem zu automatisieren. Es kann eine Reihe von Befehlen oder einen einzelnen Befehl umfassen oder die Merkmale der imperativen Programmierung wie Schleifen, Funktionen, bedingte Konstrukte usw. enthalten. *Tatsächlich ist ein Bash-Script ein Computerprogramm, das in der Programmiersprache Bash geschrieben ist.*

### Wie erstelle und führe ich ein Bash-Script aus?

- Um ein leeres Bash-Script zu erstellen, ändern Sie zunächst mit dem Befehl *cd* das Verzeichnis, in dem Sie Ihr Script speichern möchten . Versuchen Sie, einen Texteditor wie **gedit** zu verwenden , in den Sie die Shell-Befehle eingeben möchten.
- Verwenden Sie den **Touch** -Befehl, um das Script mit der Grösse Null Bytes zu erstellen.

        touch file_name
        
- Geben Sie Folgendes ein, um das Script im Texteditor (z. B. gedit) zu öffnen:

        gedit file_name.sh  

Hier wird **.sh** als Erweiterung angehängt, die Sie für die Ausführung bereitstellen müssen.

- Geben Sie die Shell-Befehle für Ihr Bash-Script in das neu geöffnete Textfenster oder den Texteditor ein. Bevor Sie Bash-Shell-Befehle eingeben, sehen Sie sich zunächst die Basis eines beliebigen Bash-Scripts an.

Jedes Bash-basierte Linux-Script beginnt mit der Zeile-

        #! /bin/bash  

Wo #! wird als **Shebang** bezeichnet und der Rest der Zeile ist der Path zum Interpreter, der den Speicherort der Bash-Shell in unserem Betriebssystem angibt.

Bash verwendet #, um eine beliebige Zeile zu kommentieren.

Bash verwendet den **Echo** Befehl, um die Ausgabe zu drucken.

Führen Sie am Ende das Bash-Script mit dem Präfix ./ aus.

Schauen Sie sich die Grundbegriffe eines Bash-Scripts an, z. B. **SheBang** und *Echo* Befehl.


## SheBang (#!)

Das **She Bang (#!)** ist eine String, die aus den Zeichen Nummernzeichen (#) und Ausrufezeichen (!) am Anfang eines Scripts besteht.

Wenn unter Unix-ähnlichen Betriebssystemen ein Script mit einem Shebang als Programm ausgeführt wird, analysiert der Programmlader die restlichen Zeilen, wobei die erste Zeile als Interpreteranweisung dient. SheBang bezeichnet also einen Interpreter zum Ausführen der Scriptzeilen und ist als ***Path Directive*** für die Ausführung verschiedener Arten von Scripten wie Bash, Python usw. bekannt.

Hier ist das richtige SheBang-Format für das besprochene Bash-Script.

    #!/bin/bash  

Die Formatierung für Shebang ist am wichtigsten. Das falsche Format kann dazu führen, dass Befehle nicht ordnungsgemäss funktionieren. Denken Sie also beim Erstellen eines Scripts immer an diese beiden Punkte der SheBang-Formatierung:

1. Es sollte immer in der allerersten Zeile des Scripts stehen.  

2. Vor dem Hash (#), zwischen den Hash-Ausrufezeichen (#!) und dem Path zum Interpreter darf kein Leerzeichen stehen.

## echo

echo ist ein in Bash integrierter Befehl, der zur Anzeige der Standardausgabe durch Übergabe der Argumente verwendet wird. Dies ist der am häufigsten verwendete Befehl zum Drucken von Textzeilen/Strings auf dem Bildschirm. Die Leistung ist auf beiden Plattformen gleich: Bash Shell und Command Line Terminal.

**Syntax:**

    echo [Option] [String]  
    echo [String]  

*Hinwies:*
>Wenn Sie Leerzeichen zwischen zwei beliebigen Zeilen Ihres Scripts drucken möchten. Geben Sie dann echo wie unten angegeben ein:

    echo