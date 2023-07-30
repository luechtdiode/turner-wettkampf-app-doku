# Wettkampf im lokalen Netz bereitstellen

Die Wettkampf-Resultate lassen sich via der Mobile-Browserapp erfassen. Die darüber erfassten Resultate werden direkt auf dem im lokalen Netzwerk betriebenen Server gespeichert.\
Auf dem Rechner im Rechnungsbüro, von wo aus der lokale Server betrieben wird, kann dann die Erfassung gesteuert, kontrolliert und korrigiert werden.

## Schmatische Darstellung:

![](<../assets/network-usecase.png>)

## Technische Voraussetzungen

* Der Rechner, auf dem der lokale Server betrieben wird, muss eingehende TCP-Verbindungen auf dem Port 5757 akzeptieren (Konfiguration über Firewall/Defender des jeweiligen Betriebssystems).
* Der Rechner, auf dem der lokale Server betrieben wird, muss im lokalen Netzwerk eingebunden sein, über welches die Wertungsrichter sich verbinden sollen.
* Der Zugang zum lokalen Netzwerk wird idealerweise mit einem Zugangs-Schutz (Benutzer/Passwort etc.) geschützt.
* Jeder Teilnehmer muss auf seinem Gerät am Wettkampf-Platz einen Zugang zum lokalen Netzwerk/WLAN haben.
* Jeder Teilnehmer, der Resultate erfassen muss (Wertungsrichter) muss auf seinem Mobile-Device einen QR-Code Reader installiert haben. Leider gibt es zahlreiche gratis QR-Code scanner, welche z.B. Werbung einblenden oder Browser-Inhalte nicht im offiziellen Browser des Mobile-Devices öffnen. **Voraussetzung ist ein QR-Code Reader, der mit dem QR-Code den Standardbrowser auf dem Mobile-Device öffnen kann**, damit für die Erfassungs-App genügend Bildschirm-Fläche zur Verfügung steht.
* Grundsätzlich reicht jedoch der Standard-Bildschirm eines normalen Mobile-Devices mit einer Auflösung 360 x 640.

## Sicherheits-Massnahmen

Für den Betrieb über das Netzwerk sind folgende Sicherheitsmassnahmen getroffen worden:

* Lese-Zugriff auf die zentral bereitgestellten Daten wird jedem gewährt, der Zugang zum lokalen Netzwerk hat.
* Es können keine Wettkämpfe hoch- oder heruntergeladen werden.
* Die Funktion `Wettkämpfe im Netzwerk entfernen` steht nicht zur Verfügung.
* Die Mutation von Daten an einem im Netzwerk zur Verfügung gestellten Wettkampf ist nur mit einer gültigen Authentifizierung und Authorisierung möglich. Die Authorisierung gilt für maximal 24 Stunden.
* Die Authentifizierung/Authorisierung kann nur mit dem Link durchgeführt werden, der von dem Gerät stammt, von dem der Wettkampf im Netzwerk bereitgestellt wurde. Der Link kann via QR-Code, Browser-Link oder Link via EMail-Einladung verteilt werden. Es liegt in der Verantwortung des Wettkampf-Erstellers, wem dieser Link zugänglich gemacht wird.
* Im Unterschied zum Neztwerkbetrieb über das Internet findt die Datenübertragung im lokalen Netzwerkbetrieb standardmässig `nicht verschlüsselt` statt. Hierfür gibt es folgenden Grund: Ein lokal bereitgestellter Server mit SSL-Zertifikat, das von allen Endgeräten als sicher akzeptiert wird, erfordert das importieren des Server-Zertifikats auf alle Endgeräten. Dieser Vorgang ist komplex und Fehleranfällig. Bei Bedarf lässt sich die App jedoch entsprechend konfigurieren. Für diese Konfiguration ist Spezialisten-KnowHow erforderlich, weshalb dies hier nicht weiter beschrieben wird.

## Wettkampf im lokalen Netz bereitstellen

1. Mittels `Start local Server` im Netzwerk-Menu wird der Server im lokalen Netzwerk gestartet. ![](../assets/start-local-server.png) Sobald der Server gestartet ist, wird die Adresse im blauen Anzeigefeld oben rechts auf `localhost:5757` umgestellt. ![](../assets/display-local-server-offline.png).
2.  Anschliessend kann der Wettkampf im lokalen Netzwerk im `Netzwerk-Dashboard` für die dezentrale Resultat-Erfassung bereitgestellt werden\
    ![](../assets/upload-competition.png)

    Bei diesem Arbeitsschritt, wird nach erfolgreichem bereitstellen eine Erfolgsmeldung angezeigt:\
    ![](../assets/connect-and-share.png)

    Gleichzeitig wird der Button `Verbindung stoppen` wählbar.

    Für eine schnelle Kontrolle dient der Status-Button oben rechts im Fenster. Mit der Status-Lampe wird mit `grün` eine aktive und mit `grau` eine nicht aktive Verbindung angezeigt. Die Verbindung kann auch über diesen Status-Button ein- und ausgeschaltet werden.
