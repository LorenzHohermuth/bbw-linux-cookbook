# Fall-Anweisungen

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