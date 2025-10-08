# Integrierter Musikplayer für Bodenmusik

Wenn bei einer Boden-Wettkampfübung Musik abgespielt werden muss, wird das von der App mit einem
integrierten Media-Player unterstützt.

## Player

Der Musikplayer kann nur Musikdatein im `.mp3`-Format abspielen.
Er kann eine Liste von Musikdateien einlesen und dann Track für Track zum Abspielen laden.

Die in der App pro Turnerin hinterlegten Musikdateien können mit dem Player geladen und abgespielt werden.
Dies ist auch über die Web-App für die Erfassung der Resultate möglich.

Für die optimale Raumakustik können folgende Einstellungen justiert werden:

- Lautstärke.
- Balance links/rechts.
- Frequenzbänder.

![Mediaplayer](/assets/mediaplayer-skin.png)

### Benutzung des Players

Der Player kann immer nur maximal eine Datei zum Abspielen geladen haben. Erst wenn die Datei fertig abgespielt wurde, oder der Player explizit ausgeschaltet wird, kann eine neue Datei geladen werden.

Wenn eine Datei geladen ist, kann sie beliebig oft gestartet, pausiert und neu abgespielt werden.

Die Benutzung des Players macht erst wirklich Sinn, wenn zuvor die Musikdateien katalogisiert wurden (pro Turner/-In hinterleget).
Dies lässt sich bei vielen Teilnehmerinnen schlecht erst am Wettkampf-Tag machen.
Es wird empfohlen, die Katalogisierung vor dem Wettkampf vorzunehmen, so dass am Wettkampf die Dateien bereits bei den Turnerinnen hinterlegt sind und nur noch abgespielt werden müssen.

#### Player in der Wettkampf-App (an Musikanlage angeschlossen)

Folgende zusätzliche Funktionen sind nur im Player-Fenster der Wettkampf-App verfügbar:

- Mit den Skip-Buttons lässt sich von einem Track zum vorherigen oder nächsten springen. Wenn der aktuelle Track bereits gestartet wurde, wird er dabei wieder auf den Anfang positioniert.
- Mit dem Power-Button lässt sich der Player ausschalten. Die Musik wird dann gestoppt und der Player steht wieder allen zur Verfügung.
- Mit dem Eject-Button lassen sich individuelle Musikdateinen oder Dateilisten in den Player laden.

#### Player-Fernsteuerung in der Web-App für die Resultaterfassung

Der oder die Wertungsrichter/-In kann in der Online Web-App, da wo von den Wertungsrichter das Ergebnis einer Wettkampfübung erfasst wird, die Kontrolle des Players übernehmen. Hierzu gibt es folgende Funktionen, sofern eine Musikdatei hinterlegt wurde:

- Laden der Musikdatei in den Player (diese ist nur möglich, wenn der Player frei ist). Nach dem Laden der Musikdatei ist der Player belegt (und kann keine andere Musik laden).
- Ausschalten / Freigeben des Musikplayers, so dass andere Musikstücke geladen können, resp. dass der Player wieder für eine andere Wettkampfübung verwendet werden kann.
- Abspielen der im Player geladenen Musik. Dies ist nur möglich, wenn es sich um die vorher geladene Musik handelt. Wenn sonst jemand für eine andere Übung den Player mit einer Musik geladen hat, kann diese nicht kontrolliert werden.

Nach dem Abspielen der Musik **wird der Player automatisch freigegeben**.

Der Player in der Web-App **ist nur dann sichtbar, wenn die Steuerung für die Wertungsrichter freigegeben wurde**:

![Remote-Steuerung des Mediaplayers für die Wertungsrichter](/assets/mediaplayer-remotecontrol-enabled.png)
![Player-Fernsteuerung in der Web-App für die Resultaterfassung](/assets/mediaplayer-webapp.png)

Die Buttons werden erst **wählbar, wenn der Durchgang für die Resultaterfassung gestartet wurde**:

![starte den Druchgang, um auch den Mediaplayer wählbar zu machen](/assets/mediaplayer-start-durchgang.png)

Anschliessend kann die Steuerung im Web-Client genutzt werden:

1) ![](/assets/mediaplayer-webapp-enabled.png)
2) ![](/assets/mediaplayer-webapp-loaded.png)
3) ![](/assets/mediaplayer-webapp-playing.png)
4) ![](/assets/mediaplayer-webapp-finished.png)

