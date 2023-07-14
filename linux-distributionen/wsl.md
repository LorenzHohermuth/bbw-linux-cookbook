# 🐧 WSL

## Definition

Insgesamt bietet WSL eine flexible und bequeme Möglichkeit, eine Linux-Umgebung auf einem Windows-System zu nutzen und erleichtert die Interaktion zwischen den beiden Betriebssystemen.

## Installation

* **Installation via Microsoft Store**
* **Installation via CMD/Powershell** Öffnen sie das CMD oder die Powershell mit Administratorrechten. Danach können sie innerhalb mit dem Befehl:

```bash
wsl --install
```

WSL installieren. Dadurch werden die nötigen Features für WSL aktiviert und eine Ubuntu Distribution von Linux installiert.

## Nutzen

Mit WSL können Benutzer eine Vielzahl von Linux-Distributionen, wie Ubuntu, Debian, Fedora und mehr, auf Windows basierenden Computern installieren und ausführen. Diese Distributionen laufen jedoch nicht in einer vollständig separaten Umgebung, sondern teilen sich den Kernel des Windows-Betriebssystems. Dadurch wird eine nahtlose Integration von Linux- und Windows-Anwendungen ermöglicht.

## Vorteile

* **Nahtlose Integration:** Mit WSL können Benutzer Linuxbefehle direkt in der Windows-Eingabeaufforderung(CMD) oder in Powershell ausführen. Ebenfalls können auch Linux-Tools und -Anwendungen direkt auf ihrem Windows-Desktop gestartet werden.
* **Entwicklungsumgebung:** WSL ist besonders für Entwickler nützlich, da damit Linux-basierte Tools und Frameworks verwendet werden können. Mit WSL können sie ihre Entwicklungsumgebung auf ihrem Windows-Computer einrichten und haben Zugriff auf eine umfangreiche Palette an Linux-Tools und -Bibliotheken.
* **Dateisystemintegration:** WSL ermöglicht den Zugriff auf das Windows-Dateisystem von der Linux-Umgebung aus. Dadurch können Benutzer problemlos auf ihre Windows-Dateien zugreifen und mit ihnen arbeiten.
* **Leichtgewichtig:** Im Vergleich zu einer virtuellen Maschine ist WSL ressourcenschonender. Es ermöglicht die Ausführung von Linux-Anwendungen, ohne dass eine vollständige virtuelle Maschine gestartet werden muss.

## WSL 1 vs WSL 2

* **WSL 1:** emuliert den Linux-Kernel auf Windows und bietet eine gute Kompatibilität.
* **WSL 2:** verwendet eine vollständige Linux-Kernel-Virtualisierung und bietet eine verbesserte Leistung und Kompatibilität.
