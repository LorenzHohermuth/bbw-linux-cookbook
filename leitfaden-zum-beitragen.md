# 🤝 Leitfaden zum Beitragen

Damit jeder weiss, wie er eigenen Einträge zu unserem **Linux Cookbook** beitragen kann, steht hier eine klare Anleitung.

-   [Repository aufsetzen](#repository-aufsetzen)
-   [Eintrag erstellen](#eintrag-erstellen)
-   [Eintrag ins Hauptrepository mergen](#eintrag-ins-hauptrepository-mergen)
-   [Eigener Fork synchronisieren](#eigener-fork-synchronisieren)

> ℹ️ Fork = geklontes Repository auf dem eigenen Account

📝 **[Markdown Cheatsheet](https://www.markdownguide.org/cheat-sheet/)**

## Repository aufsetzen

Bevor du starten kannst mit dem Erstellen deiner Einträge, muss zuerst das Repository aufgesetzt werden.

1. Gehe auf das Repository [BBW Linux Cookbook](https://github.com/LorenzHohermuth/bbw-linux-cookbook)
2. Klicke oben rechts auf "Fork" und erstelle deinen Fork

Nun hast du das Hauptrepository auf deinen eigenen Account "geforkt" und hast deine eigene Kopie des **Linux Cookbook**. Im eigenen Fork wird ab jetzt gearbeitet.

3. Eigener Fork auf Desktop clonen

```sh
git clone https://github.com/<username>/bbw-linux-cookbook
```

4. Fork im gewünschten Texteditor öffnen

## Eintrag erstellen

Um nun zu beginnen mit dem Schreiben deiner Einträge, erstellst du nach simplen Vorschriften deine Dateien.

1. Neue Datei erstellen mit dem Namen in _kebab-case_ und der Endung auf `.md`. _Beispiel: `permission-system.md`_

> ℹ️ Der erste Titel (Heading 1) in der Datei wird auch als Seitentitel verwendet.

2. Falls der Eintrag in ein Unterthema gehört, dann in den jeweiligen Ordner verschieben.
3. Der Link zu deinem erstellten Eintrag an richtiger Stelle in das `SUMMARY.md` schreiben.

## Eintrag ins Hauptrepository mergen

Nach dem Beenden deines Eintrages muss er jetzt in das Hauptrepository gemergt werden. Damit dies problemlos verläuft, folge den folgenden Schritten.

1. Alle Änderungen in den eigene Fork committen
2. Gehe auf die Seite deines Forkes
3. Klicke auf das "Conribute" dropdown
4. Klicke nun auf "Open pull request"
5. Beschreibe falls nötig kurz deine Veränderungen
6. Warte bis dein Pull Request von den Leads angeschaut wird und möglicherweise nach Revisionen gefragt wird

Nachdem dein Eintrag angenommen wurde, beginnt das ganze wieder von vorne. Nicht vergessen deinen [Fork zu synchronisieren](#eigener-fork-synchronisieren).

## Eigener Fork synchronisieren

Wenn jeder seine Änderungen zum Hauptrepository beiträgt, kann es schnell passieren dass der eigene Fork nicht mehr auf dem neusten Stand ist. Darum muss man ihn regelmässig synchronisieren.

1. Geh auf die Seite deines Forkes.
2. Klicke auf das "Sync fork" dropdown und bestätige das synchronisieren.

> ℹ️ Aufpassen, nur synchronisieren wenn alle Änderungen schon im Hauptrepository sind. Ansonsten können diese möglicherweise gelöscht/überschrieben werden.

_Bei Fragen/Problemen, einen Lead anschreiben._
