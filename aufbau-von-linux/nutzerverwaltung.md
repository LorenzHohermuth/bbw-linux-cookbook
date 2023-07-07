# Linux Nutzerverwaltung

Die Linux Nutzerverwaltung ist ein wichtiger Punkt bei der Verwaltung von Benutzerkonten und Zugriffsrechten in einem Linux-basierten Betriebssystem. Sie ermöglicht die effiziente Verwaltung von Benutzern, Gruppen und deren Berechtigungen. 

## Benutzer
Unter Linux können mehrere Benutzerkonten erstellt werden, um verschiedene Benutzer zu identifizieren und ihren Zugriff auf das System zu steuern. Jeder Benutzer erhält eine eindeutige Benutzerkennung (UserID oder UID) und einen Benutzernamen. Die Benutzerkontoinformationen werden in der Datei `/etc/passwd` gespeichert. 

- **Benutzer hinzufügen:**
Um einen neuen Benutzer hinzuzufügen, kann das Befehlszeilenprogramm `adduser` oder `useradd` verwendet werden. Der Befehl `adduser` führt zusätzliche Konfigurationsschritte aus, während `useradd` nur das Benutzerkonto erstellt.

- Beispiel mit zusätzlichen Konfigurationsschritten

```bash
sudo adduser benutzername
```

- Beispiel ohne zusätzliche Konfigurationsschritte

```bash
sudo useradd benutzername
```


Nachdem der Befehl ausgeführt wurde, werden Sie aufgefordert, einen Passwort für den neuen Benutzer festzulegen und optional zusätzliche Informationen wie z.B. Vor- und Nachname einzugeben.

- **Benutzer löschen:**
Um einen Benutzer zu löschen, kann der Befehl `userdel` verwendet werden. Beispiel:

```bash
sudo userdel benutzername
```

Dieser Befehl löscht das Benutzerkonto, entfernt die zugehörigen Dateien aus dem Home-Verzeichnis des Benutzers und entfernt ihn aus den Gruppen, denen er angehört.

## Gruppen
Gruppen in Linux ermöglichen es, Benutzer mit ähnlichen Zugriffsrechten zu organisieren. Jeder Benutzer kann einer oder mehreren Gruppen angehören. Die Gruppeninformationen werden in der Datei `/etc/group` gespeichert.

- **Gruppe erstellen:**
Um eine neue Gruppe zu erstellen, kann der Befehl `groupadd` verwendet werden. Beispiel:

```bash
sudo groupadd gruppe
```

Dieser Befehl erstellt eine neue Gruppe mit dem Namen "gruppe".

- **Gruppe löschen:**
Um eine Gruppe zu löschen, kann der Befehl `groupdel` verwendet werden. Beispiel:

```bash
sudo groupdel gruppe
```

Dieser Befehl löscht die Gruppe "gruppe".

## Berechtigungen
Die Linux Nutzerverwaltung ermöglicht es, Zugriffsrechte auf Dateien und Verzeichnisse zu verwalten. Jede Datei und jedes Verzeichnis hat Eigentümer und Gruppenberechtigungen sowie Berechtigungen für andere Benutzer.

- **Zugriffsrechte ändern:**
Um die Zugriffsrechte einer Datei oder eines Verzeichnisses zu ändern, kann der Befehl `chmod` verwendet werden. Beispiel:

```bash
chmod u+rwx dateiname
``` 

Dieser Befehl gewährt dem Eigentümer (user, `u`) Lese-, Schreib- und Ausführungsrechte (`rwx`) für die Datei "dateiname". Weitere Optionen sind `g` für die Gruppe und `o` für andere Benutzer.


## Benutzer- und Gruppenattribute ändern mit `usermod` und `groupmod`

Die Befehle `usermod` und `groupmod` ermöglichen die Modifikation von Benutzer- und Gruppenattributen in einem Linux-Betriebssystem. Diese Befehle bieten eine flexible Möglichkeit, vorhandene Benutzer- und Gruppeninformationen anzupassen, ohne die Konten zu löschen und neu zu erstellen.

- **usermod:**
Der Befehl `usermod` ermöglicht die Änderung verschiedener Benutzerattribute wie Benutzername, Benutzer-ID, Gruppenzugehörigkeit und Heimatverzeichnis. Beispiel:

```bash
sudo usermod -l neuerbenutzername alterbenutzername
```

Dieser Befehl ändert den Benutzernamen des Benutzers von "alterbenutzername" in "neuerbenutzername". Weitere Optionen können verwendet werden, um andere Attribute zu ändern.

- **groupmod:**
Der Befehl `groupmod` ermöglicht die Änderung von Gruppenattributen wie Gruppenname und Gruppen-ID. Beispiel:

```bash
sudo groupmod -n neuergruppenname altergruppenname
```

Dieser Befehl ändert den Gruppennamen von "altergruppenname" in "neuergruppenname". Weitere Optionen können verwendet werden, um andere Attribute zu ändern.

## Passwortänderung mit `passwd`

Der Befehl `passwd` ermöglicht die Änderung des Passworts eines Benutzers in einem Linux-System. Jeder Benutzer kann sein eigenes Passwort ändern, und ein Administrator kann das Passwort eines anderen Benutzers ändern.

- **Passwort ändern:**
Um das Passwort für einen Benutzer zu ändern, kann der Befehl `passwd` verwendet werden. Beispiel:

```bash
passwd benutzername
```

Nach der Eingabe des Befehls werden Sie aufgefordert, das neue Passwort zweimal einzugeben. Beachten Sie, dass beim Eingeben des Passworts keine Zeichen angezeigt werden.

