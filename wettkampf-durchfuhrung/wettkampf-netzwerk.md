## Wettkampf im Netz bereitstellen {#wettkampfnetzwerk}

Die Wettkampf-Resultate lassen sich via der Mobile-Browserapp erfassen. Die darüber erfassten Resultate werden zunächst auf einem zentralen Server gespeichert und dann an die übrigen beteiligten Rechner aus dem Rechnungsbüro weiterverteilt.
Auf den Rechner im Rechnungsbüro kann dann die Erfassung gesteuert, kontrolliert und korrigiert werden.

### Schmatische Darstellung:

![](/assets/network-usecase.png)

### Technische Voraussetzungen

* Jeder Teilnehmer muss auf seinem Gerät am Wettkampf-Platz einen Internet-Zugang haben.
* Jeder Teilnehmer, der Resultate erfassen muss (Wertungsrichter) muss auf seinem Mobile-Device einen QR-Code Reader installiert haben. Leider gibt es zahlreiche gratis QR-Code scanner, welche z.B. Werbung einblenden oder Browser-Inhalte nicht im offiziellen Browser des Mobile-Devices öffnen. **Voraussetzung ist ein QR-Code Reader, der mit dem QR-Code den Standardbrowser auf dem Mobile-Device öffnen kann**, damit für die Erfassungs-App genügend Bildschirm-Fläche zur Verfügung steht.
* Grundsätzlich reicht jedoch der Standard-Bildschirm eines normalen Mobile-Devices mit einer Auflösung 360 x 640.
* Wenn der Internet-Zugang für die Wettkampf-App über einen **`Internet-Proxy`** erreichbar ist, muss vor der Verbindung in's Internet die Proxy-Einstellung konfiguriert werden:<br>![](/assets/internet-proxy-menu.png)<br>![](/assets/proxy-dialog.png)

### Sicherheits-Massnahmen

Für den Betrieb über das Netzwerk sind folgende Sicherheitsmassnahmen getroffen worden:
* Die Daten werden ausschliesslich über eine verschlüsselte Verbindung transferiert (HTTPS, SSL). Damit wird sichergestellt, dass die Daten unverfälscht übertragen werden und während der Übertragung von dritten nicht mitgelesen werden können.
* Lese-Zugriff auf die zentral bereitgestellten Daten wird jedem gewährt.
* Ein neuer Wettkampf darf jeder hochladen, sofern dieser Wettkampf eindeutig ist. Heruntergeladene Wettkämpfe können nicht wieder hochgeladen werden (Ausnahme siehe nächstes Kapitel).
* Die Mutation von Daten an einem im Netzwerk zur Verfügung gestellten Wettkampf ist nur mit einer gültigen Authentifizierung und Authorisierung möglich. Die Authorisierung gilt für maximal 24 Stunden.
* Die Authentifizierung/Authorisierung kann nur mit dem Link durchgeführt werden, der von dem Gerät stammt, von dem der Wettkampf im Netzwerk bereitgestellt wurde. Der Link kann via QR-Code, Browser-Link oder Link via EMail-Einladung verteilt werden. Es liegt in der Verantwortung des Wettkampf-Erstellers, wem dieser Link zugänglich gemacht wird.

### Wettkampf im Netz bereitstellen

1. Die Person, welche die Wettkampf-Planung wie unter [Wettkampf-Vorbereitung](wettkampf-vorbereitung/README.md) beschrieben erstellt hat, kann grundsätzlich darüber entscheiden, ob der Wettkampf im Netz geteilt wird. Ausgangslage ist der zunächst lokal erstellte Wettkampf mit einer Riegen- und Durchgangseinteilung.
2. Anschliessend kann der Wettkampf im Netz für die dezentrale Resultat-Erfassung bereitgestellt werden <br>![](/assets/upload-competition.png)<br>
Bei diesem Arbeitsschritt, wird nach erfolgreichem bereitstellen eine Erfolgsmeldung angezeigt: ![](/assets/connect-and-share.png)<br>
Gleichzeitig wird der Button `Verbindung stoppen` wählbar.
Für eine schnelle Kontrolle dient der Status-Button oben rechts im Fenster. Mit der Status-Lampe wird mit `grün` eine aktive und mit `grau` eine nicht aktive Verbindung angezeigt. Die Verbindung kann auch über diesen Status-Button ein- und ausgeschaltet werden.<br>

