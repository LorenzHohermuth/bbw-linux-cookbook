# Aufbau / Ausführung

## Aufbau eines Scripts

### Shebang
Der Shebang ist die erste Zeile in einem Script. Es gibt dem System an mit welcher Shell es aufgeführt werden sollte. Beispiele für verschiedene Shells:

1. Bash (Bourne Again Shell)
2. Zsh (Z Shell)
3. Ksh (Korn Shell)

Der Shebang kann in der Theory weggelassen werden, sollte man aber nicht machen, da das System sonst dein Script eventuel mit der falschen Shell ausführt. Ein Shebang fängt immer mit `#!` an. Danach kommt der Shell path. Um zum Beispiel die standart Bash shall zu verwenden bräuchte man als erste Zeile im Script diesen Shebang: `#!/bin/bash`.

### Befehle grund aufbau
Befehle sind in der Regel wie folgt wie folgt aufgebaut `command [OPTIONS] arguments`. Die OPTIONS sind freiwillig und können einfach weg gellassen werden. Ein einfaches Beispiel: `echo "Hello bash"`.

## Script erstellen



## Ausführen
Um ein Script aus zuführen gibt es mehere möglcihkeiten. Dies sind drei mögliche befehle: 

Ausführbar machen chmod +x mein_skript.sh

1. `sh script_name.sh`
2. `bash script_name.sh`
3. `./script_name.sh`