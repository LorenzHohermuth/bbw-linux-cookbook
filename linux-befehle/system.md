# 🖱 System

Systembefehle in Linux sind leistungsstarke Werkzeuge zur Verwaltung des Betriebssystems. Sie ermöglichen die Datei- und Verzeichnisverwaltung, Prozesskontrolle, Benutzer- und Gruppenverwaltung, Paketverwaltung, Netzwerkkonfiguration und Systemüberwachung. Mit diesen Befehlen können Benutzer effizient und effektiv Aufgaben automatisieren und komplexe Workflows erstellen.

## Systemressourcenüberwachungsbefehle

* **shutdown** : Der Befehl "shutdown" wird verwendet, um das Betriebssystem herunterzufahren oder neu zu starten, wobei verschiedene Optionen wie der Zeitpunkt des Herunterfahrens oder die Nachricht an Benutzer festgelegt werden können.
* **reboot** : Der Befehl "reboot" wird verwendet, um das Betriebssystem und alle laufenden Prozesse neu zu starten, wodurch der Computer heruntergefahren und anschließend wieder hochgefahren wird.
* **halt** : Der Befehl "halt" wird verwendet, um das Betriebssystem herunterzufahren und den Computer vollständig auszuschalten, indem alle Prozesse beendet werden und die Stromversorgung des Systems abgeschaltet wird.
* **poweroff** :Der Befehl "poweroff" wird verwendet, um das Betriebssystem herunterzufahren und den Computer vollständig auszuschalten, indem alle laufenden Prozesse beendet werden und die Stromversorgung des Systems abgeschaltet wird. Im Gegensatz zum Befehl "halt" wird der Computer nach dem Herunterfahren nicht im Ruhezustand gehalten, sondern vollständig ausgeschaltet.
*   **systemctl** :Der Befehl "systemctl" wird verwendet, um Systemd-Dienste auf Linux-Systemen zu verwalten. Es ermöglicht das Starten, Stoppen, Neustarten, Aktivieren oder Deaktivieren von Diensten, das Anzeigen des Status von Diensten und das Verwalten von Systemeinheiten.

    * Starten eines Dienstes

    ```
        sytemctl start <servicename>
    ```

    * Stoppen eines Dienstes

    ```
    systemctl stop <servicename>
    ```

    * Neustarten eines Dienstes

    ```
    systemctl restart <servicename>
    ```

    * Aktivieren eines Dienstes, damit er beim Systemstart automatisch gestartet wird

    ```
    systemctl enable <servicename>
    ```

    * Deaktivieren eines Dienstes, sodass er beim Systemstart nicht mehr automatisch gestartet wird

    ```
    systemctl disable <servicename>
    ```

    * Anzeigen des Status eines Dienstes

    ```
    systemctl status <servicename>
    ```

\


* **kill** :Der Befehl "kill" wird verwendet, um laufende Prozesse auf einem Linux-System zu beenden. Mit diesem Befehl können Prozesse anhand ihrer Prozess-ID (PID) gezielt beendet oder signale gesendet werden, um bestimmte Aktionen auf den Prozess auszuführen.

## Systemverwaltungsbefehle

* **ps** :Der Befehl "ps" wird verwendet, um Informationen über aktive Prozesse auf einem Linux-System anzuzeigen. Es liefert eine Übersicht über laufende Prozesse, einschließlich ihrer Prozess-IDs (PIDs), Zustände, Ressourcennutzung und weiterer Details.
* **top** :Der Befehl "top" wird verwendet, um Echtzeitinformationen über die Systemressourcen und laufenden Prozesse auf einem Linux-System anzuzeigen. Es zeigt eine interaktive Übersichtstabelle mit CPU-Auslastung, Speichernutzung, Prozessinformationen und anderen Leistungsstatistiken an.
* **df** :Der Befehl "df" wird verwendet, um Informationen über die Speicherplatznutzung von Dateisystemen auf einem Linux-System anzuzeigen. Es zeigt die Größe, die verwendete Menge, die verfügbare Menge und den Dateisystemtyp für jedes gemountete Dateisystem an.
* **du** :Der Befehl "du" wird verwendet, um die Speicherplatznutzung von Dateien und Verzeichnissen auf einem Linux-System zu ermitteln. Es zeigt die Größe von Dateien und Verzeichnissen sowie die Gesamtgröße eines Verzeichnisses und seiner Unterverzeichnisse an.
* **free** :Der Befehl "free" wird verwendet, um Informationen über den Speicher (RAM) und den Swap-Speicher auf einem Linux-System anzuzeigen. Es zeigt den verfügbaren, belegten und freien Speicherplatz sowie Informationen über die Speicherauslastung und Auslagerung an.
