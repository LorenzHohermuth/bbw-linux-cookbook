# Pipes und Umleitung

**Pipes und Umleitungen** werden in der Bash sehr häufig und von allen Benutzerebenen verwendet.
Dies kann ein Problem verursachen. 
Sie werden so häufig von allen Bash-Benutzern verwendet, dass viele ihre Feinheiten, ihre Funktionsweise und ihre volle Leistungsfähigkeit nicht verstehen.


## Einführung

Erfahren Sie, wie einfach es ist, mithilfe von Piping und Umleitung leistungsstarke Arbeitsabläufe zu erstellen, die Ihre Arbeit automatisieren und Ihnen Zeit und Mühe sparen.

In den beiden vorherigen Abschnitten haben wir uns eine Sammlung von Filtern angesehen, die Daten für uns manipulieren würden. In diesem Abschnitt werden wir sehen, wie wir sie zusammenfügen können, um eine leistungsfähigere Datenmanipulation durchzuführen.

Dieser Abschnitt erfordert ein wenig Lektüre. Auch wenn die Mechanismen und ihre Verwendung recht einfach sind, ist es wichtig, verschiedene Merkmale ihres Verhaltens zu verstehen, wenn Sie sie effektiv nutzen möchten.


## Also, was sind sie?

Mit jedem Programm, das wir auf der Befehlszeile ausführen, sind automatisch drei Datenströme verbunden.

- STDIN (0) - Standardeingabe (Daten werden in das Programm eingespeist)
- STDOUT (1) - Standardausgabe (vom Programm gedruckte Daten, standardmässig am Terminal)
- STDERR (2) - Standardfehler (für Fehlermeldungen wird auch standardmässig das Terminal verwendet)

Durch Piping und Umleitung können wir diese Ströme zwischen Programmen und Dateien verbinden, um Daten auf interessante und nützliche Weise weiterzuleiten.

Im Folgenden werden wir Piping und Umleitung anhand einiger Beispiele demonstrieren, aber diese Mechanismen funktionieren mit jedem Programm auf der Befehlszeile, nicht nur mit denen, die wir in den Beispielen verwendet haben.


## Umleitung zu einer Datei

Normalerweise erhalten wir unsere Ausgabe auf dem Bildschirm, was meistens praktisch ist, aber manchmal möchten wir sie vielleicht in einer Datei speichern, um sie aufzuzeichnen, in ein anderes System einzuspeisen oder an jemand anderen zu senden. Der Grösser-als-Operator ( > ) zeigt der Befehlszeile an, dass die Programmausgabe (oder was auch immer an STDOUT gesendet wird) in einer Datei gespeichert und nicht auf dem Bildschirm ausgegeben werden soll. Sehen wir uns ein Beispiel an.

    user@bash: ls
    barry.txt bob example.png firstfile foo1 video.mpeg
    user@bash: ls > myoutput
    user@bash: ls
    barry.txt bob example.png firstfile foo1 myoutput video.mpeg
    user@bash: cat myoutput
    barry.txt
    bob
    example.png
    firstfile
    foo1
    myoutput
    video.mpeg
    user@bash:


Lassen Sie es uns aufschlüsseln:

- Zeile 1 Beginnen wir damit, zu sehen, was sich in unserem aktuellen Verzeichnis befindet.
- Zeile 3 Jetzt führen wir denselben Befehl aus, aber dieses Mal verwenden wir das >, um das Terminal anzuweisen, die Ausgabe in der Datei myoutput zu speichern. Sie werden feststellen, dass wir die Datei vor dem Speichern nicht erstellen müssen. Das Terminal erstellt es automatisch, wenn es nicht existiert.
- Zeile 4 Wie Sie sehen, wurde unsere neue Datei erstellt.
- Zeile 6 Schauen wir uns an, was dort gespeichert wurde.


## Eingige Beobachtungen

