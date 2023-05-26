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
