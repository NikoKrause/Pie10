# GitHub Tutorial

## Git auf dem Rechner installieren und einrichten

### Installation:
```
sudo apt-get install git
```


### Einrichtung:
Vor Arbeitsbeginn sollte man den eigenen Namen und eine E-Mail-Adresse eintragen:
```
git config --global user.name NAME
git config --global user.email EMAIL@ADRESSE.de
```

Um die Lesbarkeit zu erhöhen, sollte man die Ausgaben mit den folgenden Befehlen einfärben:
```
git config --global color.ui "auto"
```

Es empiehlt sich `git` mitzuteilen, welches dein Lieblingseditor ist (z.B. `atom`), um Commit Nachrichten zu erstellen und zu bearbeiten:
```
git config --global core.editor atom
```


### Lokale Kopie dieses Repositories (Pie10) auf deinem Rechner erstellen
Öffne ein Terminal und navigiere dort hin, wo der Ordner `Pie10` erstellt werden soll, z.B.
```
cd Dokumente
```

Klone das Repo:
```
git clone https://github.com/NikoKrause/Pie10.git
```

### Erstelle deinen eigenen Branch
Öffne Terminal in deinem lokalen `Pie10` Ordner. Teste den Status deines Repos:
```
git status
```

Output müsste so aussehen:
```
Auf Branch master
Ihr Branch ist auf dem selben Stand wie 'origin/master'.
```

Info: Der Branch `master` ist dein lokaler Branch. Der Branch `origin/master` ist der online `master` Branch.

Erstelle nun deinen eigenen Branch, auf dem du arbeiten kannst, ohne Konflikte befürchten zu müssen:
```
git checkout -b test
```

Wenn du Status testet mit `git status` ist der Output:
```
Auf Branch test
```

Das heißt es gibt noch keine online Version dieses Branches. Um auch eine online Version zu erstellen:
```
git push -u origin test
```

Nach Eingabe von Benutzername und Passwort hat man:
```
Branch test konfiguriert zum Folgen von Remote-Branch test von origin.
```

Jetzt zeigt `git status`
```
Auf Branch test
Ihr Branch ist auf dem selben Stand wie 'origin/test'.
```

Deine lokalen Branches kannst du sehen mit:
```
git branch
```

bzw. alle Branches anzeigen mit
```
git branch -a
```

Jetzt kannst du Änderungen im Projekt vornehmen. Mit `git status` werden dir die geänderten Dateien angezeigt.

#### Quellen:
* https://wiki.ubuntuusers.de/Git/
* https://git-scm.com/book/de/v1/Git-individuell-einrichten-Git-Konfiguration