3. Solange eine aktive Verbindung besteht, werden die Resultate über den lokalen Server mit allen anderen an diesem Wettkampf verbundenen Stationen synchronisiert. Im Gegensatz zur Verbindung über das Internet ist es nicht möglich, mit mehr als einer Station im Rechnungsbüro zu arbeiten.
4.  Mittels `Stop local Server` im Netzwerk-Menu wir der Server im lokalen Netzwer wieder gestoppt.\
    ![](../assets/stop-local-server.png)\
    Sobald der Server gestoppt ist, wird die Adresse im blauen Anzeigefeld oben rechts auf `kutuapp.sharevic.net` umgestellt.\
    ![](<../assets/display-remote-server-offline.png>)

    Diese Adresse wird verwendet, wenn der Netzwerkmodus über das Internet betrieben wird.

## Riegenblätter mit QR-Code für Direkteinstieg in die Erfassungs-Maske der Mobile-App drucken <a href="#qrcode-printouts" id="qrcode-printouts"></a>

![](../assets/print-riegenblaetter.png)

**Generiertes Riegennotenblatt:**

![](../assets/riegenblaetter.png)

**Achtung** Der auf den Riegenblätter gedruckte QR-Code enthält den Link auf den `lokalen Server` und funktioniert nicht im anderen Netzwerk-Modus, wo der Server nicht lokal betrieben wird.

Diese QR-Codes sind lediglich für einen sicheren Einstieg zu den relevanten Wertungs-Eingabemasken gedacht und stellen kein Sicherheitselement bezüglich Zugriffsberechtigung dar. Sie können deshalb problemlos auf dem Wettkampf-Platz offen auf den Tischen der Wertungsrichter aufgelegt werden.

## Mobile App Connections ...

![](<../assets/mobile-app-connections.png>)

Diese Funktion erlaubt es, die Personen als Wertungsrichter auf ihrem Mobile-Device zu berechtigen, an diesem Wettkampf Resultate zu erfassen. Es wird ein Fenster mit einem QR-Code für die folgenden Links angezeigt (Tabs auf der linken Dialogseite): 1. `Mobile-App`, 2. `Letzte Resultate`, 3. `Top Resultate`.

Falls das Gerät, auf dem der Server betrieben wird, mehrere Netzwerkanschlüsse hat, wird für jeden Netzwerkanschluss ein separater Tab mit den entsprechenden Links angezeigt. Das Programm kann in diesem Fall nicht entscheiden, welcher Netzwerk-Anschluss mit dem für die Wertungsrichter bereitgestellten lokalen Netzwerk verknüpft ist. Es müssen somit die einzelnen Adressen `ausprobiert` werden, um die funktionierenden Links zu finden. ![](<../assets/mobile-register.png>)

### Mobile-App Link

Dieser QR-Code muss von jedem Mobile-Device, von wo Resultate erfasst werden sollen, gescannt werden. Alternativ kann auch mit `Link im Browser öffnen` geöffnet werden oder mit `Link als EMail versenden` ein Link auf die Mobile-App mit Mutationsberechtigung an die Wertungsrichter versendet werden. Der Link kann ab Herausgabe während 24 Stunden für den Start der Mobile-App mit Mutationsberechtigung benutzt werden.

### Letzte Resultate Link

