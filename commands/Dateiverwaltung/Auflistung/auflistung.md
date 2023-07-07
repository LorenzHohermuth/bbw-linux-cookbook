## Auflisten von Dateien innerhalb eines Verzeichnisses

* **ls -l** :Zeigt Dateien und Verzeichnisse im aktuellen Verzeichnis im langen TabellenFormat an (Es wird empfohlen, -l mit ls zu verwenden, um die Lesbarkeit zu verbessern).
* **ls -ld dir-name** : Zeigt Informationen über das Verzeichnis dir-name anstelle seines Inhalts an.
* **ls -a** : Zeigt alle Dateien an, einschließlich der versteckten Dateien (Dateinamen, die mit einem Punkt beginnen, sind in Linux versteckte Dateien).
* **ls -F** : Zeigt Inhalt eines Verzeichnisses an und kennzeichnet Dateien und Verzeichnisse. <br>
Die Option "-F" fügt dem Dateinamen ein spezielles Zeichen hinzu, um den Dateityp anzuzeigen. Es gibt verschiedene Symbole, die angehängt werden: <br>

    * Ein Schrägstrich (/) zeigt an, dass es sich um ein Verzeichnis handelt.
    * Ein Sternchen (*) zeigt an, dass es sich um eine ausführbare Datei handelt.
    * Ein At-Zeichen (@) zeigt an, dass die Datei erweiterte Attribute hat.
    * Ein Gleichheitszeichen (=) zeigt an, dass die Datei eine Verbindung zu einem anderen Dateisystemobjekt hat.
    * Ein senkrechter Strich (|) zeigt an, dass es sich um eine FIFO-Pipe handelt.
    * Ein Klammeraffe (@) zeigt an, dass es sich um einen symbolischen Link handelt.
    * Ein Dollarzeichen ($) zeigt an, dass es sich um eine Datei handelt, die ein End-of-Line-Zeichen enthält und als Textdatei betrachtet werden kann. 

<br>

* **ls -lt** : Listet Dateien und Verzeichnisse im aktuellen Verzeichnis nach dem Zeitpunkt ihrer letzten Änderung auf wobei die zuletzt geänderten Dateien oben angezeigt werden.

* **ls -lh** : Listet Dateien und Verzeichnisse im aktuellen Verzeichnis auf wobei Informationen über ihre Grösse und lesbarkeit angezeigt werden.

* **ls -lR** : Listet Dateien und Verzeichnisse im aktuellen Verzeichnis sowie alle Unterverzeichnisse in rekursiv auf.<br> --> Alle Verzeichnisse im aktuellen Verzeichniss werden ebenfalls geöffnet.

* **tree** : Erstellt eine hierarchische Baumstruktur der Dateien und Verzeichnisse im angegebenen Verzeichnis oder im aktuellen Verzeichnis.
