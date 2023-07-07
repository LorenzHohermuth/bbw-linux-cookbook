# Netzverbindung aufbauen

## 1. **WLAN mit dem nmcli**

### **Vorbereitung**

Für diesen Schritt musst du nmcli installieren haben. Eigentlich ist es schon vorinstalliert auf den meisten Linux-Maschinen, aber vielleicht ist es das aus irgendeinem Grund nicht. 

System-Update:
``sudo apt update``

nmcli installieren:
``sudo apt install network-manager``

### **Mit Netzwerk Verbinden**

**Starten und prüfen**


"nmcli" ist eine Abkürzung für "NetworkManager command-line interface". 

Als allererstes solltest du nmcli und deine WLAN-Karte angeschaltet haben. 

Starte nmcli, falls du es schon installiert hast:

``systemctl start network-manager``

Prüfe, ob deine WLAN-Karte eingeschaltet ist und gib das in das command-line ein:

``nmcli radio wifi``

Falls sie aus ist, kannst du sie hiermit einschalten:

``nmcli radio wifi on``

Um zu sehen, welche Interfaces eine Verbindung haben, gib diesen Command ein:

``nmcli dev status`` 

Es sollte dir eine Liste mit allen interfaces und dem jeweiligem Status geben.

**Verbindungen aufbauen**

Jetzt kannst du dich mit dem Internet verbinden. Falls du nicht schon genau weisst, wie das SSID (der Name) deines WLANs heisst, gib diesen Command ein, um Netzwerke in der Nähe aufzulisten:

``nmcli dev wifi list``

Und das ist der Command, der dich verbindet. Ersetze YOUR_SSID:

``sudo nmcli dev wifi connect YOUR_SSID`` 

Falls du ein Passwort brauchst, frage den Verantwortlichen für das Netzwerk, dann benutze den hier und ersetze YOUR_PASSWORD:

``sudo nmcli dev wifi connect network-ssid password "YOUR_PASSWORD"``

Als dritte Option, falls du dein Passwort nicht auf dem Screen zeigen willst, nutze diesen hier:

``sudo nmcli --ask dev wifi connect network-ssid``

Das Programm wird dich dann nach deinem Passwort fragen. Während man es eintippt sieht man nur Punkte für jedes Zeichen.

---

## 2. **Für GUI-User (Ubuntu)**

Öffne das System Menu und wähle die WLAN-Sektion.
Klicke auf das Netzwerk, mit dem du dich verbinden möchtest und falls es dich dann nach einem Passwort fragt, gib es ein klicke auf "verbinden".

Das Icon ändert sich dann, je nach Verbindungsstatus. Je mehr Strichlein dir angezeigt werden, desto besser ist die Verbindung.