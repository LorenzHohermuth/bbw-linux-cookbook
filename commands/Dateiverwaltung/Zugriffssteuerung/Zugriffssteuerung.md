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