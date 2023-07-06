## Variablen in Funktionen

Variablen werden in Funktionen verwendet, um Daten zu speichern und zu manipulieren. Sie ermöglichen es Ihnen, mit dynamischen Werten innerhalb des Funktionsbereichs zu arbeiten. Schauen wir uns an, wie Variablen im Kontext von Funktionen verwendet werden:

### Variablennamen

In Linux werden Variablen normalerweise mit Kleinbuchstaben und Unterstrichen benannt. Sie können Buchstaben, Ziffern und Unterstriche enthalten, müssen jedoch mit einem Buchstaben oder Unterstrich beginnen.

### Lokale Variablen

Lokale Variablen sind Variablen, die innerhalb des Gültigkeitsbereichs einer bestimmten Funktion definiert und verwendet werden. Sie werden mit dem Schlüsselwort `local` deklariert. Hier ist ein Beispiel:

```bash
gruessen() {
    local name="John"  # Deklarieren und Zuweisen einer lokalen Variablen mit dem Namen 'name'
    echo "Hallo, $name!"
}

gruessen  # Aufruf der Funktion 'gruessen'
```

In diesem Beispiel wird das Schlüsselwort `local` verwendet, um die Variable `name` innerhalb der Funktion `gruessen` zu deklarieren. Der Wert "John" wird der Variable `name` zugewiesen und innerhalb der Funktion ausgegeben.

### Funktionsparameter

Funktionsparameter sind Variablen, mit denen Sie Werte an eine Funktion übergeben können. Sie werden mit speziellen Variablen wie `$1`, `$2` usw. abgerufen. Hier ist ein Beispiel:

```bash
gruessen() {
    local name=$1  # Weisen Sie der Variablen 'name' den Wert des ersten Arguments zu
    echo "Hallo, $name!"
}

gruessen "Alice"  # Geben Sie den Wert "Alice" an die Funktion 'gruessen' weiter
```

In diesem Beispiel wird der Variablen `name` innerhalb der Funktion `gruessen` der Wert übergeben, der als erstes Argument (`$1`) übergeben wird. Der Wert "Alice" wird dann innerhalb der Funktion ausgegeben.

### Rückgabewerte

Funktionen können Rückgabewerte mit der `return`-Anweisung zurückgeben. Der zurückgegebene Wert kann durch Zuweisen des Funktionsaufrufs einer Variablen erfasst werden. Hier ist ein Beispiel:

```bash
multiplizieren() {
    local ergebnis=$(( $1 * $2 ))  # Multiplizieren Sie das erste und das zweite Argument und speichern Sie das Ergebnis
    return $ergebnis  # Geben Sie das Ergebnis zurück
}

produkt=$(multiplizieren 5 3)  # Rufen Sie die Funktion 'multiplizieren' auf und speichern Sie den zurückgegebenen Wert in der Variablen 'produkt'
echo "Das Produkt ist: $produkt"
```

In diesem Beispiel multipliziert die Funktion `multiplizieren` die ersten beiden Argumente (`$1` und `$2`) und speichert das Ergebnis in der Variablen `ergebnis`. Die `return`-Anweisung wird verwendet, um den Wert von `ergebnis` aus der Funktion zurückzugeben. Der zurückgegebene Wert wird dann mit der Zuweisung `$(multiplizieren 5 3)` in der Variablen `produkt` erfasst. Schließlich wird der Wert in der Variablen `produkt` ausgegeben.

Die Verwendung von Variablen in Funktionen ermöglicht es Ihnen, Daten zu speichern, zu manipulieren und zurückzugeben, wie es erforderlich ist. Sie bieten Flexibilität und ermöglichen Ihnen, verschiedene Operationen basierend auf Eingabewerten durchzuführen. Dadurch werden die Funktionen leistungsfähiger und wiederverwendbar.