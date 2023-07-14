# 🐧 Aufbau von Linux

### Linux Geschichte

**Linux** ist ein **quelloffenes Betriebssystem**, das auf dem **Unix-Betriebssystem** basiert. Es wurde in den frühen 1990er Jahren von **Linus Torvalds** entwickelt. Torvalds, ein finnischer Informatiker, begann mit der Entwicklung von Linux im Jahr 1991 als persönliches Projekt, um ein Betriebssystem zu schaffen, das seinen eigenen Anforderungen entsprach.

Der Name **"Linux"** setzt sich aus dem Namen **"Linus"** und **"Unix"** zusammen. Torvalds hat den Linux-Kernel entwickelt, der das Herzstück des Betriebssystems bildet. Der **Linux-Kernel** ist das Fundament, auf dem verschiedene Linux-Distributionen aufbauen.

Eine Linux-Distribution ist eine Zusammenstellung von Softwarepaketen, die den Linux-Kernel mit anderen Anwendungen und Werkzeugen kombinieren, um ein vollständiges Betriebssystem zu schaffen. Es gibt eine Vielzahl von Linux-Distributionen, darunter bekannte Namen wie **Ubuntu**, **Fedora**, **Debian** und **CentOS**. Jede Distribution kann ihre eigenen Eigenschaften, Paketverwaltungssysteme und Benutzeroberflächen haben.

Das Linux-Betriebssystem hat sich im Laufe der Jahre zu einer wichtigen Plattform für Server, Desktop-Computer, Mobilgeräte und eingebettete Systeme entwickelt. Es ist für seine Stabilität, Sicherheit und Flexibilität bekannt. Linux wird in verschiedenen Bereichen eingesetzt, darunter Webserver, Supercomputer, Smartphones und IoT-Geräte.

Ein bekanntes Symbol für Linux ist das Maskottchen **Tux**, ein **Pinguin**. Tux wurde von **Larry Ewing** entworfen und repräsentiert die Open-Source-Natur von Linux. Tux ist zu einem erkennbaren Symbol für das Betriebssystem geworden und wird oft mit Linux in Verbindung gebracht.

Die Entwicklung von Linux erfolgt in einer **offenen** und **kollaborativen** Art und Weise. Tausende von Entwicklern auf der ganzen Welt tragen zur Weiterentwicklung des Linux-Kernels und anderer Komponenten bei. Das Open-Source-Modell von Linux hat zu einer lebendigen und engagierten Gemeinschaft geführt, die sich für die Freiheit, Flexibilität und Zusammenarbeit einsetzt.

Insgesamt hat Linux eine bemerkenswerte Erfolgsgeschichte geschrieben und ist zu einem der **wichtigsten Betriebssysteme** der heutigen Zeit geworden. Es hat eine große Anzahl von Anwendern, Entwicklern und Unternehmen angezogen, die von den Vorteilen eines offenen und **frei zugänglichen** Betriebssystems profitieren.

### Aufbau von Linux

Linux-Systeme bestehen aus **drei Hauptkomponenten**, die beim Booten und Betrieb des Systems eine entscheidende Rolle spielen: dem **Bootloader**, dem **Linux-Kernel** und dem **Root-Dateisystem**.

Der **Bootloader** ist die **erste Software**, die beim Starten des Computers ausgeführt wird. Seine Hauptaufgabe besteht darin, die **Hardware** des Systems zu **initialisieren** und den Linux-Kernel zu laden. Es gibt verschiedene Bootloader, die für Linux verwendet werden können, darunter **GRUB** (GRand Unified Bootloader) und **LILO** (Linux Loader). Der Bootloader befindet sich normalerweise im sogenannten Master Boot Record (MBR) auf der Festplatte oder im Bootsektor einer Partition. Beim Starten des Computers lädt der Bootloader den Linux-Kernel in den Arbeitsspeicher (RAM) und übergibt ihm Informationen über die Hardware und Konfiguration des Systems.

Der **Linux-Kernel** ist das Herzstück des Betriebssystems. Er ist verantwortlich für die **Verwaltung der Hardware-Ressourcen**, die Ausführung von Prozessen und die Bereitstellung von Systemdiensten. Der Kernel ist in **C** geschrieben und besteht aus verschiedenen Modulen, die die verschiedenen Subsysteme des Betriebssystems verwalten, wie beispielsweise das **Dateisystem**, die **Netzwerkfunktionen** und die **Gerätetreiber**. Beim Booten erhält der Kernel Informationen vom Bootloader über die Hardware und die Startparameter. Basierend auf diesen Informationen initialisiert der Kernel die Hardware, konfiguriert die Gerätetreiber und startet das Root-Dateisystem.

Das **Root-Dateisystem** ist der Teil des Dateisystems, der beim Systemstart als **erstes eingehängt** wird. Es enthält die Basisverzeichnisse und Dateien, die für den Betrieb des Systems erforderlich sind. Das Root-Dateisystem wird normalerweise auf einer **separaten Partition** auf der Festplatte gespeichert. Nachdem der Kernel gestartet wurde, wird das Root-Dateisystem eingehängt und bildet den Ausgangspunkt für das Dateisystem des gesamten Systems. Von hier aus werden alle weiteren Dateisysteme und Verzeichnisse eingehängt, die im Laufe des Betriebs benötigt werden.

Zusammen bilden der **Bootloader**, der **Linux-Kernel** und das **Root-Dateisystem** die Grundlage für den Betrieb eines Linux-Systems. Durch die enge Zusammenarbeit dieser Komponenten ermöglicht Linux ein **stabiles, flexibles und effizientes Betriebssystem**, das auf einer Vielzahl von Hardwareplattformen eingesetzt werden kann. Die Trennung von Bootloader, Kernel und Dateisystem ermöglicht es, das System anzupassen, zu aktualisieren und zu erweitern, ohne das gesamte System neu installieren zu müssen.
