## Grundlegende Syntax

Funktionen in Linux werden mit folgender Syntax definiert:

```bash
funktionsname() {
    # Funktionskörper
    # Auszuführende Anweisungen
}
```

Lassen Sie uns die Syntax aufschlüsseln:

- `funktionsname`: Dies ist der Name der Funktion, die man definieren möchten. Wähle einen aussagekräftigen Namen, der den Zweck der Funktion beschreibt.

- `()`: Die Klammern zeigen an, dass man eine Funktion definiert. Man kann Parameter innerhalb dieser Klammern übergeben, wenn Ihre Funktion Eingaben erfordert.

- `{}`: Die geschweiften Klammern umschließen den Körper der Funktion. Hier schreibt man die Anweisungen oder Befehle, die die Funktion ausführen soll.

- `# Funktionskörper`: Dies ist ein Kommentar, den man hinzufügen kann, um eine kurze Beschreibung oder den Zweck der Funktion anzugeben. Es ist optional, aber empfohlen, um eine bessere Dokumentation des Codes zu ermöglichen.

- `# Auszuführende Anweisungen`: Dies sind die tatsächlichen Befehle oder Anweisungen, die die Funktion ausführen wird, wenn sie aufgerufen wird.

Hier ist ein Beispiel für eine einfache Funktion, die eine Nachricht ausgibt:

```bash
greet() {
    echo "Hallo, Welt!"
}
```

Um diese Funktion zu verwenden, kann man sie einfach mit ihrem Namen aufrufen:

```bash
greet
```

Wenn die Funktion `greet` aufgerufen wird, wird die Anweisung `echo "Hallo, Welt!"` ausgeführt und die Nachricht "Hallo, Welt!" auf dem Bildschirm ausgegeben.

Funktionen in Linux bieten eine Möglichkeit, Code zu organisieren und wiederzuverwenden. Sie ermöglichen es, komplexe Aufgaben in kleinere, überschaubare Codeblöcke aufzuteilen, die mehrmals im Skript aufgerufen werden können.