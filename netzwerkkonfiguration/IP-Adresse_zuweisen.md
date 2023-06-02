# IP-Adresse zuweisen


## Was ist eine IP-Adresse / Wieso will ich sie ändern?

Jedes digitale Gerät mit einer Internet-Verbindung hat heutzutage eine IP-Adresse. Sie werden in Form einer Abfolge von Zahlen kommuniziert. Jede Adresse ist auf ein verbundenes Gerät (oder Netzwerk) zurückzuführen, aber sie muss nicht immer konstant sein. Es hängt immer davon ab, in welchem Netzwerk du bist und wieviele andere Geräte sich in diesem befinden. 

>Ich werde sie hier nicht ausführlich erklären, aber wäre gut wenn man **wüsste**, womit man hier zu tun hat, wenn du sie ändern willst!

---

## Varianten auf der Konsole

Für folgende Beispiele musst du die Konsole auf deinem Linux System öffnen.

### 1. Der "ip" Command 

Die intuitivste Variante ist der ip-command. Kopieren sie und setzen sie ein (eckige Klammern weglassen):

`ip addr add [ip_address] dev [interface]`

Beim Wort "interface" geht bei dir sicher ein Fragezeichen auf, aber es ist gar nicht so kompliziert.

Bei Linux Systemen gibt es drei Arten von Netzwerkverbindungen (oder interfaces).

1. eth0
2. eth1
3. wlan0