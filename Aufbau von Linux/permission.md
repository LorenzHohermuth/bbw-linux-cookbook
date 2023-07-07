# Benutzer- und Gruppenverwaltung in Linux

In Linux werden Benutzer und Gruppen verwendet, um den Zugriff auf Ressourcen zu verwalten. Benutzer haben eindeutige Kennungen, während Gruppen Benutzer mit ähnlichen Rechten organisieren. Berechtigungen (Lesen, Schreiben, Ausführen) werden auf Dateien und Verzeichnisse angewendet.

## Benutzerverwaltung

- Jeder Benutzer hat eine eindeutige Benutzerkennung (User ID oder UID) und einen Benutzernamen. Die Benutzerinformationen werden in der Datei `/etc/passwd` gespeichert.
- `useradd` wird verwendet, um einen neuen Benutzer hinzuzufügen.
- `usermod` ändert die Eigenschaften eines Benutzers.
- Mit `userdel` kann ein Benutzer gelöscht werden.


## Gruppenverwaltung

- Gruppen organisieren Benutzer mit ähnlichen Rechten. Gruppeninformationen werden in der Datei `/etc/group` gespeichert.
- `groupadd` fügt eine neue Gruppe hinzu.
- `groupmod` ändert Eigenschaften einer Gruppe.
- `groupdel` löscht eine Gruppe.


## Berechtigungen und Zugriffskontrolle

- Dateien und Verzeichnisse haben Besitzer- und Gruppeninformationen.
- Zugriffsrechte werden in drei Kategorien unterteilt: Benutzer, Gruppe und andere.
- Mit `chmod` ändert man die Berechtigungen einer Datei.
- Mit `chown` ändert man den Eigentümer einer Datei.
- Mit `chgrp` ändert man die Gruppenzugehörigkeit einer Datei.

Diese Grundlagen helfen dabei, Benutzer und Gruppen in Linux zu verwalten und Zugriffsrechte auf Ressourcen anzuwenden, um die Sicherheit zu gewährleisten.



# Linux-Befehle zur Berechtigungsverwaltung

*In Linux gibt es mehrere Befehle zur Berechtigungsverwaltung, die dir helfen, die Zugriffsrechte für Dateien und Verzeichnisse zu kontrollieren. Hier sind einige der wichtigsten Befehle und ihre Verwendung:*



1. `chmod` - Kontrolliere die Macht:
   Ändere die Zugriffsrechte von Dateien und Verzeichnissen. Du kannst festlegen, wer lesen (`r`), schreiben (`w`) und ausführen (`x`) darf. Beispiel: `chmod u+rwx datei.txt` gewährt dem Eigentümer volle Rechte auf die Datei "datei.txt".
   
   ```
    $ chmod u=rwx,g=r,o= mein_script.sh
    ```


2. `chown` - Verleihe Besitz:
   Ändere den Eigentümer einer Datei oder eines Verzeichnisses. Du kannst entweder den Eigentümername oder die Benutzerkennung (UserID) verwenden. Beispiel: `chown benutzername datei.txt` ändert den Eigentümer der Datei "datei.txt" in den Benutzer mit dem Namen "benutzername".

   ```
    $ chown benutzer1 mein_text.txt
    ```

3. `chgrp` - Gruppenzuweisung:
   Ändere die Gruppenzugehörigkeit einer Datei oder eines Verzeichnisses. Du kannst entweder den Gruppennamen oder die Gruppenkennung (GroupID) verwenden. Beispiel: `chgrp gruppenname datei.txt` ändert die Gruppe der Datei "datei.txt" in die Gruppe mit dem Namen "gruppenname".

   ```
    $ chgrp gruppe1 mein_verzeichnis
    ```
   
4. `chroot` - Auf ins Gefängnis:
   Ändere das Root-Verzeichnis für einen Prozess und seine Kindprozesse. Dies wird oft verwendet, um eine abgeschottete Umgebung zu erstellen, in der ein Prozess nur auf bestimmte Teile des Dateisystems zugreifen kann.

   ```
    $ sudo chroot /pfad/zum/neuen/verzeichnis bin/bash
    ```  



5. `setfacl` - Erweitere die Kontrolle:
   Verwende erweiterte Zugriffssteuerungslisten (ACLs), um detaillierte Zugriffsrechte für Dateien und Verzeichnisse festzulegen. Mit ACLs kannst du individuelle Zugriffsrechte für bestimmte Benutzer definieren. Beispiel: `setfacl -m u:benutzername:rwx datei.txt` gewährt dem Benutzer "benutzername" volle Rechte auf die Datei "datei.txt".

   ```
    $ setfacl -m:benutzername:rwx datei.txt
    ```
   

**Diese Befehle geben dir die nötigen Werkzeuge, um die Berechtigungen in deinem Linux-System anzupassen. Achte darauf, dass einige Befehle Superuser-Rechte erfordern. Experimentiere und behalte die Kontrolle über deine Dateien und Verzeichnisse!**