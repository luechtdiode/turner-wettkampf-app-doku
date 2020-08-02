## Turneranmeldungen online verarbeiten {#turneranmeldungen-verarbeiten_online}

Sobald der angelegte Wettkampf im Netz bereit gestellt wurde, steht auf der Wettkampf-Übersicht der Link bereit, über welchen die Vereine die Anmeldungen tätigen können.

![Link für die Vereins-Anmeldungen via Internet](/assets/online-registration-link.png)

Es wird im folgenden zwischen dem Wettkampf lokal gespeichert und dem Wettkampf im Netz gespeichert unterschieden.

### Online-Anmeldungen, erfasst durch die Verantwortlichen der Vereine {#clubregistration}

Jeder Verein, der sich an diesem Wettkampf anmelden möchte, muss sich über dieses Online-Formular registrieren, welches sich mit Hilfe des oben erwähnten Links öffnen lässt:

![Online-Registrierung](/assets/verein-registration-form.png)

Anschliessend kann er seine Turnerinnen und Turner bei der entsprechenden Kategorie anmelden:

![Online-Turner-Registrierung](/assets/turner-registration-form.png)

Nach der Erfassung der Anmeldungen kann der Vereins-Verantwortliche in der Liste überwachen, ob seine Anmeldung in die Wettkampf-Einteilung übernommen wurde. 

![Status-Registrierung](/assets/status-registration.png)

Solange das noch nicht der Fall ist, wird der Status `pending`angezeigt. Sobald die Anmeldung berücksichtigt wurde, wird der Status `in sync`angezeigt.

### Abgleich der Online-Anmeldungen mit den Wettkampf-Einteilungen {#sync-registrations}

Für den Abgleich der Online-Anmeldedaten mit dem lokal gespeicherten Wettkampf muss die Verbindung mit dem Netzwerk aktiv sein (siehe Grosser Button mit grüner Lampe).

![offline](/assets/netzwerk-offline.png)

![online](/assets/netzwerk-online.png)

Mit der Funktion `Online Anmeldungen entgegennehmen` können die Vereinsanmeldungen in den lokal gespeicherten Wettkampf entgegengenommen werden. Die Funktion prüft jedesmal, was sich im lokal gespeicherten Wettkampf gegenüber der in der online erfassten Vereinsanmeldungen geändert hat und schlägt dann eine Liste von Mutationen vor, die am lokal gespeicherten Wettkampf durchgeführt werden können. 

![Synchronisierung Online-Anmeldungen](/assets/pending-sync-actions.png)

Wenn ein Verein nicht bereits in der lokalen Datenbank gespeichert ist, wird auch dessen übernahme notwendig, weil sonst dessen Anmeldungen nicht verarbeitet werden.

Wenn die Mutationen erfolgreich durchgeführt werden konnten, wird dies mit folgender Meldung bestätigt:

![Bestätigung Anmeldungen verarbeitet](/assets/bestaetigung-sync-actions.png)

Der neue Verein ist dann angelegt und dessen Turner und Turnerin im Wettkampf bei den entspr. Programmen/Kategorien eingeteilt. Der Riegenname wird automatisch generiert. Sofern bereits eine Durchgangsplanung gemacht wurde, ist dort zu überprüfen, ob die Riege bereits eingeteilt ist.

![Kontrolle der Anmeldungen](/assets/auto-assigned-riege.png)

![Kontrolle der Riegen-Einteilung im Durchgang](/assets/durchgangsplanung-nachbearbeitung.png)

Siehe auch 
* [Riegeneinteilung erstellen](riegeneinteilung_erstellen.md)
* [Riegenzuteilung nachbearbeiten](riegzuteilung_nachbearbeiten.md)


### Abschliessen der Anmeldungs-Verarbeitung

Nach der erfolgreiden Übernahme der Anmeldedaten (kann auch wiederholt gemacht werden), der überprüfung der korrekten Einteilung und der nachführung der Durchgangsplanung, **soll der Wettkampf wieder ins Netz aktualisiert werden**.
Erst dann ist die Anpassung für alle sichtbar, also auch für die Vereine, die ihre Anmeldungen auf dem Online-Formular überprüfen.
