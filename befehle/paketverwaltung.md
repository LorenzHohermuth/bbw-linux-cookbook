# Paketverwaltung

## Übersicht

- [Einleitung](#einleitung)
- [Fortgeschrittenes Packaging Tool - APT](#fortgeschrittenes-packaging-tool---apt)
- [Paket installieren](#paket-installieren)
- [Paket entfernen](#paket-entfernen)
- [Aktualisieren des Paketindexes](#aktualisieren-des-paketindexes)
- [Paket-Upgrades](#paket-upgrades)

## Einleitung

Ubuntu's Paketverwaltungssystem stammt aus demselben System, das von der Debian GNU/Linux-Distribution verwendet wird. Die Paketdateien enthalten alle erforderlichen Dateien, Metadaten und Anweisungen, um eine bestimmte Funktionalität oder Softwareanwendung auf Ihrem Ubuntu-Computer zu implementieren.

## Fortgeschrittenes Packaging Tool - APT

Das apt-Kommando ist ein leistungsstolles Befehlszeilentool, das mit Ubuntus Advanced Packaging Tool (APT) zusammenarbeitet. Die Befehle in apt bieten die Möglichkeit, neue Softwarepakete zu installieren, vorhandene Softwarepakete zu aktualisieren, den Paketlistenindex zu aktualisieren und sogar das gesamte Ubuntu-System zu aktualisieren.

## Paket installieren

Die Installation von Paketen mit apt ist recht einfach. Um beispielsweise den Netzwerkscanner nmap zu installieren, geben Sie folgendes ein:

```shell
sudo apt install nmap
```

**Tipp**

Sie können mehrere Pakete angeben, die installiert oder entfernt werden sollen, indem Sie sie mit Leerzeichen trennen.

## Paket entfernen

Das Entfernen eines Pakets (oder mehrerer Pakete) ist ebenfalls unkompliziert. Um das im vorherigen Beispiel installierte Paket zu entfernen, geben Sie einfach Folgendes ein:

```shell
sudo apt remove nmap
```

Durch das Hinzufügen der Option --purge zu apt remove werden auch die Konfigurationsdateien des Pakets entfernt. Dies kann oder kann nicht die gewünschte Wirkung haben, also verwenden Sie es mit Vorsicht.

## Aktualisieren des Paketindexes

Der APT-Paketindex ist im Wesentlichen eine Datenbank der verfügbaren Pakete aus den in der Datei /etc/apt/sources.list und im Verzeichnis /etc/apt/sources.list.d definierten Repositorys. Um den lokalen Paketindex mit den neuesten Änderungen in den Repositorys zu aktualisieren, geben Sie Folgendes ein:

```shell
sudo apt update
```

## Paket-Upgrades

Installierte Pakete auf Ihrem Computer können periodisch Upgrades aus den Paket-Repositories erhalten (z. B. Sicherheitsupdates). Um Ihr System zu aktualisieren, aktualisieren Sie zuerst Ihren Paketindex mit sudo apt update und geben Sie dann Folgendes ein:

```shell
sudo apt upgrade
```