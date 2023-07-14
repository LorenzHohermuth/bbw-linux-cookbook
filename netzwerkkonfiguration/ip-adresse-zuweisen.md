# 🏠 IP-Adresse zuweisen

## Was ist eine IP-Adresse / Wieso will ich sie ändern?

Jedes digitale Gerät mit einer Internet-Verbindung hat heutzutage eine IP-Adresse. Sie werden in Form einer Abfolge von Zahlen kommuniziert. Jede Adresse ist auf ein verbundenes Gerät (oder Netzwerk) zurückzuführen, aber sie muss nicht immer konstant sein. Es hängt immer davon ab, in welchem Netzwerk du bist und wieviele andere Geräte sich in diesem befinden.

> Ich werde sie hier nicht ausführlich erklären, aber wäre gut wenn man **wüsste**, womit man hier zu tun hat, wenn du sie ändern willst!

***

## 1. Der "ip" Command

Die intuitivste Variante ist der ip-command. Kopieren sie und setzen sie ein (eckige Klammern weglassen):

`ip addr add [ip_address] dev [interface]`

Beim Wort "interface" geht bei dir sicher ein Fragezeichen auf, aber es ist gar nicht so kompliziert.

Die Haupt-Interfaces sind die Ethernet und WLAN interfaces, weil sie natürlich die einzigen sind, mit denen man sich mit dem Internet verbinden kann.

* eth0, eth1 ...
* wlan0, wlan1 ...

Bevor du den vorherigen command ausführst, solltest du dich für ein Interface entscheiden. So kannst du deine aktiven Verbindungen sehen:

`ip addr`

Folgende könntest du dann manipulieren.

Dann gibst du den Command vom Anfang ein, als Bespiel:

`sudo ip addr add 192.168.56.21/24 dev eth1`

> "sudo" bedeutet "super user do". Manche Sachen kann nur der Admin auf dem Gerät tun, aber dieses Wort erleichtert dir das.

***

## 3. Der "ifconfig" Command

Um die IP-Adresse auf Linux zu ändern, kan man den Befehl "ifconfig" verwenden.

Um herauszufinden, welche Interfaces dein System hat, gib `ifconfig -a` ein. Oder um herauszufinden, welche verfügbar sind, gib `ifconfig -l` ein. Oder gib `ifconfig -u` ein, um zu sehen, welche aktiv sind.

Um eine Adresse zu ändern, gib "ifconfig" gefolgt vom interface und der neuen IP-Adresse ein.

Bsp: `sudo ifconfig eth0 192.168.56.21/24`

Die neue IP-Adresse wird dieser Schnittstelle zugewiesen.

***

## 3. Mit dem GUI (für Desktop Benutzer)

Öffne die Einstellungen vom GNOME dashboard und wähle "Netzwerk". Klicke das Zahnrad-Icon auf deiner Verbindung.

Geh zum "IPv4"-Tab und stelle um auf "Manuell", um deine Anpassungen vorzunehmen.

Wenn du die Verbindung neu startest, sollten die Änderungen Eintreffen!

***

## 4. IP-Adressen permanent machen

Leider verschwindet deine IP-Adresse bei einem System Reboot wieder, nach den zwei obigen Methoden. So kannst du sie permanent machen (keine Angst, es ist umkehrbar):

Im file "/etc/network/interfaces" wirst du sehen, dass deine IP gerade noch von einem DHCP-Client gesetzt würde werden.

So sollte der File-Content aussehen:

```
auto eth0 
iface eth0 inet dhcp
```

Editiere das File, dass es sich neu so liest:

```
auto enp0s3

iface enp0s3 inet static

address 192.168.56.20

netmask 255.255.255.0

gateway 192.168.40.31
```

Dann, damit die Änderungen in Kraft treten, führst du folgenden Command in der Konsole aus:

`sudo systemctl restart networking.service`

***

## 5. VPNs

Mit einer VPN (Virtual Private Network) kannst du unter anderem deine Daten schützen, dazu gehört dein Standort.

Wenn du die VPN einschaltest, wählst du ein Land aus, drückst auf den Start Button und zack! Du hast eine neue IP-Adresse, die nicht auf dich zurückführbar ist.