## Rekursive Änderung von Zugriffsrechten mit `chmod` und `-R`

Der Befehl `chmod` ermöglicht die Änderung von Zugriffsrechten für Dateien und Verzeichnisse in einem Linux-System. Durch die Verwendung des Parameters `-R` können die Änderungen rekursiv auf Unterverzeichnisse und Dateien angewendet werden.

- **Rekursive Änderung von Zugriffsrechten:**
Um die Zugriffsrechte eines Verzeichnisses und aller darin enthaltenen Dateien und Unterverzeichnisse rekursiv zu ändern, verwenden Sie den Befehl `chmod` mit dem Parameter `-R`. Beispiel:

```bash
chmod -R <zugriffsrechte> verzeichnisname
```
    
Ersetzen Sie `<zugriffsrechte>` durch die gewünschten Zugriffsrechte und `verzeichnisname` durch den Namen des Verzeichnisses, für das die Änderungen gelten sollen.

## Verwaltung von Sudo-Berechtigungen mit `visudo`

Der Befehl `visudo` wird verwendet, um die Konfigurationsdatei `/etc/sudoers` sicher zu bearbeiten. Diese Datei enthält Informationen über die Sudo-Berechtigungen für Benutzer und Gruppen.

- **Bearbeiten der Sudo-Konfigurationsdatei:**
Um die Sudo-Konfigurationsdatei zu bearbeiten, verwenden Sie den Befehl `visudo`. Beispiel:

```bash
sudo visudo
```

Dieser Befehl öffnet die Konfigurationsdatei in einem Texteditor. Sie sollten nur `visudo` verwenden, da dieser Befehl die Datei vor dem Speichern auf Fehler überprüft und so verhindert, dass Sie den Zugriff auf das System verlieren.

In der Sudo-Konfigurationsdatei können Sie Benutzern oder Gruppen Sudo-Berechtigungen erteilen, um bestimmte Aufgaben mit erhöhten Rechten auszuführen. Es ist wichtig, die Syntax der Datei korrekt zu befolgen, da Fehler zu Problemen beim Ausführen von Sudo-Befehlen führen können.

## Verwaltung des Kontingents für den Benutzer

Der Befehl `edquota` wird verwendet, um das Speicherkontingent für Benutzer in Linux zu bearbeiten. Mit diesem Befehl können Administratoren die maximale Speichernutzung für einzelne Benutzer festlegen und verwalten. Es ermöglicht die Festlegung von Soft- und Hard-Limits sowie die Überwachung von Kontingentüberschreitungen. Der Befehl öffnet einen Texteditor, in dem die Kontingentwerte bearbeitet werden können. es werden administrative Rechte benötigt, um `edquota` auszuführen.

## Kürzelsammlung

- **Kürzel mit Erklärungen**

- `-l`: Ändert den Benutzernamen eines bestehenden Benutzers. Zum Beispiel: `usermod -l neuerbenutzername alterbenutzername`.

- `-n`: Ändert den Gruppennamen einer vorhandenen Gruppe. Zum Beispiel: `groupmod -n neuergruppenname altergruppenname`.

- `-u`: Ändert die Benutzer-ID (UID) eines Benutzers. Zum Beispiel: `usermod -u neue_uid benutzername`.

- `-g`: Ändert die primäre Gruppenzugehörigkeit eines Benutzers. Beispiel: `usermod -g neueprimärguppenname benutzername`.

- `-aG`: Fügt einen Benutzer zu einer zusätzlichen Gruppe hinzu. Beispiel: `usermod -aG zusätzlichegruppe benutzername`.

- `-d`: Ändert das Heimatverzeichnis eines Benutzers. Zum Beispiel: `usermod -d /neuesverzeichnis benutzername`.

- `-p`: Setzt das Passwort eines Benutzers. Zum Beispiel: `passwd benutzername`.

- `-R`: Wendet rekursiv Änderungen auf Unterverzeichnisse und Dateien an. Wird oft in Kombination mit `chmod` verwendet. Zum Beispiel: `chmod -R <zugriffsrechte>` verzeichnisname.

- `-C`: Legt das Kontingent für den Benutzer fest, d.h. die maximale Größe des Home-Verzeichnisses. Zum Beispiel: `edquota -u benutzername`.

- `-s`: Ändert die Standard-Shell für einen Benutzer. Zum Beispiel: `usermod -s /bin/bash benutzername`.

- `-i`: Ändert den Kommentar oder die Beschreibung eines Benutzers. Zum Beispiel: `usermod -c "Neuer Kommentar" benutzername`.

Diese Kürzel und Optionen können je nach Linux-Distribution und Version variieren. Es wird empfohlen, die entsprechende Dokumentation oder die Hilfe der einzelnen Befehle zu konsultieren, um spezifische Informationen zu erhalten.

## Zusammenfassung Nutzerverwaltung

Die Linux Nutzerverwaltung bietet die Möglichkeit, Benutzerkonten, Gruppen und Zugriffsrechte effizient zu verwalten. Benutzer können hinzugefügt, gelöscht und verwaltet werden. Gruppen ermöglichen eine einfache Organisation von Benutzern mit ähnlichen Zugriffsrechten. Durch die Verwendung von Zugriffsrechten können Dateien und Verzeichnisse geschützt und der Zugriff auf sie gesteuert werden. Eine solide Kenntnis der Linux Nutzerverwaltung ist für Systemadministratoren und Benutzer wichtig, um ein sicheres und effizientes Betriebssystem zu gewährleisten.