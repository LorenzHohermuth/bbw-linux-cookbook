# Dateistruktur von Linux:

Die Dateistruktur von Linux folgt einem hierarchischen System, das als "Filesystem Hierarchy Standard" (FHS) bezeichnet wird. Hier ist eine grobe Übersicht über die wichtigsten Verzeichnisse:

## bin:

**/bin**: Enthält ausführbare Binärdateien (Programme), die für den Betrieb des Systems erforderlich sind. Hier finden sich grundlegende Befehle wie `ls`, `cp` und `mv`.

## boot:

**/boot**: Beinhaltet die Dateien, die für den Bootvorgang des Systems benötigt werden, einschließlich des Bootloaders und des Linux-Kernels.

## dev:

**/dev**: Enthält Gerätedateien für verschiedene Hardwarekomponenten und Peripheriegeräte wie Festplatten, USB-Geräte, Tastaturen usw.

## etc:

**/etc**: Enthält Konfigurationsdateien für das System und verschiedene Programme. Hier werden beispielsweise die Dateien `/etc/passwd` (Benutzerkonten) und `/etc/apt` (APT-Konfiguration) gespeichert.

## home:

**/home**: Dies ist das Hauptverzeichnis für Benutzer. Jeder Benutzer hat normalerweise ein eigenes Unterverzeichnis hier, in dem persönliche Dateien und Einstellungen gespeichert werden.

## lib:

**/lib** und **/lib64**: Hier befinden sich Bibliotheksdateien (Shared Libraries), die von Programmen während der Laufzeit verwendet werden.

## media:

**/media**: Normalerweise ein Mountpunkt für wechselbare Medien wie USB-Sticks oder externe Festplatten.

## opt:

**/opt**: Hier werden zusätzliche Softwarepakete von Drittanbietern installiert.

## root:

**/root**: Das Heimatverzeichnis des Administrators (root). Es enthält die persönlichen Dateien und Konfigurationen des Administrators.

## sbin:

**/sbin**: Ähnlich wie `/bin`, enthält aber Binärdateien, die nur vom Administrator (root) ausgeführt werden dürfen. Hier befinden sich grundlegende Systembefehle wie `shutdown` und `ifconfig`.

## tmp:

**/tmp**: Ein temporäres Verzeichnis, in dem Programme temporäre Dateien ablegen können. Der Inhalt wird normalerweise beim Neust

> ℹ️ Es gibt natürlich weiter Verzeichnisse das sind die wichtigsten und die, die am meisten verwendet werden.
