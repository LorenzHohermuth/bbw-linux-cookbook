# Schleifen

Schleifen im Bash-Skripting werden verwendet, wenn Sie einen bestimmten Block von Befehlen mehrmals wiederholen müssen. Sie ermöglichen die Automatisierung wiederkehrender Aufgaben und machen Ihre Skripte effizienter und einfacher zu warten. Es gibt drei Arten von Schleifen, die in Bash häufig verwendet werden: `for`, `while` und `until`.

* ## [For-Schleife](#for "for-Schleife")
* ## [While-Schleife](#while "while-Schleife")
* ## [Until-Schleife](#until "until-Schleife")

---

## For-Schleife

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

---

## While-Schleife

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

---

## Until-Schleife

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