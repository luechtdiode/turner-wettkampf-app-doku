# Wettkampf Drehbuch

Das **Wettkampf-Drehbuch** ist das zentrale Steuerungswerkzeug während der Wettkampf-Durchführung. Es zeigt den aktuellen Fortschritt aller Durchgänge und Gerätestationen und erlaubt es, die Durchgänge für die Resultat-Erfassung freizuschalten und abzuschliessen.

Es wird über die [Admin-Web-App](../wettkampf-vorbereitung/webadmin.md) geöffnet: In der [Wettkampf-Übersicht](../wettkampf-vorbereitung/wettkampf_uebersicht.md) unter `Verwaltung` → `Wettkampf Drehbuch`.

![](/assets/webadmin-drehbuch.png)

## Aufbau der Ansicht

Die Ansicht besteht aus mehreren Bereichen:

* **Übersicht (Stepper)**: Oben werden die Durchgänge bzw. Durchgangs-Gruppen als Schritte dargestellt. Der aktuell laufende Durchgang ist hervorgehoben. Für die Geräte-Stationen des Durchganges wird angezeigt, ob sie noch ausstehend, im `Einturnen`, aktiv oder bereits `Abgeschlossen` sind. Beim Erreichen von 100% wird die Station automatisch als abgeschlossen markiert; mit dem Button `Abschliessen` kann eine Station auch manuell abgeschlossen werden.
* **Fortschritts-Übersicht**: Eine Tabelle zeigt pro Durchgang die Zeitplanung (Plan, effektiver Start/Ende, Dauer) sowie pro Gerät den Erfassungsfortschritt der einzelnen Stationen in Prozent. In der Spalte `Fertig` steht der Gesamtfortschritt des Durchganges.
* **Ranglisten**: Am unteren Ende werden die gespeicherten Ranglisten mit ihrem Veröffentlichungs-Status aufgelistet (siehe [Ranglisten erstellen](ranglisten_erstellen.md)).

## Durchgang steuern

Pro Durchgang resp. pro Durchgangs-Gruppe stehen folgende Aktionen zur Verfügung (Symbole in der Spalte `Aktionen`):

* **Start** (grünes Play-Symbol): Der Durchgang wird gestartet und damit die Resultat-Erfassung für diesen Durchgang freigeschaltet. Bei einem beendeten Durchgang wird der Durchgang neu gestartet.
* **Abschliessen** (gelbes Checkmark-Symbol): Der Durchgang wird abgeschlossen, worauf keine weiteren Resultate mehr erfasst werden können.
* **Zurücksetzen** (rotes Refresh-Symbol): Die aufgezeichneten Durchgangszeiten werden zurückgesetzt (nach einer Sicherheits-Abfrage). Dies ist nützlich, wenn ein Durchgang erneut durchgeführt wird.

Bei Durchgangs-Gruppen wirken die Aktionen auf alle Durchgänge der Gruppe. Die Stepper-Ansicht ist klickbar: Ein noch nicht gestarteter Durchgang wird mit einem Klick gestartet.

## Wechsel zu einer Gerätestation

Ein Klick auf eine Station in der Fortschritts-Übersicht öffnet die entsprechende [Erfassungs-Station](resultat-erfassung_mit_notenblatter.md) in der Web-App, wo die Wertungen eingesehen und korrigiert werden können.

## Login-Link für die Wertungserfassung

Mit dem Button `Login-Link für Wertungserfassung anzeigen ...` wird ein Fenster mit dem Link und QR-Code geöffnet, über den sich Wertungsrichter auf ihren Mobile-Devices an der Erfassung anmelden können. Der Link kann direkt geöffnet oder per E-Mail versendet werden.

## Live-Aktualisierung

Das Drehbuch wird über eine WebSocket-Verbindung live aktualisiert. Wenn eine Station im `Einturnen` ist, eine Wertung erfasst wird oder ein Durchgang gestartet resp. abgeschlossen wird, wird die Anzeige auf allen geöffneten Geräten automatisch aktualisiert. Zusätzlich kann die Ansicht mit einem Pull-to-Refresh manuell neu geladen werden.
