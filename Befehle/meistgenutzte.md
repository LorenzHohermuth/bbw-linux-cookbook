# Meistgenutzte

- [1. `ls`: Verzeichnisinhalt auflisten.](#1-ls-verzeichnisinhalt-auflisten)
- [2. `cd`: Verzeichnis wechseln.](#2-cd-verzeichnis-wechseln)
- [3. `pwd`: Aktuelles Verzeichnis anzeigen.](#3-pwd-aktuelles-verzeichnis-anzeigen)
- [4. `mkdir`: Verzeichnis erstellen.](#4-mkdir-verzeichnis-erstellen)
- [5. `rm`: Dateien oder Verzeichnisse entfernen.](#5-rm-dateien-oder-verzeichnisse-entfernen)
- [6. `cp`: Dateien und Verzeichnisse kopieren.](#6-cp-dateien-und-verzeichnisse-kopieren)
- [7. `mv`: Dateien und Verzeichnisse verschieben oder umbenennen.](#7-mv-dateien-und-verzeichnisse-verschieben-oder-umbenennen)
- [8. `touch`: Leere Datei erstellen.](#8-touch-leere-datei-erstellen)
- [9. `cat`: Dateiinhalt anzeigen und zusammenführen.](#9-cat-dateiinhalt-anzeigen-und-zusammenführen)
- [10. `grep`: Nach Mustern in Dateien suchen.](#10-grep-nach-mustern-in-dateien-suchen)
- [11. `chmod`: Dateiberechtigungen ändern.](#11-chmod-dateiberechtigungen-ändern)
- [12. `chown`: Dateibesitz ändern.](#12-chown-dateibesitz-ändern)
- [13. `sudo`: Befehl als Superuser (root) ausführen.](#13-sudo-befehl-als-superuser-root-ausführen)
- [14. `apt-get` oder `apt`: Paketverwaltungsbefehl für Debian-basierte Systeme.](#14-apt-get-oder-apt-paketverwaltungsbefehl-für-debian-basierte-systeme)
- [15. `yum`: Paketverwaltungsbefehl für RPM-basierte Systeme.](#15-yum-paketverwaltungsbefehl-für-rpm-basierte-systeme)
- [16. `ssh`: Secure Shell-Client für entfernte Anmeldung.](#16-ssh-secure-shell-client-für-entfernte-anmeldung)
- [17. `wget`: Dateien aus dem Web herunterladen.](#17-wget-dateien-aus-dem-web-herunterladen)
- [18. `top`: Systemressourcennutzung anzeigen.](#18-top-systemressourcennutzung-anzeigen)
- [19. `ps`: Ausgeführte Prozesse auflisten.](#19-ps-ausgeführte-prozesse-auflisten)
- [20. `kill`: Einen Prozess beenden.](#20-kill-einen-prozess-beenden)
- [21. `find`: Nach Dateien und Verzeichnissen suchen.](#21-find-nach-dateien-und-verzeichnissen-suchen)
- [22. `history`: Befehlsverlauf anzeigen.](#22-history-befehlsverlauf-anzeigen)
- [23. `su`: Benutzer wechseln.](#23-su-benutzer-wechseln)

> Zunächst einmal möchte ich erwähnen, dass Sie alle OPTIONEN und Hilfe mit Befehl `-h` oder Befehl `--help` anzeigen können. Ersetzen Sie natürlich den Befehl durch beispielsweise ls: `ls --help`.

## 1. `ls`: Verzeichnisinhalt auflisten.

- Beschreibung: Zeigt den Inhalt eines Verzeichnisses an.
- Syntax: `ls [OPTIONEN] [VERZEICHNIS]`
- Beispiel: `ls -l` zeigt den Inhalt des aktuellen Verzeichnisses mit detaillierten Informationen an.

## 2. `cd`: Verzeichnis wechseln.

- Beschreibung: Wechselt das aktuelle Verzeichnis.
- Syntax: `cd [VERZEICHNIS]`
- Beispiel: `cd /pfad/zum/verzeichnis` wechselt zum angegebenen Verzeichnis.

## 3. `pwd`: Aktuelles Verzeichnis anzeigen.

- Beschreibung: Zeigt den Pfad des aktuellen Arbeitsverzeichnisses an.
- Syntax: `pwd`
- Beispiel: `pwd` /bbw-linux-cookbook - hier sehen Sie Ihr aktuelles Arbeitsverzeichnis

## 4. `mkdir`: Verzeichnis erstellen.

- Beschreibung: Erstellt ein neues Verzeichnis.
- Syntax: `mkdir [OPTIONEN] VERZEICHNIS`
- Beispiel: `mkdir neues_verzeichnis` erstellt ein neues Verzeichnis mit dem Namen "neues_verzeichnis"

## 5. `rm`: Dateien oder Verzeichnisse entfernen.

- Beschreibung: Entfernt Dateien oder Verzeichnisse.
- Syntax: `rm [OPTIONEN] DATEI`
- Beispiel: `rm datei.txt` entfernt die Datei mit dem Namen "datei.txt"

## 6. `cp`: Dateien und Verzeichnisse kopieren.

- Beschreibung: Kopiert Dateien und Verzeichnisse.
- Syntax: `cp [OPTIONEN] QUELLE ZIEL`
- Beispiel: `cp datei.txt /pfad/zum/ziel` kopiert "datei.txt" zum angegebenen Ziel

## 7. `mv`: Dateien und Verzeichnisse verschieben oder umbenennen.

- Beschreibung: Verschiebt oder benennt Dateien und Verzeichnisse um.
- Syntax: `mv [OPTIONEN] QUELLE ZIEL`
- Beispiel: `mv datei.txt /pfad/zum/ziel` verschiebt "datei.txt" zum angegebenen Ziel

## 8. `touch`: Leere Datei erstellen.

- Beschreibung: Erstellt eine leere Datei.
- Syntax: `touch [OPTIONEN] DATEI`
- Beispiel: `touch datei.txt` erstellt eine leere Datei mit dem Namen "datei.txt"

## 9. `cat`: Dateiinhalt anzeigen und zusammenführen.

- Beschreibung: Zeigt den Inhalt einer oder mehrerer Dateien an und führt sie zusammen.
- Syntax: `cat [OPTIONEN] DATEI`
- Beispiel: `cat datei.txt` zeigt den Inhalt von "datei.txt" an

## 10. `grep`: Nach Mustern in Dateien suchen.

- Beschreibung: Sucht nach Mustern in Dateien.
- Syntax: `grep [OPTIONEN] MUSTER DATEI`
- Beispiel: `grep "suchbegriff" datei.txt` sucht nach dem angegebenen Muster in "datei.txt"

## 11. `chmod`: Dateiberechtigungen ändern.

- Beschreibung: Ändert die Berechtigungen einer Datei.
- Syntax: `chmod [OPTIONEN] MODUS DATEI`
- Beispiel: `chmod +x skript.sh` gibt der Datei "skript.sh" Ausführungsrechte

## 12. `chown`: Dateibesitz ändern.

- Beschreibung: Ändert den Besitz einer Datei.
- Syntax: `chown [OPTIONEN] BENUTZER DATEI`
- Beispiel: `chown benutzer datei.txt` ändert den Besitz der Datei "datei.txt" auf den angegebenen Benutzer

## 13. `sudo`: Befehl als Superuser (root) ausführen.

- Beschreibung: Führt einen Befehl als Superuser (root) aus.
- Syntax: `sudo Befehl`
- Beispiel: `sudo apt-get update` führt den Befehl "apt-get update" als Superuser aus

## 14. `apt-get` oder `apt`: Paketverwaltungsbefehl für Debian-basierte Systeme.

- Beschreibung: Verwaltet Pakete auf Debian-basierten Systemen.
- Syntax: `apt-get [OPTIONEN] BEFEHL`
- Beispiel: `apt-get install paketname` installiert das angegebene Paket

## 15. `yum`: Paketverwaltungsbefehl für RPM-basierte Systeme.

- Beschreibung: Verwaltet Pakete auf RPM-basierten Systemen.
- Syntax: `yum [OPTIONEN] BEFEHL`
- Beispiel: `yum install paketname` installiert das angegebene Paket

## 16. `ssh`: Secure Shell-Client für entfernte Anmeldung.

- Beschreibung: Stellt eine sichere Verbindung zu einem entfernten Host her.
- Syntax: `ssh [OPTIONEN] BENUTZER@HOST`
- Beispiel: `ssh benutzer@beispiel.com` stellt eine Verbindung zu "beispiel.com" her

## 17. `wget`: Dateien aus dem Web herunterladen.

- Beschreibung: Lädt Dateien aus dem Web herunter.
- Syntax: `wget [OPTIONEN] URL`
- Beispiel: `wget https://beispiel.com/datei.txt` lädt die Datei "datei.txt" von der angegebenen URL herunter

## 18. `top`: Systemressourcennutzung anzeigen.

- Beschreibung: Zeigt Informationen zur Systemressourcennutzung an.
- Syntax: `top`
- Beispiel: `top` zeigt Echtzeitinformationen zu Prozessen und Ressourcennutzung an

## 19. `ps`: Ausgeführte Prozesse auflisten.

- Beschreibung: Zeigt Informationen zu laufenden Prozessen an.
- Syntax: `ps [OPTIONEN]`
- Beispiel: `ps aux` zeigt eine Liste aller Prozesse im Detail an

## 20. `kill`: Einen Prozess beenden.

- Beschreibung: Beendet einen laufenden Prozess.
- Syntax: `kill [OPTIONEN] PID`
- Beispiel: `kill 1234` beendet den Prozess mit der angegebenen PID

## 21. `find`: Nach Dateien und Verzeichnissen suchen.

- Beschreibung: Sucht nach Dateien und Verzeichnissen basierend auf bestimmten Kriterien.
- Syntax: `find [VERZEICHNIS] [OPTIONEN] [AUSDRUCK]`
- Beispiel: `find /pfad/zum/verzeichnis -name "*.txt"` sucht nach allen Dateien mit der Erweiterung ".txt" im angegebenen Verzeichnis

## 22. `history`: Befehlsverlauf anzeigen.

- Beschreibung: Zeigt eine Liste der zuvor ausgeführten Befehle an.
- Syntax: `history [OPTIONEN]`
- Beispiel: `history` zeigt den Befehlsverlauf an

## 23. `su`: Benutzer wechseln.

Beschreibung: Wechselt den aktuellen Benutzer zu einem anderen Benutzer oder zum Superuser (root).
Syntax: `su [OPTIONEN] [BENUTZER]`
Beispiel: `su` `pascal` wechselt zum Benutzer Pascal, während `su` allein zum Superuser (root) wechselt.
