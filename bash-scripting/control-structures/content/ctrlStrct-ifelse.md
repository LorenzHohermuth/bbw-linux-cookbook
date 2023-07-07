# If/Else-Anweisungen

Die `if/else`-Anweisungen sind bedingte Anweisungen im Bash-Skripting. Sie werden verwendet, um bestimmte Codeabschnitte auszuführen, basierend darauf, ob eine bestimmte Bedingung als wahr oder falsch ausgewertet wird. Wenn Sie eine `if`-Anweisung verwenden, überprüft das Skript eine bestimmte Bedingung, und wenn diese wahr ist, wird ein bestimmter Codeblock ausgeführt. Eine `else`-Anweisung kann verwendet werden, um einen alternativen Codeblock anzugeben, der ausgeführt wird, wenn die ursprüngliche Bedingung falsch ist. Lassen Sie uns ins Detail gehen:

## Grundlegende if-Anweisung

Eine einfache `if`-Anweisung kann im folgenden Format geschrieben werden:

```bash
if [Bedingung]
then
   # Code, der ausgeführt wird, wenn die Bedingung wahr ist
fi
```

Beispiel:

```bash
if [ "$1" -gt "100" ]
then
   echo "Die Zahl ist größer als 100."
fi
```

In dem obigen Skript überprüft die Bedingung, ob das erste Argument der Befehlszeile größer als 100 ist. Wenn dies der Fall ist, gibt das Skript die Nachricht aus.

## If/Else-Anweisung

Die `if/else`-Anweisung wird verwendet, wenn Sie einen Codeblock ausführen möchten, wenn eine Bedingung wahr ist, und einen anderen Block, wenn die Bedingung falsch ist:

```bash
if [Bedingung]
then
   # Code, der ausgeführt wird, wenn die Bedingung wahr ist
else
   # Code, der ausgeführt wird, wenn die Bedingung falsch ist
fi
```

Beispiel:

```bash
if [ "$1" -gt "100" ]
then
   echo "Die Zahl ist größer als 100."
else
   echo "Die Zahl ist nicht größer als 100."
fi
```

In diesem Skript wird, wenn das erste Argument der Befehlszeile nicht größer als 100 ist, eine andere Nachricht angezeigt.

## If/Else If/Else-Anweisung

Diese Anweisung wird verwendet, wenn Sie mehrere Bedingungen überprüfen und für jede eine andere Codeblock ausführen möchten. Wenn keine der Bedingungen wahr ist, führt das Skript den Codeblock in der `else`-Anweisung aus:

```bash
if [Bedingung1]
then
   # Code, der ausgeführt wird, wenn Bedingung1 wahr ist
elif [Bedingung2]
then
   # Code, der ausgeführt wird, wenn Bedingung2 wahr ist
else
   # Code, der ausgeführt wird, wenn keine der Bedingungen wahr ist
fi
```

Beispiel:

```bash
if [ "$1" -gt "100" ]
then
   echo "Die Zahl ist größer als 100."
elif [ "$1" -eq "100" ]
then
   echo "Die Zahl ist gleich 100."
else
   echo "Die Zahl ist kleiner als 100."
fi
```

In diesem Skript wird, wenn das erste Argument der Befehlszeile nicht größer als 100 ist, aber gleich 100, eine spezifische Nachricht angezeigt. Wenn die Zahl kleiner

als 100 ist, wird eine andere Nachricht angezeigt.

In all diesen Beispielen beachten Sie die Verwendung von eckigen Klammern `[...]` für Bedingungen. Im Bash-Skripting werden Bedingungen oft innerhalb dieser Klammern ausgedrückt. Es können verschiedene Bedingungen getestet werden, wie den Wert von Variablen, arithmetische Vergleiche oder den Status einer Datei. Die Bedingungen in den Beispielen sind arithmetische Vergleiche. Andere Formen von Bedingungen können genauso einfach in `if/else`-Anweisungen implementiert werden.