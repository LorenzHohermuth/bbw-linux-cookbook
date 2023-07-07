# Erweiterte Syntax

Zusätzlich zur grundlegenden Syntax von Funktionen bietet Linux erweiterte Funktionen, die mehr Flexibilität und Kontrolle innerhalb von Funktionen ermöglichen. In diesem Abschnitt werden wir einige dieser erweiterten Syntaxoptionen untersuchen, darunter:

- Übergabe von Argumenten per Referenz
- Verwendung von lokalen und globalen Variablen
- Behandlung des Gültigkeitsbereichs von Variablen
- Rückgabe von Werten aus Funktionen

Lassen Sie uns jeden dieser Punkte genauer betrachten:

### Übergabe von Argumenten per Referenz

Standardmäßig werden in Linux Argumente, die an eine Funktion übergeben werden, per Wert übergeben, was bedeutet, dass die Funktion eine Kopie des Argumentwerts erhält. Es ist jedoch auch möglich, Argumente per Referenz zu übergeben, sodass die Funktion den ursprünglichen Wert des Arguments direkt ändern kann.

Um ein Argument per Referenz zu übergeben, kann man das `&`-Symbol vor dem Argumentnamen verwenden, um die Funktion definieren. Hier ist ein Beispiel:

```bash
increment() {
    local -n num_ref=$1  # Erstellt eine Referenz auf die als erstes Argument übergebene Variable
    ((num_ref++))  # Inkrementiert den Wert der referenzierten Variable
}

count=5
increment count
echo "Neuer Wert von count: $count"
```

In diesem Beispiel nimmt die Funktion `increment` ein Argument `num_ref` entgegen, das eine Referenz auf eine Variable ist. Die Syntax `local -n` wird verwendet, um eine Referenz auf die als erstes Argument übergebene Variable (`count`) zu erstellen. Die Anweisung `((num_ref++))` inkrementiert den Wert der referenzierten Variable, was den ursprünglichen Wert von `count` direkt ändert. Als Ergebnis wird "Neuer Wert von count: 6" ausgegeben.

Das Übergeben von Argumenten per Referenz kann nützlich sein, wenn eine Funktion den Wert einer Variablen außerhalb ihres Gültigkeitsbereichs ändern soll.

### Verwendung von lokalen und globalen Variablen

In Funktionen können sowohl lokale als auch globale Variablen verwendet werden. Lokale Variablen werden innerhalb des Gültigkeitsbereichs der Funktion deklariert und sind nur innerhalb der Funktion zugänglich. Globale Variablen werden hingegen außerhalb von Funktionen deklariert und können von allen Funktionen im Skript verwendet werden.

Um auf eine globale Variable innerhalb einer Funktion zuzugreifen, kann man einfach den Namen verwenden. Hier ist ein Beispiel:

```bash
global_var=42

print_global() {
    echo "Wert der globalen Variable: $global_var"
}

print_global
```

In diesem Beispiel greift die Funktion `print_global` auf den Wert der globalen Variable `global_var` zu und gibt ihn aus.

Lokale Variablen hingegen werden mit dem Schlüsselwort `local` innerhalb der Funktion deklariert. Sie haben einen separaten Gültigkeitsbereich innerhalb der Funktion und beeinflussen keine Variablen mit demselben Namen außerhalb der Funktion. Hier ist ein Beispiel:

```bash
print_local() {
    local local_var="Hallo, lokal!"
    echo "$local_var"
}

print_local
```

In diesem Beispiel deklariert die Funktion `print_local` eine lokale Variable `local_var` und weist ihr einen Wert zu. Der Wert wird innerhalb der Funktion ausgegeben. Die lokale Variable `local_var` beeinflusst keine Variable mit demselben Namen außerhalb der Funktion.

### Behandlung des Gültigkeitsbereichs von Variablen

Der Gültigkeitsbereich einer Variablen bezieht sich auf den Teil des Skripts, in dem eine Variable sichtbar ist und darauf zugegriffen werden kann. In Linux haben Variablen, die außerhalb von Funktionen deklariert werden, einen globalen Gültigkeitsbereich und können von allen Funktionen verwendet werden. Variablen, die innerhalb einer Funktion deklariert werden, haben hingegen einen lokalen Gültigkeitsbereich und sind nur innerhalb dieser Funktion zugänglich.

Es ist wichtig zu beachten, dass lokale Variablen Vorrang vor globalen Variablen mit demselben Namen haben. Wenn innerhalb einer Funktion eine lokale Variable mit demselben Namen wie eine globale Variable deklariert wird, wird die lokale Variable anstelle der globalen verwendet.

Hier ist ein Beispiel zur Veranschaulichung des Gültigkeitsbereichs von Variablen:

```bash
global_var=42

change_var() {
    local local_var=10
    echo "Wert der lokalen Variable: $local_var"
}

echo "Wert der globalen Variable: $global_var"
change_var
```

In diesem Beispiel haben wir eine globale Variable `global_var` mit einem Wert von `42`. Die Funktion `change_var` deklariert eine lokale Variable `local_var` mit einem Wert von `10` und gibt ihren Wert innerhalb der Funktion aus. Außerhalb der Funktion geben wir den Wert der globalen Variable aus. Die Ausgabe lautet:

```
Wert der globalen Variable: 42
Wert der lokalen Variable: 10
```

Wie man sieht, ist die lokale Variable `local_var` nur innerhalb der Funktion `change_var` zugänglich, während die globale Variable `global_var` sowohl innerhalb als auch außerhalb der Funktion zugänglich ist.

### Rückgabe von Werten aus Funktionen

Funktionen in Linux können Werte mit der `return`-Anweisung zurückgeben. Der zurückgegebene Wert kann durch Zuweisen des Funktionsaufrufs an eine Variable erfasst werden. Hier ist ein Beispiel:

```bash
multiply() {
    local result=$(( $1 * $2 ))  # Multipliziert das erste und das zweite Argument und speichert das Ergebnis
    return $result  # Gibt das Ergebnis zurück
}

product=$(multiply 5 3)  # Ruft die Funktion 'multiply' auf und speichert den zurückgegebenen Wert in der Variablen 'product'
echo "Das Produkt ist: $product"
```

In diesem Beispiel multipliziert die Funktion `multiply` die ersten beiden Argumente (`$1` und `$2`) und speichert das Ergebnis in der Variablen `result`. Die `return`-Anweisung wird verwendet, um den Wert von `result` aus der Funktion zurückzugeben. Der zurückgegebene Wert wird dann mit der Zuweisung `$(multiply 5 3)` in der Variablen `product` erfasst. Schließlich wird der in `product` gespeicherte Wert ausgegeben, was zu der Ausgabe "Das Produkt ist

: 15" führt.

Die Rückgabe von Werten aus Funktionen ermöglicht es Ihnen, Berechnungen oder Operationen innerhalb der Funktion durchzuführen und Ergebnisse zu erhalten, die in Ihrem Skript weiterverwendet werden können.

Mit den oben diskutierten erweiterten Syntaxoptionen kann man die Möglichkeiten von Funktionen in Linux nutzen, um flexibleren und wiederverwendbaren Code zu erstellen. Diese Funktionen bieten eine größere Kontrolle über die Handhabung von Variablen und ermöglichen es Ihnen, Funktionen zu entwerfen, die Variablen ändern, auf globale Werte zugreifen und Ergebnisse zurückgeben können.