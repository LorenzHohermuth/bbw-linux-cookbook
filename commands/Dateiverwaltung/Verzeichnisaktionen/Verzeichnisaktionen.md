# Dateien oder Verzeichnisse - Erstellen, Kopieren und Entfernen

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

