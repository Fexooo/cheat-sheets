# Deutsches Git cheat sheet

Diese Datei erklärt einige basics zu Git und ist zum nachgucken der verschiedenen Kommandos gedacht. In dieser Datei wird ausschließlich auf die Konsolen Git Version eingegangen.
Es werden bisher hauptsächlich alltägliche Kommandos erläutert.

## Basics

### Einen Commit vorbereiten

Hinzufügen einer Datei in einen aktuellen commit.

``` shell
git add [PFAD_ZU_DATEI]
```

Dabei werden nur aktuelle Änderungen gespeichert. Besitzt eine Datei keine Änderung wird sie auch nicht zum commit hinzugefügt.
Um die aktuellen Änderungen in einem Ordner hinzuzufügen (NICHT EMPFOHLEN) kann auch das folgende Kommando verwendet werden.

```shell
git add .
```

### Commit lokal anlegen

Zum anlegen eines commits kann das folgende Kommando verwendet werden.

```shell
git commit -m "[NAME_DES_COMMITS]"
```

Dieser Commit ist nach dem ausführen bereits in der lokalen Git Historie hinterlegt.

### Zur Remote Repository pushen

Zum pushen neuer commits wird das folgende Kommando verwendet.

````shell
git push
````

Falls vorher ein Rebase stattgefunden hat wird die Git Historie mit dem remote branch nicht mehr übereinstimmen. Je nach Einstellung des Remote Git Servers wird dann der push fehlschlagen.
In diesem Falle und du weißt was du tust kannst du mit dem folgenden Kommando diese Sicherheitswarnung ignorieren und deinen lokalen Git Stand auf den Remote Server force pushen. (Klappt auch nur bei jeweiligen Rechten)

````shell
git push --force
````

### Änderungen der Remote Repository pullen

Falls jemand anderes auch an dem Projekt arbeitet oder aus welchem Grund auch immer die Remote Repository des aktuellen Branches Änderungen hat, die du noch nicht lokal hast, kannst du folgendes Kommando verwenden um diese herunterzuladen.

````shell
git pull
````

### Fetch

Um alle Änderungen der Remote Repository zu pullen unabhängig des aktuellen lokalen Branches kann das folgende Kommando verwendet werden.

```shell
git fetch --all
```

### Rebase

Falls du an einem Branch arbeitest und ein neues Feature auf dem main Branch gemerged wurde muss dein Branch vor dem Merge auf den Stand des main Branches gebracht werden. Also benötigst du einen Rebase.
Ein Rebase Prozess startest du mit dem Kommando:

````shell
git rebase origin/[BRANCH_NAME]
````

Wichtig ist bei einem Rebase Prozess, dass du bitte darauf achtest was dein Terminal dir erklärt und es dir auch durchliest. Jenachdem wo Änderungen vorgenommen wurden, kann es zu einem Rebase Konflikt kommen. In diesem Fall musst du die Dateien lokal kontrollieren und gegebenenfalls den Konflikt manuell lösen. Danach kannst du mit den Kommandos:

````shell
git add [PFAD_ZUR_DATEI] // Wichtig dieses Kommando für ALLE Dateien mit einem Konflikt ausführen
git rebase --continue
````

fortfahren.

### Neuen Branch erstellen

Einen neuen Branch kannst du lokal mit dem Kommando:

````shell
git checkout -b "[BRANCH_NAME]"
````

erstellen. Einen neuen Branch zu pushen funktioniert nahezu analog wie oben beschrieben mit den Commits. Nach dem Push Kommando wird dann allerdings ein spezifisches Push Kommando im Terminal vorgeschlagen. Dieses einfach kopieren und ausführen.

### Branches wechseln

Um einen Branch zu wechseln kann folgendes Kommando verwendet werden.

````shell
git branch "[BRANCH_NAME]"
````
