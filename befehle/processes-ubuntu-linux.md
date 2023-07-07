# Prozessmanagement Ubuntu Linux

## Übersicht

- [Einleitung](#einleitung)
- [Auflisten und Verwalten von Prozessen mit dem System-Monitor](#auflisten-und-verwalten-von-prozessen-mit-dem-system-monitor)
- [Das Töten eines Prozesses mit "kill" und "killall"](#das-töten-eines-prozesses-mit-kill-und-killall)
- [Verwendung des Befehls "kill" zum Senden eines Signals an einen Prozess anhand der PID](#verwendung-des-befehls-kill-zum-senden-eines-signals-an-einen-prozess-anhand-der-pid)
- [Verwendung des Befehls "killall" zum Senden eines Signals an einen Prozess anhand des Namens](#verwendung-des-befehls-killall-zum-senden-eines-signals-an-einen-prozess-anhand-des-namens)

## Einleitung

Das Verwalten von Prozessen in Linux ist ein wichtiges Thema, das es zu erlernen und zu verstehen gilt, da es sich um ein Multitasking-Betriebssystem handelt und viele Prozesse gleichzeitig ablaufen. Linux bietet zahlreiche Tools zur Verwaltung von Prozessen, wie beispielsweise die Auflistung laufender Prozesse, das Beenden von Prozessen, die Überwachung der Systemnutzung usw. In Linux wird jeder Prozess durch seine Prozess-ID (PID) repräsentiert. Es gibt einige weitere Attribute des Prozesses, wie die Benutzer-ID und die Gruppen-ID, wenn ein Benutzer oder eine Gruppe den Prozess ausführt. Manchmal müssen Sie einen Prozess beenden oder mit ihm interagieren, daher sollten Sie wissen, wie Sie diese Prozesse verwalten können, um Ihr System reibungslos zu betreiben.

## Auflisten und Verwalten von Prozessen mit dem System-Monitor

Linux verfügt über einen Systemmonitor namens GNOME, der die laufenden Prozesse dynamisch anzeigt. Um den Systemmonitor zu starten, drücken Sie die Windows-Taste und geben Sie "Systemmonitor" ein. Klicken Sie dann auf das entsprechende Symbol, um ihn zu öffnen. Dort können Sie die Prozesse in Spalten anzeigen.
Durch einen Rechtsklick auf die Prozesse können Sie diese beenden, anhalten oder die Prozesspriorität (renice) ändern.

![System Monitor](pul-system_monitor.webp)

Die laufenden Prozesse werden mit den Benutzerkonten in alphabetischer Reihenfolge angezeigt. Sie können die Prozesse nach beliebigen Spaltenüberschriften wie CPU, Speicher usw. sortieren. Klicken Sie einfach auf die entsprechende Überschrift, und die Prozesse werden sortiert. Wenn Sie beispielsweise auf "CPU" klicken, können Sie sehen, welcher Prozess die meiste CPU-Leistung verbraucht. Um Prozesse zu verwalten, klicken Sie mit der rechten Maustaste auf sie und wählen Sie die gewünschte Option aus. Um den Prozess zu verwalten, wählen Sie die folgenden Optionen.

- Eigenschaften(Properties): Zeigt weitere Einstellungen in Bezug auf einen Prozess an.
- Speicherkarten(Memory Maps): Zeigt die System-Speicherkarten an, um zu sehen, welche Bibliotheken und andere Komponenten im Speicher für den Prozess verwendet werden.
- Geöffnete Dateien(Open file): Zeigt an, welche Dateien vom Prozess geöffnet sind.
- Priorität ändern(Change Priority): Zeigt eine Seitenleiste an, über die Sie die Priorität des Prozesses mit Optionen von sehr hoch bis sehr niedrig und benutzerdefiniert ändern können.
- Anhalten(Stop): Pausiert den Prozess, bis Sie wählen, fortzufahren.
- Fortsetzen(Continue): Startet einen pausierten Prozess wieder.
- Beenden(Kill): Beendet einen Prozess sofort erzwungen.

## Das Töten eines Prozesses mit "kill" und "killall"

Die Befehle "kill" und "killall" werden verwendet, um einen laufenden Prozess zu beenden/beenden. Diese Befehle können auch verwendet werden, um einem laufenden Prozess ein gültiges Signal zu senden, wie z.B. einem Prozess mitzuteilen, dass er fortgesetzt, beendet oder Konfigurationsdateien erneut gelesen werden soll, usw. Signale können sowohl durch Zahlen als auch durch Namen angegeben werden. Hier sind einige häufig verwendete Signale:

- SIGTERM (15): Dieses Signal wird verwendet, um einen Prozess ordnungsgemäß zu beenden. Dem Prozess wird die Möglichkeit gegeben, Aufräumarbeiten durchzuführen, bevor er beendet wird.
- SIGKILL (9): Dieses Signal wird verwendet, um einen Prozess sofort und erzwungen zu beenden, ohne ihm die Möglichkeit zu geben, Aufräumarbeiten durchzuführen.
- SIGSTOP (19): Dieses Signal wird verwendet, um einen Prozess anzuhalten. Der Prozess wird vorübergehend angehalten und kann mit dem Signal SIGCONT fortgesetzt werden.
- SIGCONT (18): Dieses Signal wird verwendet, um einen zuvor angehaltenen Prozess fortzusetzen.
- SIGHUP (1): Dieses Signal wird verwendet, um einem Prozess mitzuteilen, dass er seine Konfigurationsdateien erneut lesen soll.

Bitte beachten Sie, dass die Verwendung von "kill" und "killall" sorgfältig erfolgen sollte, da das Beenden von Prozessen irreversible Auswirkungen haben kann.

## Verwendung des Befehls "kill" zum Senden eines Signals an einen Prozess anhand der PID

Der Befehl "kill" in Linux wird verwendet, um Signale an laufende Prozesse zu senden, indem die Prozess-ID (PID) angegeben wird. Hier ist die allgemeine Syntax:

```shell
kill SIGNAL PID
```

- "SIGNAL" steht für das gewünschte Signal, das an den Prozess gesendet werden soll. Sie können das Signal entweder numerisch (z. B. 15 für SIGTERM) oder durch seinen Namen (z. B. SIGTERM) angeben.
- "PID" steht für die Prozess-ID des Ziels, an den das Signal gesendet werden soll.

Ein Beispiel für die Verwendung des Befehls "kill", um ein Signal an einen Prozess anhand der PID zu senden:

```shell
kill -SIGTERM 1234
```

Dieser Befehl sendet das Signal SIGTERM an den Prozess mit der PID 1234, um ihn ordnungsgemäß zu beenden. Sie können das Signal und die PID entsprechend Ihren Anforderungen anpassen.

## Verwendung des Befehls "killall" zum Senden eines Signals an einen Prozess anhand des Namens

Mit dem Befehl "killall" müssen Sie nicht nach der Prozess-ID suchen; Sie können ein Kill-Signal an einen Prozess nach seinem Namen statt nach der Prozess-ID senden. Wenn Sie jedoch nicht vorsichtig sind, können mehr Prozesse beendet werden als beabsichtigt. Beispielsweise würde "killall chrome" alle Chrome-Prozesse beenden, einschließlich derjenigen, die Sie nicht beenden möchten. Manchmal ist es nützlich, Prozesse mit demselben Namen zu beenden.

Ähnlich wie beim "kill"-Befehl können Sie beim "killall"-Befehl Signale entweder durch ihren Namen oder ihre Nummer angeben. Sie können jeden laufenden Prozess mit dem "killall"-Befehl beenden, indem Sie nur seinen Namen und das zu sendende Signal angeben. Zum Beispiel können Sie einem Firefox-Prozess ein Kill-Signal mit dem "killall"-Befehl senden, indem Sie den folgenden Befehl eingeben:

```shell
ubuntu@ubuntu:~$ killall -9 firefox
```

oder

```shell
ubuntu@ubuntu:~$ killall SIGKILL chrome
```

Ändern der Prozesspriorität mit "nice" und "renice":

Jeder Prozess auf Ihrem Linux-System hat einen sogenannten "nice"-Wert, der zwischen -19 und 20 liegt. Dieser Wert bestimmt, welcher Prozess im System einen höheren CPU-Zugriff erhält. Je niedriger der Wert des "nice"-Werts ist, desto mehr Zugriff hat ein Prozess auf die CPU-Ressourcen. Beispielsweise hat ein Prozess mit einem "nice"-Wert von -16 mehr Zugriff auf die CPU als ein Prozess mit einem "nice"-Wert von 18. Nur ein Benutzer mit Root-Rechten kann negative "nice"-Werte zuweisen. Ein normaler Benutzer kann nur Werte zwischen 0 und 19 für "nice" zuweisen und nur für seine eigenen Prozesse. Ein Root-Benutzer kann jedem Prozess jeden "nice"-Wert zuweisen.

Wenn Sie einem Prozess einen höheren CPU-Zugriff durch Zuweisen eines "nice"-Werts geben möchten, verwenden Sie den folgenden Befehl:

Und ändern Sie die Prozesspriorität mit dem Befehl "nice":

```shell
ubuntu@ubuntu:~$ nice +3 chrome
```

Und setzen Sie die Priorität des Prozesses mit dem Befehl "renice" neu:

```shell
ubuntu@ubuntu:~$ renice -n -6 3612
```