Sie werden feststellen, dass im obigen Beispiel die in der Datei gespeicherte Ausgabe beim Drucken auf dem Bildschirm eine Datei pro Zeile und nicht die gesamte Ausgabe in einer Zeile war. Der Grund dafür ist, dass der Bildschirm eine bekannte Breite hat und das Programm seine Ausgabe entsprechend formatieren kann. Wenn wir umleiten, kann es sich um eine Datei oder um eine andere Stelle handeln. Daher ist es am sichersten, sie als einen Eintrag pro Zeile zu formatieren. Dies ermöglicht es uns auch, diese Daten später einfacher zu manipulieren, wie wir weiter unten auf der Seite sehen werden.

*Tip:*
>Beim Weiterleiten und Umleiten sind die tatsächlichen Daten immer dieselben, die Formatierung dieser Daten kann sich jedoch geringfügig von der Formatierung unterscheiden, die normalerweise auf dem Bildschirm angezeigt wird. Behalte dies im Kopf.

Sie werden auch feststellen, dass die Datei, die wir zum Speichern der Daten erstellt haben, ebenfalls in unserer Liste enthalten ist. Der Mechanismus funktioniert so, dass zunächst die Datei erstellt wird (sofern sie noch nicht vorhanden ist) und dann das Programm ausgeführt und die Ausgabe in der Datei gespeichert wird.


## Speichern in einer vorhandenen Datei

Wenn wir zu einer Datei weiterleiten, die nicht existiert, wird diese automatisch für uns erstellt. Wenn wir jedoch in eine bereits vorhandene Datei speichern, wird deren Inhalt gelöscht und die neue Ausgabe darin gespeichert.

    user@bash: cat myoutput
    barry.txt
    bob
    example.png
    firstfile
    foo1
    myoutput
    video.mpeg
    user@bash: wc -l barry.txt > myoutput
    user@bash: cat myoutput
    7 barry.txt
    user@bash:

Stattdessen können wir die neuen Daten erhalten, die an die Datei angehängt werden sollen, indem wir den Doppel-Grösser-als-Operator ( >> ) verwenden.   

    user@bash: cat myoutput
    7 barry.txt
    user@bash: ls >> myoutput
    user@bash: cat myoutput
    7 barry.txt
    barry.txt
    bob
    example.png
    firstfile
    foo1
    myoutput
    video.mpeg
    user@bash:
     

## Umleitung aus einer Datei

Wenn wir den Kleiner-als-Operator (<) verwenden, können wir Daten in die andere Richtung senden. Wir lesen Daten aus der Datei und geben sie über den STDIN-Stream an das Programm weiter.

    user@bash: wc -l myoutput
    8 myoutput
    user@bsh: wc -l < myoutput
    8
    user@bash:

Bei vielen Programmen (wie wir in den vorherigen Abschnitten gesehen haben) können wir eine Datei als Befehlszeilenargument angeben und den Inhalt dieser Datei lesen und verarbeiten. Vor diesem Hintergrund fragen Sie sich vielleicht, warum wir diesen Operator verwenden müssen. Das obige Beispiel veranschaulicht einen subtilen, aber nützlichen Unterschied. Sie werden feststellen, dass die Ausgabe des Programms den Namen der verarbeiteten Datei enthielt, als wir wc ausführten und die zu verarbeitende Datei als Befehlszeilenargument bereitstellten. Als wir es ausführten und den Inhalt der Datei in wc umleiteten, wurde der Dateiname nicht gedruckt. Dies liegt daran, dass die Daten immer dann anonym gesendet werden, wenn wir Umleitungen oder Pipes verwenden. Im obigen Beispiel hat wc also einige Inhalte zur Verarbeitung erhalten, weiss jedoch nicht, woher diese stammen, und gibt diese Informationen möglicherweise nicht aus. Infolge,

Wir können die beiden Umleitungsformen, die wir bisher kennengelernt haben, problemlos in einem einzigen Befehl kombinieren, wie im folgenden Beispiel dargestellt.

    user@bash: wc -l < barry.txt > myoutput
    user@bash: cat myoutput
    7
    user@bash:


