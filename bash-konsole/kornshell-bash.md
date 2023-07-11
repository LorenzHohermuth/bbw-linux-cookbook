# 🥊 Bash vs KSH (Kornshell)

***

## Kurzfassung

Korn Shell wurde von David Korn einige Jahre vor der Bash-Shell entwickelt. Sie kombiniert Eigenschaften vieler anderer Shell-Typen wie der Bourne Shell oder der C-Shell. Da sie jedoch ziemlich alt ist, hat sie im Vergleich zur Bash eine begrenzte Anzahl von Nutzern. Bash ist insbesondere bei Linux-Liebhabern verbreitet, aufgrund von Funktionen wie assoziativen Arrays, Schleifenverarbeitung oder dem Druckbefehl.

***

## Features

### Korn Shell

Korn Shell bietet eine Vielzahl von Features. Hier sind einige wichtige Beispiele:

**Assoziative Arrays** KSH unterstützt assoziative Arrays, die es ermöglichen, Daten in Form von Schlüssel-Wert-Paaren zu speichern und abzurufen. Dies erleichtert die Verwaltung und den Zugriff auf strukturierte Daten.

**Schleifenverarbeitung** Die Korn Shell unterstützt verschiedene Arten von Schleifen, wie zum Beispiel "for"-Schleifen, "while"-Schleifen und "until"-Schleifen. Diese ermöglichen die wiederholte Ausführung von Befehlen oder Aktionen basierend auf bestimmten Bedingungen.

**Druckbefehl** Die KSH bietet den "print"-Befehl, der eine flexible und formatierte Ausgabe von Text ermöglicht. Dies umfasst die Möglichkeit, Variablen einzufügen und die Ausgabe zu formatieren, um sie leichter lesbar zu machen.

**Job Control** Die Korn Shell unterstützt die Verwaltung von Hintergrundprozessen und die Steuerung von laufenden Jobs. Dadurch können Benutzer mehrere Aufgaben parallel ausführen und zwischen ihnen wechseln.

**Fortgeschrittene Skripting-Fähigkeiten** Mit der Korn Shell können komplexe Skripts erstellt werden, die bedingte Anweisungen, Funktionen, Dateioperationen und andere fortgeschrittene Programmierkonstrukte enthalten. Dies ermöglicht die Automatisierung von Aufgaben und die Entwicklung umfangreicher Skripts.

\
\### Bash Shell Die Bash Shell verfügt ebenfalls über eine Reihe nützlicher Features. Hier sind einige wichtige Beispiele:

**History-Funktion** Bash speichert die Befehlshistorie, so dass Benutzer frühere Befehle leicht wieder aufrufen und bearbeiten können. Dies erleichtert die Navigation und den Zugriff auf zuvor verwendete Befehle.

**Kommandoerweiterung** Die Bash Shell unterstützt die Erweiterung von Kommandos durch die Verwendung von Platzhaltern, Variablen und Substitutionen. Dies ermöglicht eine dynamische und flexible Befehlsausführung.

**Integrierte Funktionen** Bash enthält eine Vielzahl von integrierten Funktionen, die direkt von der Shell aus aufgerufen werden können. Dies umfasst mathematische Berechnungen, Dateioperationen, Zeichenkettenmanipulation und vieles mehr.

**Tab-Vervollständigung** Bash bietet eine Tab-Vervollständigungsfunktion, die es Benutzern ermöglicht, Befehle, Dateinamen und Verzeichnisse automatisch zu vervollständigen. Dies spart Zeit und minimiert Tippfehler.

**Skripting-Funktionen** Die Bash Shell ermöglicht die Erstellung von Skripts, die bedingte Anweisungen, Schleifen, Funktionen und andere Programmierkonstrukte enthalten. Dies erleichtert die Automatisierung von Aufgaben und die Entwicklung komplexer Skripts.

***

## Technische Unterschide

Die Korn Shell (KSH) und die Bash Shell unterscheiden sich in mehreren technischen Aspekten. Hier sind einige aufgelistet:

**Syntax** Beide Shells haben unterschiedliche Syntaxregeln und Sprachkonstrukte. Die Korn Shell verwendet einen etwas älteren Syntax, der manchmal als weniger intuitiv und lesbar empfunden wird. Die Bash Shell hingegen verwendet eine modernere und benutzerfreundlichere Syntax, die leichter zu erlernen und zu verstehen ist.

**Variablenbehandlung** In der Korn Shell erfolgt die Behandlung von Variablen standardmäßig case-sensitive, während die Bash Shell standardmäßig case-insensitive ist. Das bedeutet, dass in der Korn Shell "VAR" und "var" als unterschiedliche Variablen betrachtet werden, während sie in der Bash Shell als dieselbe Variable gelten.

**Array-Unterstützung** Die Korn Shell unterstützt nur eindimensionale Arrays, während die Bash Shell auch assoziative Arrays ermöglicht. Assoziative Arrays erlauben den Zugriff auf Elemente nicht nur über numerische Indizes, sondern auch über Schlüsselwerte. Dies kann die Datenverwaltung und -manipulation in bestimmten Szenarien vereinfachen.

**Command-Line-Editing** Die Korn Shell bietet ein etwas einfacheres Command-Line-Editing im Vergleich zur Bash Shell. Die Bash Shell bietet zusätzliche praktische Funktionen, die die Benutzerfreundlichkeit erhöhen. Dazu gehören beispielsweise die Autovervollständigung von Befehlen und Pfaden durch Drücken der Tab-Taste, die einfache Suche nach zuvor verwendeten Befehlen mithilfe der Pfeiltasten und die Möglichkeit, Befehle aus der Befehlshistorie abzurufen und zu bearbeiten.

**Erweiterbarkeit** Beide Shells unterstützen die Möglichkeit, eigene Funktionen und Skripte zu erstellen. Die Bash Shell bietet jedoch eine breitere Palette an Erweiterungsmöglichkeiten und Add-Ons, da sie in der Linux-Community weit verbreitet und aktiv weiterentwickelt wird.

***

## Direkter Vergleich

| Kriterien                      | KSH       | Bash             |
| ------------------------------ | --------- | ---------------- |
| Script erweiterung             | .ksh      | .sh              |
| performance                    | sehr gut  | durchschnittlich |
| Speicherort                    | /bin/ksh. | /bin/bash.       |
| Anzahl Programmierung features | sehr viel | viel             |
| Binäre Größe                   | 1.6MB     | 1.1MB            |
| Leserlichkeit der Scripts      | schlecht  | gut              |
