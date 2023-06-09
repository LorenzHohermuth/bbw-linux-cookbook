# Netzwerk-Befehle in Linux
Netzwerkbefehle in Linux sind spezielle Befehle zur Verwaltung, Diagnose und Ausführung von Netzwerkoperationen. Sie ermöglichen es Benutzern, Informationen über Netzwerkschnittstellen, Verbindungen, Konfigurationen und den Datenverkehr abzurufen und zu manipulieren. Zu den grundlegenden Netzwerkbefehlen gehören:


## Netzwerkschnittstellen
Mit `ifconfig` können Sie Informationen über Netzwerkschnittstellen abrufen, wie z.B. IP-Adresse, Netzwerkmaske und MAC-Adresse. Es ermöglicht auch das Konfigurieren von Netzwerkschnittstellen, das Aktivieren oder Deaktivieren von Schnittstellen und das Anzeigen von Statistiken.


## Erreichbarkeit testen 
Der `ping`-Befehl wird verwendet, um die Erreichbarkeit eines Netzwerkgeräts oder einer IP-Adresse zu überprüfen. Er sendet ICMP Echo Request-Pakete an das Ziel und erwartet ICMP Echo Reply-Pakete als Antwort. Dadurch kann überprüft werden, ob ein bestimmtes Netzwerkgerät erreichbar ist.


## Informationen über Datenpaket-Pfad 
Mit `traceroute` können Sie den Pfad verfolgen, den ein Datenpaket von Ihrem System zu einer Zieladresse nimmt. Es zeigt die IP-Adressen der Geräte (Router), über die das Paket unterwegs ist, sowie die Zeit, die das Paket benötigt, um jedes Gerät zu erreichen.


## Netzwerk Informationen
Mit dem Befehl `netstat` ermöglicht man das Anzeigen von Informationen über Netzwerkverbindungen, Routing-Tabellen, Netzwerkstatistiken und Schnittstellenstatistiken. Sie können offene Verbindungen, lauschende Ports und andere Netzwerkdetails anzeigen.


## Remote-Verbindung
 Mit dem `ssh`-Befehl können Sie eine sichere Remote-Verbindung zu einem entfernten Linux-System herstellen. Es verwendet das Secure Shell-Protokoll (SSH), um eine verschlüsselte Verbindung herzustellen und ermöglicht die sichere Fernverwaltung des entfernten Systems.


## Secure Copy Protocol 
 Mit dem `scp`-Befehl können Sie Dateien sicher zwischen lokalem und entferntem System übertragen. Es verwendet ebenfalls das SSH-Protokoll, um eine verschlüsselte Übertragung zu gewährleisten.

Dies sind nur einige der grundlegenden Netzwerkbefehle in Linux. Mit ihnen haben Sie die Kontrolle über Ihre Netzwerkumgebung und können verschiedene Aufgaben im Zusammenhang mit Netzwerkverbindungen effektiv durchführen.


# Erweiterte Netzwerk-Befehle und Tools
### Netzwerküberwachungstools
- `tcpdump`: Mit dem `tcpdump`-Befehl können Sie den Netzwerkdatenverkehr auf einer bestimmten Netzwerkschnittstelle überwachen. Sie können Filter verwenden, um den erfassten Datenverkehr auf bestimmte Protokolle, IP-Adressen oder Ports zu beschränken. Dieser Befehl ist besonders nützlich für die Netzwerkdiagnose und das Debugging.

- `iptraf`: Mit `iptraf` können Sie Echtzeitstatistiken über den Netzwerkdatenverkehr auf Ihrem System anzeigen. Es zeigt detaillierte Informationen über die Übertragungsraten, die Anzahl der Pakete, die Protokolle und vieles mehr. `iptraf` ist ein leistungsstarkes Werkzeug zur Überwachung des Netzwerkverkehrs in Echtzeit.