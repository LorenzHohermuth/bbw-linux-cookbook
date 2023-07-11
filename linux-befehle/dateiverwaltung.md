# Dateiverwaltung Linux

Die Dateiverwaltungsbefehle in Linux bieten eine leistungsstarke Reihe von Werkzeugen zum Navigieren, Organisieren und Manipulieren von Dateien und Verzeichnissen im Betriebssystem. Diese Befehle ermöglichen es Benutzern, eine Vielzahl von Operationen durchzuführen, wie das Erstellen, Löschen, Kopieren, Verschieben und Suchen von Dateien und Verzeichnissen.

- [Auflisten von Dateien innerhalb eines Verzeichnisses](#auflisten-von-dateien-innerhalb-eines-verzeichnisses)
- [Dateien oder Verzeichnisse - Erstellen, Kopieren und Entfernen](#dateien-oder-verzeichnisse---erstellen-kopieren-und-entfernen)
- [Befehle zur Verzeichnismanipulation in Linux](#befehle-zur-verzeichnismanipulation-in-linux)
- [Zugriffssteuerung](#zugriffssteuerung)
  - [Liste der Berechtigungssymbole und ihre Bedeutung in Bezug auf den 'chmod'-Befehl](#liste-der-berechtigungssymbole-und-ihre-bedeutung-in-bezug-auf-den-chmod-befehl)

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

## Dateien oder Verzeichnisse - Erstellen, Kopieren und Entfernen

* **cp -p source destination** :Der Befehl kopiert die ausgewählte Datei "example.txt" in ein erwähltes Verzeichnis und erhält dabei alle Attribute der Originaldatei wie Besitzer, Zeitstempel, Gruppe und Berechtigungen.

```
cp -p example.txt destination/
```

* **cp -R source_dir destination_dir** :Der Befehl "cp -R" kopiert das Verzeichnis "source_dir" rekursiv in das angegebene Zielverzeichnis "destination_dir". Dabei werden alle Dateien und Unterverzeichnisse im Quellverzeichnis einschließlich ihrer Verzeichnisstruktur kopiert.

* **mv file1 file2** :Der Befehl "mv file1 file2" verschiebt oder benennt die Datei "file1" in "file2" um --> es kommt darauf an ob man einen Verzeichnisspfad oder Dateinamen angibt.

```
mv file1.txt destination/
```

```
mv oldname.txt newname.txt
```

* **rm -i filename** :Der Befehl "rm -i filename" entfernt eine Datei im Linux-Betriebssystem, fragt jedoch vor jedem Löschvorgang nach Bestätigung des Benutzers und kann mehrere Dateien angeben.

* **rm -R dir-name** :Der Befehl "rm -R dir-name" entfernt das Verzeichnis "dir-name" und alle seine enthaltenen Dateien und Unterverzeichnisse rekursiv im Linux-Betriebssystem.

* **rm -rf dir-name** :Der Befehl "rm -rf dir-name" entfernt das Verzeichnis "dir" und seinen gesamten Inhalt rekursiv im Linux-Betriebssystem, ohne nach Bestätigung zu fragen und ohne Rücksicht auf nicht existierende Dateien.

* **rmdir dir-name** :Der Befehl "rmdir dir-name" entfernt das Verzeichnis "dir-name", wenn es leer ist. Dieser Befehl kann nur leere Verzeichnisse entfernen und funktioniert nicht, wenn das Verzeichnis Dateien oder Unterverzeichnisse enthält.

* **mkdir dir-name**:Der Befehl "mkdir dir-name" erstellt ein Verzeichnis mit dem Namen "dir-name" im aktuellen Verzeichnis im Linux-Betriebssystem.

* **mkdir -p dir-name/dir-name** :Der Befehl "mkdir -p dir-name/dir-name" erstellt eine Verzeichnisstruktur, einschließlich der Elternverzeichnisse, falls sie nicht existieren. Es können mehrere Verzeichnisse angegeben werden.

* **touch filename** :Der Befehl "touch filename" erstellt eine Datei mit dem Namen "filename", wenn sie nicht existiert. Falls die Datei bereits existiert, wird der Zeitstempel der Datei auf die aktuelle Zeit geändert.

## Befehle zur Verzeichnismanipulation in Linux

* **pwd** : Zeigt den vollständigen Pfad zum aktuellen Arbeitsverzeichnis an.
* **cd -** : Navigiert zum zuletzt verwendeten Verzeichnis.
* **cd ~** : Navigiert zum Home-Verzeichnis des aktuellen Benutzers.
* **cd ..** : Geht zum übergeordneten Verzeichnis des aktuellen Verzeichnisses.

## Zugriffssteuerung

### Liste der Berechtigungssymbole und ihre Bedeutung in Bezug auf den 'chmod'-Befehl
<br>

1. u - Benutzer (user): Der Besitzer der Datei oder des Verzeichnisses.
2. g - Gruppe (group): Die Gruppe, der die Datei oder das Verzeichnis zugeordnet ist.
3. o - Andere (others): Alle anderen Benutzer, die nicht der Besitzer sind und nicht zur Gruppe gehören.
4. &#43; - Hinzufügen (add): Fügt die angegebene Berechtigung hinzu.
5. &#45; - Entfernen (remove): Entfernt die angegebene Berechtigung.
6. r - Lesen (read): Leseberechtigung für die Datei oder das Verzeichnis.
7. w - Schreiben (write): Schreibberechtigung für die Datei oder das Verzeichnis.
8. x - Ausführen (execute): Ausführungsberechtigung für die Datei oder das Verzeichnis.
<br>
<br>
<br>


* **chmod < specification > filename** :Der Befehl "chmod" ändert die Dateiberechtigungen und ermöglicht es, die Zugriffsrechte für den Benutzer (u), die Gruppe (g) und andere (o) zu ändern, indem Berechtigungen hinzugefügt (+) oder entfernt (-) werden, wie z. B. Lesen (r), Schreiben (w) und Ausführen (x).

```
chmod u+x,g+x script.sh
```

* **chmod -R < specification > dir-name** :Der Befehl "chmod -R" ändert rekursiv die Berechtigungen eines Verzeichnisses und aller darin enthaltenen Dateien und Unterverzeichnisse gemäß der angegebenen Spezifikation. Dadurch werden die Zugriffsrechte für das Verzeichnis und alle seine Inhalte gleichzeitig geändert.

```
chmod -R u+rw,g+rw,o+rw my-directory
```

* **chmod go=+r myfile** :Der Befehl "chmod go=+r myfile" fügt dem Eigentümer und der Gruppe die Leseberechtigung hinzu und entfernt die vorherigen Berechtigungen für andere.

```
chmod go+r myfile.txt
```

* **chmod a +rwx myfile** :Der Befehl "chmod a +rwx myfile" gewährt allen Benutzern (Besitzer, Gruppe und andere) Lese-, Schreib- und Ausführungsberechtigungen für die Datei "myfile".

```
chmod a+rwx myfile
```

* **chmod go -r myfile** :Der Befehl "chmod go -r myfile" entfernt die Leseberechtigung (-r) für die Gruppe (g) und andere (o) von der Datei "myfile", während die Berechtigungen für den Eigentümer unverändert bleiben. Dadurch können die Gruppe und andere nicht mehr auf die Datei zugreifen.

```
chmod go-r myfile.txt
```

* **chown owner1 filename** :Der Befehl "chown owner1 filename" ändert den Besitzer (Eigentümer) einer Datei auf den Benutzer "owner1". Dadurch wird die Eigentümerschaft der Datei auf den angegebenen Benutzer übertragen.

```
chown ownerl myfile.txt
```

* **chgrp grp_owner filename** :Der Befehl "chgrp grp_owner filename" ändert die primäre Gruppenzugehörigkeit der Datei "filename" auf die Gruppe "grp_owner". Das bedeutet, dass die angegebene Gruppe zur neuen primären Gruppe für die Datei wird.

```
chgrp grp_owner myfile.txt
```

* **chgrp -R grp_owner dir-name** :Der Befehl "chgrp -R grp_owner dir-name" ändert die primäre Gruppenzugehörigkeit eines Verzeichnisses "dir-name" und aller darin enthaltenen Dateien und Unterverzeichnisse rekursiv auf die Gruppe "grp_owner". Dieser Befehl ermöglicht es, die Gruppenzugehörigkeit eines Verzeichnisses und dessen gesamten Inhalts gleichzeitig zu ändern.

```
chgrp -R grp_owner my-directory
```