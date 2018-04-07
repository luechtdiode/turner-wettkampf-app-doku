## Wettkampf im Netz bereitstellen {#wettkampfnetzwerk}

Die Wettkampf-Resultate lassen sich via der Mobile-Browserapp erfassen. Die darüber erfassten Resultate werden zunächst auf einem zentralen Server gespeichert und dann an die übrigen beteiligten Rechner aus dem Rechnungsbüro weiterverteilt.
Auf den Rechner im Rechnungsbüro kann dann die Erfassung gesteuert, kontrolliert und korrigiert werden.

### Schmatische Darstellung:

![](/assets/network-usecase.png)

### Technische Voraussetzungen

* Jeder Teilnehmer muss auf seinem Gerät am Wettkampf-Platz einen Internet-Zugang haben.
* Jeder Teilnehmer, der Resultate erfassen muss (Kampfrichter) muss auf seinem Mobile-Device einen QR-Code Reader installiert haben. Leider gibt es zahlreiche gratis QR-Code scanner, welche z.B. Werbung einblenden oder Browser-Inhalte nicht im offiziellen Browser des Mobile-Devices öffnen. **Voraussetzung ist ein QR-Code Reader, der mit dem QR-Code den Standardbrowser auf dem Mobile-Device öffnen kann**, damit für die Erfassungs-App genügend Bildschirm-Fläche zur Verfügung steht.
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
Bei diesem Arbeitsschritt, wird nach erfolgreichem bereitstellen eine Erfolgsmeldung angezeigt und die Funktion `Connect and share` wird im Netzwerk-Menu wählbar: ![](/assets/connect-and-share.png)<br>
Für eine schnelle Kontrolle dient der Status-Button oben rechts im Fenster. Mit der Status-Lampe wird mit `grün` eine aktive und mit `grau` eine nicht aktive Verbindung angezeigt.<br>![](/assets/active-shareing.png)
3. Sofern der Wettkampf im Rechnungsbüro mit einem anderen Gerät durchgeführt wird, kann der Wettkampf auf dem anderen Gerät heruntergeladen werden: <br>  ![](/assets/download-competitions.png)<br> ![](/assets/list-download-competitions.png)<br>
Nachdem ein Wettkampf heruntergeladen wurde, kann zwar lokal alles mit dem Wettkampf gemacht werden. Allerdings kann man sich nicht zu dem Wettkampf im Netzwerk verbinden und es können auch keine Daten mit dem Wettkampf im Netzwerk synchronisiert werden. Hierzu muss zunächst die volle Kontrolle über den Wettkampf erlangt werden.<br>
Es gibt zwei mögliche Verfahren, um die volle Kontrolle über den Wettkampf von einem Gerät auf das Andere zu übertragen:
    * Vom Gerät, auf dem der Wettkampf hochgeladen wurde, muss eine Datei auf das zusätzliche Gerät kopiert werden. Die Datei enthält den Sicherheits-Schlüssel für den Vollzugriff auf diesen Wettkampf:<br>
    ![](/assets/competition-share-secret.png)<br> Diese Datei ist für den Benutzer **unsichtbar**, Es empfiehlt sich also, den gesamten Wettkampf-ordner von `%userprofile%\kutuapp\data` zu kopieren. Mittels der Funktion ![](/assets/open-competition-folder.png) kann direkt dorhin navigiert werden. Mit diesem Vorgehen können mehrere Geräte die volle Kontrolle über den Wettkampf erlangen.
    * Nachdem der Wettkampf auf dem Ziel-Gerät heruntergeladen wurde, kann vom Gerät, wo er hochgeladen wurde der Wettkampf im Netzwerk entfernt werden (siehe [Wettkampf im Netzwerk entfernen](#wettkampfnetzwerk-entfernen)). Daraufhin kann der Wettkampf vom Ziel-Gerät frisch in's Netzwerk hochgeladen werden. Die Kontrolle des Wettkampfs liegt immer bei dem Gerät, von wo aus ein Wettkampf hochgeladen wurde. Mit diesem Verfahren liegt die volle Kontrolle über den Wettkampf immer nur bei einem Gerät.
4. Solange eine aktive Verbindung besteht, werden die Resultate über den zentralen Server mit allen anderen an diesem Wettkampf verbundenen Stationen synchronisiert. So ist es denn auch möglich, mit mehr als einer Station im Rechnungsbüro zu arbeiten, um so die Ausfallsicherheit zu erhöhen.

### Pro Gerät und Durchgang einen QR-Code für die Einstellung im Mobile-Device der Kampfrichter erstellen {#qrcode-printouts}

Bevor der Wettkampf beginnt, sollten pro Gerät eine Liste der QR-Codes erstellt werden, die die Konfiguration des Mobile-Devices der Kampfrichter sicherstellt.<br>![](/assets/prepare-station-qrcodes.png)<br>![](/assets/station-initialization-qrcode.png)<br>
Diese QR-Codes sind lediglich für einen sicheren Einstieg zu den relevanten Wertungs-Eingabemasken gedacht und stellen kein Sicherheitselement bezüglich Zugriffsberechtigung dar. Sie können deshalb problemlos auf dem Wettkampf-Platz offen auf den Tischen der Kampfrichter aufgelegt werden. Auch ein Versand per EMail an die Kampfrichter wäre unproblematisch.

### Kampfrichter Mobile register ...

Diese Funktion erlaubt es, die Personen auf ihrem Mobile-Device zu berechtigen, an diesem Wettkampf Resultate zu erfassen. Es wird ein Fenster mit einem QR-Code angezeigt. Dieser QR-Code muss von jedem Mobile-Device, von wo Resultate erfasst werden sollen, gescannt werden.
Alternativ kann auch ein `Browser-Link` geöffnet werden oder ein `EMail` mit dem Link an die Kampfrichter versendet werden.
Die Registrierung kann ab Herausgabe während 24 Stunden benutzt werden.<br>![](/assets/mobile-register.png)<br>
![](/assets/resultcatcher-home.png)

### Kampfrichter initialisiert sein Mobile-Device an seiner Station mit QR-Code

Bei jedem Gerät sollen die [QR-Codes ausgedruckt vorliegen](#qrcode-printouts), die an dem Gerät pro Durchgang verwendet werden sollen. Mit dem Scan des jeweiligen QR-Codes kann eine URL im Browser des Mobile-Devices geöffnet werden. Dort wird die Erfassungs-App genau an der Stelle gestartet, wo der Kampfrichter die Resultate erfassen soll (beim richtigen Wettkampf, beim richtigen Gerät und beim richtigen Durchgang).<br>
![](/assets/resultcatcher-initialized.png)

### Freischalten eines Durchganges für die Resultat-Erfassung über das Netzwerk

In der Wettkampf-App gibt es eine Ansicht Namens `Netzwerk-Dashboard` für die Kontrolle und Steuerung der Resultat-Erfassung während einem Wettkampf.
In dieser Ansicht ist schnell sichtbar, wo noch Resultate fehlen - resp. ob ein Durchgang vollständig ist.
Wenn über das Netzwerk Resultate erfasst werden sollen, muss ein Durchgang jeweils von dieser Ansicht aus `gestartet` werden.
In der Ansicht wird dann die Startzeit eingetragen und die Resultat-Erfassung über die Mobile-Devices ist somit freigeschaltet.
Wenn alle Resultate eines Durchganges erfasst sind, soll er `beendet` werden, worauf keine weiteren Resultate via Mobile-Devices mehr engegengenommen werden.
Die Aktionen zum starten und beenden sind als Popup-Menu Funtkionen auf dem jeweiligen Durchgang zugänglich und sind nur dann wählbar, wenn der Netzwerk-Modus eingeschaltet ist.

### Kampfrichter erfasst Wettkampf-Resultate

Mit dem Button `RESULTATE` gelangt man in der Mobile-App zu den Turner/-Innen, die in der Reihenfolge aufgelistet werden, in der sie ihre Wettkampf-Übung vorturnen sollen.<br>
![](/assets/resultcatcher-riegenlist.png)![](/assets/resultcatcher-wertung.png)

### Wettkampf Resultate lokal aktualisieren

Sollten bereits Daten über Mobile-Devices erfasst worden sein, bevor im Rechnungsbüro die zentrale Wettkampf-App mit dem Netzwerk verbunden war, können die lokalen Daten mit denjenigen aus dem Netzwerk überschrieben/ersetzt werden.

### Netzwerkmodus stoppen

Stoppt die Verbindung zum Netzwerk. Bei gestoppter Verbindung werden keine Resultate mehr zum oder vom Netzwerk synchronisiert.

### Wettkampf im Netzwerk entfernen {#wettkampfnetzwerk-entfernen}

Mit dieser Funktion wird der Wettkampf im Netzwerk entfernt und steht danach nicht mehr im Netzwerk zur Verfügung.