Dieser QR-Code führt mit einem Link auf die Anzeige der aktuell erfassten Resultaten. Siehe ![Aktuelle Wettkampf Resultate anzeigen](https://github.com/luechtdiode/turner-wettkampf-app-doku/tree/75f6f1ab61e90469693c54864ff38b520eb31438/wettkampf-durchfuhrung/#letzteResultate)

### Top Resultate Link

Dieser QR-Code führt mit einem Link auf die Anzeige der aktuell erfassten Top-Resultaten. Siehe ![Letzte Top Resultate anzeigen](https://github.com/luechtdiode/turner-wettkampf-app-doku/tree/75f6f1ab61e90469693c54864ff38b520eb31438/wettkampf-durchfuhrung/#topResultate)

## Wertungsrichter initialisiert sein Mobile-Device an seiner Station mit dem [QR-Code vom Riegenblatt](#qrcode-printouts)

Auf den Riegenblätter zur manuellen Resultaterfassung, befindet sich jeweils ein QR-Code, mit welchem die Mobile-App direkt am richtigen Ort gestartet werden kann. Zu Beginn kann es sein, dass die Resultaterfassung noch gesperrt ist. Diese wird durch die Wettkampfleitung im Rechnungsbüro freigegeben.

![](<../assets/resultaterfassen-gesperrt.png>)

## Freischalten eines Durchganges für die Resultat-Erfassung über das Netzwerk

In der Wettkampf-App gibt es eine Ansicht Namens `Netzwerk-Dashboard` für die Kontrolle und Steuerung der Resultat-Erfassung während einem Wettkampf. In dieser Ansicht ist schnell sichtbar, wo noch Resultate fehlen - resp. ob ein Durchgang vollständig ist. Wenn über das Netzwerk Resultate erfasst werden sollen, muss ein Durchgang jeweils von dieser Ansicht aus `gestartet` werden.

![](<../assets/durchgang-starten.png>)

In der Ansicht wird dann die Startzeit eingetragen und die Resultat-Erfassung über die Mobile-Devices ist somit freigeschaltet.

![](<../assets/resultcatcher-running.png>)

## Wertungsrichter erfasst Wettkampf-Resultate

Mit dem Button `RESULTATE` gelangt man in der Mobile-App zu den Turner/-Innen, die in der Reihenfolge aufgelistet werden, in der sie ihre Wettkampf-Übung vorturnen sollen.

| <p>Mit einem Click auf die Person öffnet sich die Noten-Eingabemaske.<br><br></p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | ![](<../assets/resultaterfassen-gestartet2.png>)    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- |
| <p>Bei Kunstturn-Wettkämpfen kann hier auch eine D-Note erfasst werden.</p><p>Mit einem Click auf die E-Note (1) kann die entsprechende Ausführungs-Note (E wie Execution) erfasst/korrigiert werden.</p><p>Die Endnote wird beim `Speichern` oder beim `Speichern &#x26; Weiter` (2) vom Programm berechnet und aktualisiert. Bei Athletiktests gibt es verschiedene Multiplikationsfaktoren, die mit der E-Note multipliziert die Endnote ausmachen. Bei Kunstturn-Wettkämpfen wird die D-Note und die E-Note zusammengezählt.</p><p>Es können auch Fehler gemeldet werden. Wenn z.B. die Berechtigung für die Resultat-Erfassung abgelaufen ist oder der Durchgang gerade gesperrt ist, können keine Resultate erfasst/korrigiert werden.</p><p><em>Achtung</em> Wenn die eingeblendete Nummer-Eingabetastatur die Buttons überdeckt, muss für dessen Betätigung der Bildschirm nach oben gescrollt werden, so dass die Buttons wieder sichtbar werden.</p> | ![](<../assets/resultcatcher-wertung-erfassen.png>) |

Wenn alle Resultate einer Riege an einem Gerät erfasst sind, soll die Resultaterfassung für diese Riege an diesem Gerät abgeschlossen werden. Dies wird mittels `Eingaben abschliessen` gemacht und bewirkt zusätzlich, dass die nächste Riege für die Resultaterfassung geladen wird.

## Durchgang abschliessen

Wenn alle Resultate eines Durchganges erfasst sind, soll der `Durchgang abgeschlossen` werden, worauf keine weiteren Resultate via Mobile-Devices mehr engegengenommen werden.

![](../assets/durchgang-abschliessen.png)

![](<../assets/durchgang-abgeschlossen.png>)

![](<../assets/resultaterfassen-gesperrt.png>)

Die Aktionen zum starten und beenden sind als Popup-Menu Funtkionen auf dem jeweiligen Durchgang zugänglich und sind nur dann wählbar, wenn der Netzwerk-Modus eingeschaltet ist.

## Aktuelle Wettkampf Resultate anzeigen <a href="#letzteresultate" id="letzteresultate"></a>

Die gerade gewerteten Wettkampf-Übungen können über ein digitales Resultate-Display angezeigt werden:

![](../assets/nav-resultat-display.png)

![](../assets/resultat-display.png)

Die Anzeige wird automatisch aktualisiert, wenn neue Resultate erfasst werden.

## Letzte Top-Resultate anzeigen <a href="#topresultate" id="topresultate"></a>

Wenn im `Wettkampf-Modus` und mit dem Netzwerk `verbunden` `(1)`, über die Funktion `Bestenliste (2)` ein Zusammenzug der besten Resultate der aktuellen Runde erstellt wird,

![](../assets/top-resultat-trigger.png)

kann dieser über das entsprechende elektronische Display über die App angezeigt werden:

![](../assets/nav-top-resultat-display.png)

![](../assets/top-resultat-display.png)

## Netzwerkmodus stoppen

Stoppt die Verbindung zum Netzwerk. Bei gestoppter Verbindung werden keine Resultate mehr zum oder vom Netzwerk synchronisiert.

![](../assets/network-disconnect.png)