Mit dem roten Power-Button wird die Musik-Belegung im Player freigegeben. Dies ist nur notwendig, wenn die Musik-Datei irrtümlicherweise geladen wurde. Normalerweise wird die Musik abgespielt und am Ende wird der Player automatisch freigegeben.

## Bodenmusik katalogisieren

Jeder Turnerin kann eine eigene Boden-Musik hinterlegt werden. Die hinterlegten Dateien müssen auf dem Gerät gespeichert sein, das am Wettkampf-Platz an der Musikanlage angeschlossen ist.

### Musik offline hinterlegen

In der Wettkampf-App wird die Bodenmusik in den jeweiligen Wertungs-Erfassungstabs einer Turnerin oder einem Turner zugewiesen.

![Lokal Musik zuweisen](/assets/mediaplayer-assign-local-music.png)

1) In der Athlet-Spalte wird angezeigt, ob eine Bodenmusik hinterlegt ist (mit dem Noten-Symbol)
2) Auf dem Bodenmusik-Button lässt sich ein Menu aufklappen.
3) Mit dem Befehl `Bodenmusik zuordnen ...` lässt sich im lokalen Dateisystem eine Bodenmusik auswählen. Diese wird dann in den Wettkampf aufenommen und dem Athlet resp. der Athlethin hinterlegt.

#### Optionaler Katalog-Abgleich mit dem Wettkampf auf dem Server

Wenn diese Zuweisungen durchgeführt werden, während die App mit dem Server verbunden ist, ist der Katalog automatisch auch auf dem Server nachgeführt.

Wenn dies im offline-Modus gemacht wird und später die Fernsteuerung über die Web-App benutzt werden soll, muss der Wettkampf explizit manuell via Upload auf den Server hochgeladen werden.

### Musik über die Wettkampf-Anmeldung hochladen

Wenn Vereine die Online-Registrierung für Wettkampf-Teilnehmer/-Innen nutzen, ist dort ebenfalls die Möglichkeit, pro Anmeldung eine Bodenmusik hochzuladen. Hier besteht ein Grössenlimit von 5Mb.

![](/assets/mediaplayer-registration-empty.png)

Der Wettkampf-Administrator lädt diese Dateien beim **Synchronisieren der Anmeldedaten** auf sein Gerät herunter, von wo die Dateien dann abgespielt werden können.

Der Katalog wird hiermit automatisch lokal und auf dem Server nachgeführt.

![](/assets/mediaplayer-registration-assigned.png)

Die in der Anmeldung hochgeladene Datei kann jeweils auch wieder aktualisiert, abgespielt oder wieder gelöscht werden. So könnte die Person, die die Anmeldungen durchführt ev. im Training mit der angemeldeten Turnerin zusammen verifizieren, ob die richtige Datei hochgeladen wurde.

![](/assets/mediaplayer-registration-preview-loaded.png)

Die via Online-Anmeldung hochgeladenen Dateien auf dem Server können nach dem abgeschlossenen Wettkampf aus Platzgründen durch die App gelöscht werden. Die lokal gespeicherten Musikdateien werden nur gelöscht, wenn dort der Wettkampf gelöscht wird.

## Transport der Musikdateien via Import-/Export

Die Musikdateien können, wenn sie nicht über die Online-Anmeldung hochgeladen werden, von irgendwelchen Datenträgern eingelesen und katalogisiert werden. Sie liegen dann bereit auf dem lokalen Dateisystem im Wettkampf-Verzeichnis unter `audiofiles`.
Wenn die lokal gespeicherten Musikdateien auf einem anderen Gerät abgespielt werden sollen, ist das sichergestellt indem der Wettkampf mit der Export-Funktion in eine Zip-Datei exportiert wird. Diese kann auf dem Ziel-Gerät manuell wieder importiert werden.

Aktuell sollte es allerdings immer nur ein Gerät sein, das dann mit dem Player ferngesteuert werden soll.

## Mutationen am Wettkampf-Tag

Die Katalogisierung kann auch während dem Wettkampf angepasst werden. 

Turner oder Turnerinnen, die sich kurzfristig abgemeldet haben und deshalb im Wettkampf entfernt werden, werden korrekt auch im Musik-Katalog nachgeführt.

Wenn ein separates Gerät für den Mediaplayer Anschluss eingerichtet wird, müssen die Katalog-Anpassungen auch auf diesem Gerät gemacht werden.
