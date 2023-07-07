## Systemressourcenüberwachungsbefehle

* **shutdown** : Der Befehl "shutdown" wird verwendet, um das Betriebssystem herunterzufahren oder neu zu starten, wobei verschiedene Optionen wie der Zeitpunkt des Herunterfahrens oder die Nachricht an Benutzer festgelegt werden können.

* **reboot** : Der Befehl "reboot" wird verwendet, um das Betriebssystem und alle laufenden Prozesse neu zu starten, wodurch der Computer heruntergefahren und anschließend wieder hochgefahren wird.

* **halt** : Der Befehl "halt" wird verwendet, um das Betriebssystem herunterzufahren und den Computer vollständig auszuschalten, indem alle Prozesse beendet werden und die Stromversorgung des Systems abgeschaltet wird.

* **poweroff** :Der Befehl "poweroff" wird verwendet, um das Betriebssystem herunterzufahren und den Computer vollständig auszuschalten, indem alle laufenden Prozesse beendet werden und die Stromversorgung des Systems abgeschaltet wird. Im Gegensatz zum Befehl "halt" wird der Computer nach dem Herunterfahren nicht im Ruhezustand gehalten, sondern vollständig ausgeschaltet.

* **systemctl** :Der Befehl "systemctl" wird verwendet, um Systemd-Dienste auf Linux-Systemen zu verwalten. Es ermöglicht das Starten, Stoppen, Neustarten, Aktivieren oder Deaktivieren von Diensten, das Anzeigen des Status von Diensten und das Verwalten von Systemeinheiten.

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

<br>

* **kill** :Der Befehl "kill" wird verwendet, um laufende Prozesse auf einem Linux-System zu beenden. Mit diesem Befehl können Prozesse anhand ihrer Prozess-ID (PID) gezielt beendet oder signale gesendet werden, um bestimmte Aktionen auf den Prozess auszuführen.
