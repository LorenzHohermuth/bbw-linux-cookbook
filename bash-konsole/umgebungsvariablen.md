# 🌱 Umgebungsvariablen

Umgebungsvariablen in Bash sind dynamische Werte, die das Verhalten und die Konfiguration einer Bash-Konsolen-Sitzung und der darin ausgeführten Programme beeinflussen können. Sie werden verwendet, um Informationen wie Systempfade, Benutzereinstellungen und Konfigurationseinstellungen zu speichern.

## Überblick

In der Bash sind Umgebungsvariablen Variablen, die in der Konsolen-Umgebung gesetzt werden und auf die jedes Programm oder Skript, das in dieser Umgebung läuft, zugreifen kann. Sie werden durch ein Name-Werte Paar (Key-Value) dargestellt, wobei der Name mit einem Wert verbunden wird.

Umgebungsvariablen können in zwei Typen unterteilt werden:

1. **Systemumgebungsvariablen**: Diese Variablen werden vom Betriebssystem gesetzt und sind für alle Benutzer und Programme auf dem System verfügbar. Sie definieren typischerweise systemweite Einstellungen wie Systempfade, Standardeditoren und Spracheinstellungen.

2. **Benutzer-Umgebungsvariablen**: Diese Variablen sind benutzerspezifisch und werden in der Umgebung des Benutzers gesetzt. Sie können verwendet werden, um benutzerspezifische Konfigurationen oder temporäre Variablen zu definieren, die von bestimmten Anwendungen benötigt werden.

## Umgebungsvariablen setzen

In Bash gibt es mehrere Möglichkeiten, Umgebungsvariablen zu setzen:

1. **Variablen in der aktuellen Konsole setzen**: Um eine Umgebungsvariable zu setzen, die nur in der aktuellen Konsolen-Sitzung verfügbar ist, kann der Befehl `export` verwendet werden. Die Syntax lautet wie folgt:

```bash
export VARIABLE_NAME=Wert
```

Um zum Beispiel die Variable `PATH` so zu setzen, dass sie zusätzliche Verzeichnisse enthält, können Sie den folgenden Befehl verwenden:

```bash
export PATH=$PATH:/pfad/zu/weiteren/verzeichnissen
```

2. **Dauerhaftes Setzen von Variablen**: Um Umgebungsvariablen zu setzen, die auch in zukünftigen Konsolen-Sitzungen verfügbar sein sollen, können die Variablen zur Konsolen-Konfigurationsdatei (`~/.bashrc` oder `~/.bash_profile`) hinzugefügt werden. Durch Hinzufügen des Befehls `export` zu einer dieser Dateien werden die Variablen automatisch gesetzt, wenn eine neue Konsolen-Sitzung gestartet wird.

3. **Temporäre Variablenzuweisung**: Umgebungsvariablen können auch temporär für die Dauer eines Befehls gesetzt werden. Dies wird erreicht, indem die Variable unmittelbar vor dem Befehl definiert wird, ohne `export` zu verwenden. Zum Beispiel:

```bash
VARIABLE_NAME=Wert Befehl
```

## Zugriff auf Umgebungsvariablen

Sobald eine Umgebungsvariable gesetzt ist, kann auf sie innerhalb eines Konsolen-Skripts oder direkt in der Konsole zugegriffen werden. Um auf eine Umgebungsvariable zuzugreifen, stellen Sie dem Variablennamen ein `$`-Zeichen voran. Um zum Beispiel auf den Wert der Variable `HOME` zuzugreifen, können Sie `$HOME` verwenden.

Hier ist ein simples Beispiel für den Zugriff auf eine Umgebungsvariable in Bash:

-   Um den Wert einer bestimmten Umgebungsvariablen anzuzeigen, können Sie den Befehl `echo` verwenden:

```bash
echo $VARIABLE_NAME
```

-   Umgebungsvariablen können auch innerhalb von Skripten für bedingte Anweisungen, Schleifen oder jede andere erforderliche Verarbeitung verwendet werden.

## Allgemeine Umgebungsvariablen

Bash stellt mehrere allgemeine Umgebungsvariablen zur Verfügung, von denen einige enthalten sind:

-   `HOME`: Repräsentiert das Home-Verzeichnis des Benutzers.
-   `PATH`: Gibt die Verzeichnisse an, in denen nach ausführbaren Programmen gesucht werden soll.
-   `USER`: Enthält den Benutzernamen des aktuell angemeldeten Benutzers.
-   `PWD`: Speichert das aktuelle Arbeitsverzeichnis.
-   `LANG` und `LC_*`: Bestimmen die Sprach- und Gebietsschemaeinstellungen.
-   `TERM`: Legt den Terminaltyp fest.

Dies sind nur einige Beispiele, und es gibt noch viele weitere Umgebungsvariablen, die je nach System und Konfiguration verfügbar sind.

## Abschliessend

Umgebungsvariablen spielen bei der Erstellung und Anpassung von Bash-Skripten eine entscheidende Rolle. Sie ermöglichen eine dynamische Konfiguration und Personalisierung der Konsolen-Umgebung und der darin ausgeführten Programme. Wenn man versteht, wie man Umgebungsvariablen setzt und darauf zugreift, erhält man Flexibilität und Kontrolle über das Verhalten des Systems und die benutzerspezifischen Einstellungen.