## Umleitung von STDERR

Schauen wir uns nun den dritten Stream an, der Standardfehler oder STDERR ist. Den drei Streams sind tatsächlich Nummern zugeordnet (in Klammern in der Liste oben auf der Seite). STDERR ist Stream Nummer 2 und wir können diese Nummern verwenden, um die Streams zu identifizieren. Wenn wir vor dem > Operator eine Zahl platzieren, wird dieser Stream umgeleitet (wenn wir keine Zahl verwenden, wie wir es bisher getan haben, wird standardmässig Stream 1 verwendet).

    user@bash: ls -l video.mpg blah.foo
    ls: cannot access blah.foo: No such file or directory
    -rwxr--r-- 1 ryan users 6 May 16 09:14 video.mpg
    user@bash: ls -l video.mpg blah.foo 2> errors.txt
    -rwxr--r-- 1 ryan users 6 May 16 09:14 video.mpg
    user@bash: cat errors.txt
    ls: cannot access blah.foo: No such file or directory
    user@bash:

Vielleicht möchten wir sowohl die normale Ausgabe als auch die Fehlermeldungen in einer einzigen Datei speichern. Dies kann durch Umleiten des STDERR-Streams zum STDOUT-Stream und der Umleitung von STDOUT in eine Datei erfolgen. Wir leiten zuerst zu einer Datei um und leiten dann den Fehlerstrom um. Wir erkennen die Umleitung zu einem Stream, indem wir ein & vor die Stream-Nummer setzen (sonst würde es zu einer Datei namens 1 umleiten).

    user@bash: ls -l video.mpg blah.foo > myoutput 2>&1
    user@bash: cat myoutput
    ls: cannot access blah.foo: No such file or directory
    -rwxr--r-- 1 ryan users 6 May 16 09:14 video.mpg
    user@bash:


## Piping

Bisher haben wir uns mit dem Senden von Daten an und von Dateien beschäftigt. Jetzt werfen wir einen Blick auf einen Mechanismus zum Senden von Daten von einem Programm an ein anderes. Man nennt es Piping und der von uns verwendete Operator ist ( | ) (auf den meisten Tastaturen über dem Backslash ( \ ) zu finden). Dieser Operator leitet die Ausgabe des Programms auf der linken Seite als Eingabe an das Programm auf der rechten Seite weiter. Im folgenden Beispiel werden wir nur die ersten drei Dateien im Verzeichnis auflisten.

    user@bash: ls
    barry.txt bob example.png firstfile foo1 myoutput user@bash: video.mpeg
    ls | head -3
    barry.txt
    bob
    example.png
    user@bash:

Wir können so viele Programme zusammenfügen, wie wir möchten. Im folgenden Beispiel haben wir die Ausgabe dann an tail weitergeleitet, um nur die dritte Datei zu erhalten.

    user@bash: ls | head -3 | tail -1
    example.png
    user@bash:

*Tip:*
>Alle Befehlszeilenargumente, die wir für ein Programm bereitstellen, müssen neben diesem Programm stehen.

*Tip:*
>Ich erlebe oft, dass Leute versuchen, ihre Aufgaben in einem Zug aufzuschreiben, und dabei irgendwo einen Fehler machen. Sie denken dann, dass es sich um einen Punkt handelt, aber in Wirklichkeit ist es ein anderer Punkt. Sie verschwenden viel Zeit damit, ein nicht vorhandenes Problem zu beheben, ohne das tatsächliche Problem zu erkennen. Wenn Sie Ihre Pipes schrittweise aufbauen, tappen Sie nicht in diese Falle. Führen Sie das erste Programm aus und stellen Sie sicher, dass es die erwartete Ausgabe liefert. Fügen Sie dann das zweite Programm hinzu und überprüfen Sie es erneut, bevor Sie das dritte hinzufügen usw. Das erspart Ihnen viel Frust.

