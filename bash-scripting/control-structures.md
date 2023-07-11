# 🎛 Kontrollstrukturen

Kontrollstrukturen in der Linux Bash-Skripting ermöglichen es Ihnen, den Ablauf des Skripts basierend auf Bedingungen und Iterationen zu steuern. Sie bieten die Möglichkeit, Entscheidungen zu treffen, Codeblöcke bedingt auszuführen und Code wiederholt auszuführen. Das Verständnis von Kontrollstrukturen ist für das Schreiben effizienter und flexibler Skripte unerlässlich.

* [If/Else-Anweisungen](control-structures.md#ifelse-anweisungen)
  * [Grundlegende if-Anweisung](control-structures.md#grundlegende-if-anweisung)
  * [If/Else-Anweisung](control-structures.md#ifelse-anweisung)
  * [If/Else If/Else-Anweisung](control-structures.md#ifelse-ifelse-anweisung)
* [Schleifen](control-structures.md#schleifen)
  * [For-Schleife](control-structures.md#for-schleife)
  * [While-Schleife](control-structures.md#while-schleife)
  * [Until-Schleife](control-structures.md#until-schleife)
* [Fall-Anweisungen](control-structures.md#fall-anweisungen)

## If/Else-Anweisungen

Die `if/else`-Anweisungen sind bedingte Anweisungen im Bash-Skripting. Sie werden verwendet, um bestimmte Codeabschnitte auszuführen, basierend darauf, ob eine bestimmte Bedingung als wahr oder falsch ausgewertet wird. Wenn Sie eine `if`-Anweisung verwenden, überprüft das Skript eine bestimmte Bedingung, und wenn diese wahr ist, wird ein bestimmter Codeblock ausgeführt. Eine `else`-Anweisung kann verwendet werden, um einen alternativen Codeblock anzugeben, der ausgeführt wird, wenn die ursprüngliche Bedingung falsch ist. Lassen Sie uns ins Detail gehen:

### Grundlegende if-Anweisung

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

### If/Else-Anweisung

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

### If/Else If/Else-Anweisung

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

## Schleifen

Schleifen im Bash-Skripting werden verwendet, wenn Sie einen bestimmten Block von Befehlen mehrmals wiederholen müssen. Sie ermöglichen die Automatisierung wiederkehrender Aufgaben und machen Ihre Skripte effizienter und einfacher zu warten. Es gibt drei Arten von Schleifen, die in Bash häufig verwendet werden: `for`, `while` und `until`.

* [Schleifen](control-structures.md#schleifen)
  * [For-Schleife](control-structures.md#for-schleife)
  * [While-Schleife](control-structures.md#while-schleife)
  * [Until-Schleife](control-structures.md#until-schleife)

***

### For-Schleife

Die `for`-Schleife wird verwendet, wenn Sie einen Satz von Befehlen eine vordefinierte Anzahl von Malen ausführen möchten. Die grundlegende Syntax lautet:

```bash
for variable in liste
do
   # Auszuführende Befehle
done
```

Hier ist ein Beispiel:

```bash
for i in 1 2 3 4 5
do
   echo "Zahl ist $i"
done
```

In diesem Skript durchläuft die `for`-Schleife die Liste der Zahlen (1, 2, 3, 4, 5) und gibt für jede Iteration den aktuellen Wert von `i` aus.

***

### While-Schleife

Die `while`-Schleife wird verwendet, wenn Sie einen Satz von Befehlen so lange wiederholen möchten, wie eine bestimmte Bedingung wahr ist. Die grundlegende Syntax lautet:

```bash
while [bedingung]
do
   # Auszuführende Befehle
done
```

Hier ist ein Beispiel:

```bash
counter=1

while [ $counter -le 5 ]
do
   echo "Zähler ist $counter"
   ((counter++))
done
```

In diesem Skript gibt die `while`-Schleife weiterhin den Wert von `counter` aus und erhöht ihn, solange der Zähler kleiner oder gleich 5 ist.

***

### Until-Schleife

Die `until`-Schleife wird verwendet, wenn man ein Satz von Befehlen wiederholen möchten, bis eine bestimmte Bedingung wahr ist. Sie ist das Gegenteil einer `while`-Schleife, da der Codeblock ausgeführt wird, solange die Bedingung falsch ist. Die grundlegende Syntax lautet:

```bash
until [bedingung]
do
   # Auszuführende Befehle
done
```

Hier ist ein Beispiel:

```bash
counter=1

until [ $counter -gt 5 ]
do
   echo "Zähler ist $counter"
   ((counter++))
done
```

In diesem Skript gibt die `until`-Schleife weiterhin den Wert von `counter` aus und erhöht ihn, bis der Zähler größer als 5 ist.

## Fall-Anweisungen

Eine `case`-Anweisung, oft als `switch`-Anweisung in anderen Programmiersprachen bezeichnet, ermöglicht die Ausführung unterschiedlicher Codeblöcke basierend auf dem Wert einer bestimmten Variablen oder Ausdrucks. Sie ist effizienter und lesbarer als die Verwendung einer komplexen Kombination von `if/elif/else`-Anweisungen, insbesondere wenn es um mehrere mögliche Werte geht.

Hier ist die grundlegende Struktur einer `case`-Anweisung in Bash:

```bash
case expression in
    pattern1 )
        # Befehle, die ausgeführt werden sollen, wenn pattern1 übereinstimmt
        ;;
    pattern2 )
        # Befehle, die ausgeführt werden sollen, wenn pattern2 übereinstimmt
        ;;
    * )
        # Standardfall, Befehle, die ausgeführt werden sollen, wenn kein Muster übereinstimmt
        ;;
esac
```

Die `case`-Anweisung bewertet den gegebenen `expression` anhand der angegebenen Muster. Jedes Muster kann ein wörtlicher Wert oder ein regulärer Ausdruck sein. Der Codeblock für das erste Muster, das mit dem Ausdruck übereinstimmt, wird ausgeführt. Nach jedem Codeblock werden doppelte Semikolons `;;` verwendet, um das Ende dieses Abschnitts zu kennzeichnen.

Hier ist ein Beispiel:

```bash
read -p "Geben Sie einen Fruchtnamen ein: " frucht

case $frucht in
    "Apfel" )
        echo "Apfel schmeckt lecker."
        ;;
    "Banane" )
        echo "Ich mag Bananen."
        ;;
    * )
        echo "Unbekannte Frucht."
        ;;
esac
```

In diesem Skript überprüft die `case`-Anweisung den eingegebenen Fruchtnamen. Wenn es "Apfel" ist, gibt es "Apfel schmeckt lecker" aus. Wenn es "Banane" ist, gibt es "Ich mag Bananen" aus. Für jede andere Eingabe gibt es "Unbekannte Frucht" aus.

Die `case`-Anweisung ist nützlich, wenn Sie verschiedene Aktionen für verschiedene mögliche Werte einer Variablen durchführen müssen. Sie ist eine wichtige Kontrollstruktur, die die Flexibilität und Lesbarkeit Ihrer Bash-Skripte erheblich verbessern kann.

Es ist auch erwähnenswert, die Verwendung des Schlüsselworts `esac`. In Bash wird das Schlüsselwort `esac` verwendet, um die `case`-Anweisung zu beenden. Es ist praktisch das rückwärts geschriebene `case`. Zum Beispiel:

```bash
case $variable in
    pattern1 )
        # Befehle für pattern1
        ;;
    pattern2 )
        # Befehle für pattern2
        ;;
esac
```

Das Schlüsselwort `esac` kennzeichnet das Ende des `case`-Anweisungsblocks.

Die Verwendung des Schlüsselworts `esac` ist wichtig, um die korrekte Syntax und Beendigung der `case`-Anweisung sicherzustellen.
