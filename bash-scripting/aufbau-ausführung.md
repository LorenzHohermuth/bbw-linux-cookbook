# 🌳 Aufbau / Ausführung Bash Scripting

## Script erstellen

Um ein Script zu erstellen, reicht ein einfacher Editor wie vi, nano oder gedit. Um z.B. mit nano ein neues Script zu erstellen, kann man den Befehl `nano scriptname.sh` verwenden.

## Aufbau eines Scripts

### Shebang

Der Shebang ist die erste Zeile in einem Script. Es gibt dem System an, mit welcher Shell es aufgeführt werden sollte. Beispiele für verschiedene Shells:

* Bash (Bourne Again Shell)
* Zsh (Z Shell)
* Ksh (Korn Shell)

Der Shebang kann in der Theorie weggelassen werden, sollte man aber nicht machen, da das System sonst dein Script eventuell mit der falschen Shell ausführt. Ein Shebang fängt immer mit `#!` an. Danach kommt der Shell path. Um zum Beispiel die Standart Bash Shell zu verwenden, bräuchte man als erste Zeile im Script diesen Shebang: `#!/bin/bash`.

### Befehle Grundaufbau

Befehle sind in der Regel wie folgt aufgebaut `command [OPTIONS] arguments`. Die options sind freiwillig und können einfach weggelassen werden. Ein einfaches Beispiel von einem Command ohne options: `echo "Hello bash"`.

## Ausführen eines Scripts

Um ein Script auszuführen, ohne Rechte hinzugefügt zu haben, kann man folgende Befehle verwenden.

* `sh script_name.sh`
* `bash script_name.sh`

Um ein Script mit hinzugefügten Rechten auszuführen, kann man diesen Befehl verwenden

* `./script_name.sh`

Um ein Script die Rechte hinzuzufügen braucht man den Befehl `chmod` was für "change mode" steht. Um die Rechte für das Ausführen der Datei zu geben, braucht man die Option `+x`. Und als Letztes der Dateiname. Ein Beispiel: `chmod +x mein_skript.sh`