Sie können Pipes und Redirection auch kombinieren.

    user@bash: ls | head -3 | tail -1 > myoutput
    user@bash: cat myoutput
    example.png
    user@bash:


## Mehr Beispiele

Im Folgenden finden Sie einige weitere Beispiele, die Ihnen einen Eindruck davon vermitteln sollen, was Sie mit Pipes alles machen können. Es gibt viele Dinge, die Sie mit Pipes erreichen können, und dies sind nur einige davon. Mit Erfahrung und ein wenig kreativem Denken werden Sie sicher noch viele weitere Möglichkeiten finden, Pipes zu nutzen, um Ihr Leben einfacher zu machen.

Alle in den Beispielen verwendeten Programme sind Programme, die wir bereits gesehen haben. Ich habe einige Befehlszeilenargumente verwendet, die wir jedoch noch nicht behandelt haben. Schauen Sie sich die entsprechenden Manpages an, um herauszufinden, was sie tun. Sie können die Befehle auch selbst ausprobieren und schrittweise aufbauen, um genau zu sehen, was jeder Schritt bewirkt.

In diesem Beispiel sortieren wir die Auflistung eines Verzeichnisses, sodass alle Verzeichnisse zuerst aufgelistet werden.

    user@bash: ls -l /etc | tail -n +2 | sort
    drwxrwxr-x 3 nagios nagcmd 4096 Mar 29 08:52 nagios
    drwxr-x--- 2 news news 4096 Jan 27 02:22 news
    drwxr-x--- 2 root mysql 4096 Mar 6 22:39 mysql
    ...
    user@bash:

In diesem Beispiel werden wir die Ausgabe eines Programms weniger in das Programm einspeisen, damit wir sie einfacher anzeigen können.

    user@bash: ls -l /etc | less
    (Sie können den gesamten Bildschirm der Ausgabe scrollen. Probieren Sie es selbst aus.)

Identifizieren Sie alle Dateien in Ihrem Home-Verzeichnis, für die die Gruppe Schreibberechtigung hat.

    user@bash: ls -l ~ | grep '^.....w'
    drwxrwxr-x 3 ryan users 4096 Jan 21 04:12 dropbox
    user@bash:

Erstellen Sie eine Liste aller Benutzer, die eine Datei in einem bestimmten Verzeichnis besitzen, und geben Sie an, wie viele Dateien und Verzeichnisse sie besitzen.

    user@bash: ls -l /projects/ghosttrail | tail -n +2 | sed 's/\s\s*/ /g' | cut -d ' ' -f 3 | sort | uniq -c
    8 anne
    34 harry
    37 tina
    18 ryan
    user@bash:


## Zusammenfassung

**Dinge, die wir gelernt haben**

>\>  Speichern Sie die Ausgabe in einer Datei.  
>\>\>  Hängen Sie die Ausgabe an eine Datei an.  
><  Eingabe aus einer Datei lesen.  
>2\>  Fehlermeldungen umleiten.  
>|  Senden Sie die Ausgabe eines Programms als Eingabe an ein anderes Programm.  

**Wichtige Konzepte**

*Streams*  
    Jedes Programm, das Sie auf der Befehlszeile ausführen können, verfügt über drei Streams: STDIN, STDOUT und STDERR.

## Activitäten

Lassen Sie uns einige Daten verstümmeln:

- Experimentieren Sie zunächst damit, die Ausgabe verschiedener Befehle in einer Datei zu speichern. Überschreiben Sie die Datei und hängen Sie sie ebenfalls an. Stellen Sie sicher, dass Sie dabei sowohl absolute als auch relative Paths verwenden.
- Prüfen Sie nun, ob Sie nur die 20. letzte Datei im Verzeichnis /etc auflisten können.
- Überprüfen Sie abschliessend, ob Sie zählen können, für wie viele Dateien und Verzeichnisse Sie in Ihrem Home-Verzeichnis die Ausführungsberechtigung haben.

