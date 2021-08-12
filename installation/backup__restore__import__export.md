# Backup / Restore / Import / Export

Alle Daten können per Sicherungs-Tool oder auch von Hand ab dem Verzeichnis `%userprofile%\kutuapp` gesichert resp. wegkopiert werden.

Genauso einfach können diese Dateien wieder dorthin kopiert werden. Beim Restore der Dateien sollte die App nicht gestartet sein.

Für einen totalen Reset der Daten kann dieses Verzeichnis auch einfach gelöscht werden. Es wird dann von der App automatisch wieder angelegt.

Wenn nur die Daten eines konkreten Wettkampfes gesichert werden sollen, kann hierfür die Funktion "`Wettkampf exportieren`" verwendet werden:

![Wettkampf exportieren Popup-Menu](/assets/wettkampf-export.png)

Ein solch exportierter Wettkampf beinhaltet folgende Daten:

* Alle Daten des Wettkampfes \(Name, Datum, Art, Auszeichnungs-Schwellwerte\).
* Alle Daten der dem Wettkampf zugeteilten Turner/-Innen.
* Alle Resultate, die im Wettkampf erfasst wurden.
* Alle Riegen- und Durchgangs-Einteilungen
* Die logo -Datei \(logo.jpg, logo.png, logo.svg\)
* Der Zugriffs-Schlüssel für die Administrations-Berechtigung auf dem Wettkampf, falls der Wettkampf in das Netzwerk hochgeladen wurde.

Folgende Daten **werden nicht in den Export verpackt**:

* Gespeicherte Listen \(Notenblätter, Rigennotenbläter, Ranglisten, Einteilung.csv etc.\) und andere Dateien, die im Wettkampf-Verzeichnis abgelegt sind.

Der Import dieser exportierten Daten kann auf jeder beliebigen anderen Turner-Wettkampf-App Installation erfolgen.

Die dabei importierten Daten werden mit den bereits vorhandenen Daten abgeglichen. Dabei werden folgende Regeln angewendet:

![Wettkampf importieren Popup-Menu](/assets/wettkampf-import.png)

* Ein Turner, eine Turnerin wird anhand des Geschlechts, Namens, Vornamens, Vereins und dem Jahrgang in der bestehenden Datenbank gesucht. Die Namen werden mit einem Ähnlichkeits-Test miteinander verglichen, so dass Tippfehler oder Varianten von verschiedenen Namens-Schreibweisen tolerant behandelt werden. Sofern der Turner resp. die Turnerin bereits existiert, wird er/sie nicht neu angelegt. Es findet eine Veredelung der Daten statt, indem z.B. ein Geburtsdatum mit 01.01.2000 durch ein Geburtsdatum 21.03.2000 veredelt wird. Ebenso bei den Adressfeldern.
* Die Wettkampf-Daten selbst werden zuvor komplett gelöscht, so dass sie konfliktfrei wieder importiert werden können.