3. Weitere Interessierte können sich mit der Funktion `Wettkampf herunterladen` den kompletten Wettkampf über das Netzwerk herunterladen:<br>![](/assets/download-competitions.png)<br> ![](/assets/list-download-competitions.png)<br>
Nachdem ein Wettkampf heruntergeladen wurde, kann zwar lokal alles mit dem Wettkampf gemacht werden. Allerdings kann man sich nicht zu dem Wettkampf im Netzwerk verbinden und es können auch keine Daten mit dem Wettkampf im Netzwerk synchronisiert werden. Hierzu muss zunächst die volle Kontrolle über den Wettkampf erlangt werden.<br>
Es gibt zwei mögliche Verfahren, um die volle Kontrolle über den Wettkampf von einem Gerät auf das Andere zu übertragen:
    * Vom Gerät, auf dem der Wettkampf hochgeladen wurde, muss der Wettkampf wie bisher via `Import-`/`Export`-Funktion als Zip-Datei auf das zusätzliche Gerät kopiert werden. Die Datei enthält den Sicherheits-Schlüssel für den Vollzugriff auf diesen Wettkampf:<br>
    ![](/assets/competition-share-secret.png)<br> Diese Datei ist für den Benutzer **unsichtbar**. Mit diesem Vorgehen können mehrere Geräte die volle Kontrolle über den Wettkampf erlangen.
    * Nachdem der Wettkampf auf dem Ziel-Gerät heruntergeladen wurde, kann vom Gerät, wo er hochgeladen wurde der Wettkampf im Netzwerk entfernt werden (siehe [Wettkampf im Netzwerk entfernen](#wettkampfnetzwerk-entfernen)). Daraufhin kann der Wettkampf vom Ziel-Gerät frisch in's Netzwerk hochgeladen werden. Die Kontrolle des Wettkampfs liegt immer bei dem Gerät, von wo aus ein Wettkampf hochgeladen wurde. Mit diesem Verfahren liegt die volle Kontrolle über den Wettkampf immer nur bei einem Gerät.
4. Solange eine aktive Verbindung besteht, werden die Resultate über den zentralen Server mit allen anderen an diesem Wettkampf verbundenen Stationen synchronisiert. So ist es denn auch möglich, mit mehr als einer Station im Rechnungsbüro zu arbeiten, um so die Ausfallsicherheit zu erhöhen.

### Pro Gerät und Durchgang einen QR-Code für die Einstellung im Mobile-Device der Wertungsrichter erstellen {#qrcode-printouts}

Bevor der Wettkampf beginnt, sollten pro Gerät eine Liste der QR-Codes erstellt werden, die die Konfiguration des Mobile-Devices der Wertungsrichter sicherstellt.

![](/assets/prepare-station-qrcodes.png)

![](/assets/station-initialization-qrcode.png)

Diese QR-Codes sind lediglich für einen sicheren Einstieg zu den relevanten Wertungs-Eingabemasken gedacht und stellen kein Sicherheitselement bezüglich Zugriffsberechtigung dar. Sie können deshalb problemlos auf dem Wettkampf-Platz offen auf den Tischen der Wertungsrichter aufgelegt werden. Auch ein Versand per EMail an die Wertungsrichter wäre unproblematisch.

### Wertungsrichter Mobile register ...

Diese Funktion erlaubt es, die Personen als Wertungsrichter auf ihrem Mobile-Device zu berechtigen, an diesem Wettkampf Resultate zu erfassen. Es wird ein Fenster mit einem QR-Code angezeigt. Dieser QR-Code muss von jedem Mobile-Device, von wo Resultate erfasst werden sollen, gescannt werden.
Alternativ kann auch ein `Browser-Link` geöffnet werden oder ein `EMail` mit dem Link an die Wertungsrichter versendet werden.
Die Registrierung kann ab Herausgabe während 24 Stunden benutzt werden.

![](/assets/mobile-register.png)

### Wertungsrichter initialisiert sein Mobile-Device an seiner Station mit QR-Code

Bei jedem Gerät sollen die [QR-Codes ausgedruckt vorliegen](#qrcode-printouts), die an dem Gerät pro Durchgang verwendet werden sollen. Mit dem Scan des jeweiligen QR-Codes kann eine URL im Browser des Mobile-Devices geöffnet werden. Dort wird die Erfassungs-App genau an der Stelle gestartet, wo der Wertungsrichter die Resultate erfassen soll (beim richtigen Wettkampf, beim richtigen Gerät und beim richtigen Durchgang).

![](/assets/resultcatcher-initialized.png)

### Freischalten eines Durchganges für die Resultat-Erfassung über das Netzwerk

In der Wettkampf-App gibt es eine Ansicht Namens `Netzwerk-Dashboard` für die Kontrolle und Steuerung der Resultat-Erfassung während einem Wettkampf.
In dieser Ansicht ist schnell sichtbar, wo noch Resultate fehlen - resp. ob ein Durchgang vollständig ist.
Wenn über das Netzwerk Resultate erfasst werden sollen, muss ein Durchgang jeweils von dieser Ansicht aus `gestartet` werden.

![](/assets/durchgang-starten.png)

In der Ansicht wird dann die Startzeit eingetragen und die Resultat-Erfassung über die Mobile-Devices ist somit freigeschaltet.

![](/assets/resultcatcher-running.png)

Wenn alle Resultate einer Riege an einem Gerät erfasst sind, soll die Resultaterfassung für diese Riege an diesem Gerät abgeschlossen werden. Dies wird mittels `Eingabe abschliessen` gemacht und bewirkt zusätzlich, dass die nächste Riege für die Resultaterfassung geladen wird.

Wenn alle Resultate eines Durchganges erfasst sind, soll der `Durchgang abgeschlossen` werden, worauf keine weiteren Resultate via Mobile-Devices mehr engegengenommen werden.

![](/assets/durchgang-abschliessen.png)

![](/assets/durchgang-abgeschlossen.png)

![](/assets/resultaterfassen-gesperrt.png)

Die Aktionen zum starten und beenden sind als Popup-Menu Funtkionen auf dem jeweiligen Durchgang zugänglich und sind nur dann wählbar, wenn der Netzwerk-Modus eingeschaltet ist.

### Wertungsrichter erfasst Wettkampf-Resultate

Mit dem Button `RESULTATE` gelangt man in der Mobile-App zu den Turner/-Innen, die in der Reihenfolge aufgelistet werden, in der sie ihre Wettkampf-Übung vorturnen sollen.

1. Mit einem Click auf die Person öffnet sich die Noten-Eingabemaske.
2. Mit einem Click auf die D-Note kann die entsprechene Schwierigkeits-Note (D wie Difficulty) erfasst/korrigiert werden. Diese Note wird nur bei Kunstturn-Wettkämpfen verwendet. Beim Geräteturnen wird nur die E-Note erfasst.
3. Mit einem Click auf die E-Note kann die entsprechene Ausführungs-Note (E wie Execution) erfasst/korrigiert werden.
4. Die Endnote wird vom Programm berechnet und aktualisiert, wenn die `Save`-Aktion erfolgreich ausgeführt werden kann. Wenn z.B. die Berechtigung für die Resultat-Erfassung abgelaufen ist oder der Durchgang gerade gesperrt ist, können keine Resultate erfasst/korrigiert werden. Bei Athletiktests gibt es verschiedene Multiplikationsfaktoren, die mit der E-Note multipliziert die Endnote ausmachen. Bei Kunstturn-Wettkämpfen wird die D-Note und die E-Note zusammengezählt.

![](/assets/resultcatcher-results.png)

### Wettkampf Resultate lokal aktualisieren

Sollten bereits Daten über Mobile-Devices erfasst worden sein, bevor im Rechnungsbüro die zentrale Wettkampf-App mit dem Netzwerk verbunden war, können die lokalen Daten mit denjenigen aus dem Netzwerk überschrieben/ersetzt werden. Dies wirt mit der Aktion `Download` durchgeführt. Es wird eine Sicherheits-Abfrage angezeigt, wo noch einmal darauf hingewiesen wird, dass die lokal erfassten Daten allesamt mit denjenigen aus dem Netzwerk überschrieben werden.

![](/assets/wettkampf-herunterladen.png)

### Netzwerkmodus stoppen

Stoppt die Verbindung zum Netzwerk. Bei gestoppter Verbindung werden keine Resultate mehr zum oder vom Netzwerk synchronisiert.

![](/assets/network-disconnect.png)

### Wettkampf im Netzwerk entfernen {#wettkampfnetzwerk-entfernen}

Mit dieser Funktion wird der Wettkampf im Netzwerk entfernt und steht danach nicht mehr im Netzwerk zur Verfügung.

![](/assets/network-remove.png)