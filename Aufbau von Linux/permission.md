# Benutzer- und Gruppenverwaltung in Linux

In Linux werden Benutzer und Gruppen verwendet, um den Zugriff auf Ressourcen zu verwalten. Benutzer haben eindeutige Kennungen, während Gruppen Benutzer mit ähnlichen Rechten organisieren. Berechtigungen (Lesen, Schreiben, Ausführen) werden auf Dateien und Verzeichnisse angewendet.

## Benutzerverwaltung

- Jeder Benutzer hat eine eindeutige Benutzerkennung (User ID oder UID) und einen Benutzernamen. Die Benutzerinformationen werden in der Datei `/etc/passwd` gespeichert.
- `useradd` wird verwendet, um einen neuen Benutzer hinzuzufügen.
- `usermod` ändert die Eigenschaften eines Benutzers.
- Mit `userdel` kann ein Benutzer gelöscht werden.
