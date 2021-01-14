
# Änderungen an der Webseite vornehmen
Dieses Dokument fasst zusammen, in welcher Art die Webseite geupdated werden kann.

## Installations Tools:
1. Git installieren (https://git-scm.com/download/win)
2. NPM installieren (https://nodejs.org/en/download/) 32 o. 64 bit

## Repository Clonen
1. git bash öffnen (siehe Schritt 1, Installations Tools)
2. In Git Bash eingeben: 
>git clone https://github.com/drpohlmann/drpohlmann.github.io.git  
(nur notwendig, wenn Ordner noch nicht existiert!)
3. In Git Bash eingeben:
> cd drpohlmann.github.io  
(hiermit ändert sich der aktuelle Ordner zum korrekten Verzeichnis, dieser Schritt ist notwendig, für alle folgenden Befehle)

## Abhängigkeiten installieren (NPM)
1. Entpacken des Zip Archivs in einen Ordner, im besten Fall in den Nutzerdokumenten.
2. git bash öffnen (siehe Schritt 1, Installations Tools), wie oben mit cd in das soeben erstellte Verzeichnis wechseln (Schritt 1)
3. In Git Bash eingeben:
> npm install  
Diese Prozess kann je nach Internetverbindung 5-10 Minuten dauern

## Ändern der Webseite
Die Webseite basiert auf React. Die zu ändernden Dateien liegen unter dem Order src. Der Aufbau ist wie folgt:
> /src  
> -- components  
> ---- common  
> ---- publications  
> ---- vita  
> -- Contact.js  
> -- Picture.js  
> -- Publications.js  
> -- Vita.js  
> [...]  

Vita und Pubklikationen können in den Dateien Publications.js und Vita.js angepasst werden, das Schema sollte ersichtlich sein. Das Rendering sollte i.d.R. nicht angepasst werden müssen.

## Updaten der Webseite online
Nachdem die Webseite geupdated wurde, muss sie neu erstellt und hochgeladen werden. Um die Webseite neu zu erstellen wird die Gitbash benötigt.
1. Neubauen der React Applikation
> npm run build  
> (Dieser Befehl erstellt einen Ordner "build" im Wurzelverzeichnis des oben geclonten Repositories)
2. Kopieren aller Dateien des Unterordners "build" in das von Gitbash geclonte Verzeichnis (Repository Clonen, nicht Abhängigkeiten installieren)
3. Dateien für Git verfügbar machen
> git add .  
4. Kommentar schreiben, was geändert wurde
> git commit -am "Dies ist die Kommentarnachricht"
5. Änderungen auf GitHub hochladen
> git push
6. Nach wenigen Minuten sind die Änderungen auf https://drpohlmann.github.io/ verfügbar.
