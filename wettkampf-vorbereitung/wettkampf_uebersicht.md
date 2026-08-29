# Wettkampf Übersicht

Die Wettkampf-Übersicht ist die zentrale Verwaltungsseite eines Wettkampfes in der [Admin-Web-App](webadmin.md). Sie wird geöffnet, indem in `Meine Wettkämpfe` auf den gewünschten Wettkampf geklickt wird:

![](/assets/webadmin-overview.png)

Im Kopf wird der Wettkampf mit Logo, Titel und Datum angezeigt. Darunter sind die Verwaltungsfunktionen gruppiert.

## Verwaltung

Über die Liste `Verwaltung` werden die einzelnen Bereiche des Wettkampfes geöffnet:

* **Formulare (Notenerfassung)** – [Formular Templates für die Notenerfassung](formular_templates_fuer_notenerfassung.md)
* **Anmeldungen** – [Turneranmeldungen online verarbeiten](turneranmeldungen/turneranmeldungen_verarbeiten_online.md)
* **Riegeneinteilung** – [Riegeneinteilung erstellen](riegeneinteilung_erstellen/README.md)
* **Wettkampf Drehbuch** – [Wettkampf Drehbuch](../wettkampf-durchfuhrung/drehbuch.md)
* **Ranglisten** – [Ranglisten erstellen](../wettkampf-durchfuhrung/ranglisten_erstellen.md)

## Links

Unter `Links` werden die öffentlichen Links zum Wettkampf bereitgestellt, die z.B. auf der Wettkampf-Homepage hinterlegt werden können, so dass die Teilnehmenden online auf die aktuellsten Daten zugreifen können:

* **Online-Anmeldung**: Öffnet die öffentliche Anmeldeseite. Zusätzlich wird ein QR-Code angezeigt, der auf dem Wettkampf-Platz ausgehängt werden kann.
* **Startliste**: Öffnet die öffentliche Online-Startliste. Auch hierfür wird ein QR-Code angezeigt.
* **Live-Resultate**: Öffnet die Live-Ansicht mit den aktuell erfassten Resultaten. Auch hierfür wird ein QR-Code angezeigt.

## Admin-Zugang übertragen

Über `Admin-Zugang übertragen` wird ein **Admin-Secret-Link** mit QR-Code erzeugt, mit dem der Admin-Zugang auf einen Wettkampf auf einem anderen Gerät freigeschaltet werden kann:

![](/assets/webadmin-admin-access-link.png)

Es kann eine **Gültigkeitsdauer** für den Link gewählt werden (1, 2, 3, 5, 7, 30 oder 365 Tage, oder unbegrenzt). Der Standard ist 7 Tage. Nach dem Ändern der Dauer wird der Link (und der QR-Code) neu erzeugt und muss dann erneut kopiert bzw. gescannt werden.

> **ACHTUNG**: Die Herausgabe dieser Berechtigung kann nicht rückgängig gemacht werden. Nur an autorisierte Personen übergeben! Ein abgelaufener Link führt dazu, dass der Wettkampf auf dem Zielgerät wieder aus `Meine Wettkämpfe` entfernt wird (siehe [Admin-Secret](webadmin.md#anmelden-mit-einem-admin-secret)).

## Wettkampf

* **Bearbeiten**: Öffnet die Anlegen-Maske mit den [Einstellungen zum Wettkampf](wettkampf_anlegen.md), die angepasst werden können.
* **Backup als ZIP herunterladen**: Lädt eine Sicherung des Wettkampfes als ZIP-Datei herunter.
* **Restore mit ZIP Backup hochladen**: Stellt einen Wettkampf aus einer ZIP-Datei wieder her.
* **Wettkampf kopieren**: Legt eine Kopie des Wettkampfes mit derselben Parametrisierung an (siehe [Wettkampf kopieren](wettkampf_anlegen.md#wettkampf-kopieren)).
* **Wettkampf löschen**: Siehe [Wettkampf löschen](#wettkampf-löschen) unten.

## Wettkampf löschen

Beim Befehl `Wettkampf löschen` wird abgefragt, wie der Wettkampf entfernt werden soll:

![](/assets/webadmin-competition-delete-dialog.png)

* **Nur aus dieser Liste entfernen**: Entfernt den Eintrag nur aus `Meine Wettkämpfe` in diesem Browser. Die Daten bleiben auf dem Server erhalten. Ein [neuer Admin-Zugang](webadmin.md#anmelden-mit-einem-admin-secret) kann den Wettkampf wieder hinzufügen.
* **Auch vom Server löschen**: Entfernt den Eintrag aus der Liste und löscht alle Daten (Athleten, Wertungen, Anmeldungen) **unwiderruflich** vom Server.

# Übersicht in der Desktop-App

# Übersicht der angemeldeten Vereine und Medallienbedarf

Im Übersicht-Tab werden pro Verein, Programm/Kategorie und Geschlecht die Anmeldungen statistisch angezeigt. Hiermit lassen sich schnell Vollständigkeits-Kontrollen durchführen. Die Daten eignen sich auch als Basis für weitergehende Verarbeitungen wie z.B. für die Startgeld-Budgetierung.

Je nach Angabe der Auszeichnungs-Schwelle wird anhand der Anmeldungen auch der Medallien-Bedarf tabellarisch ausgewiesen.

![](/assets/wettkampf-uebersicht.png)

## Wettkampf-Logo anpassen

Bei neu angelegten Wettkämpfen muss ggf. das Wettkampf-Logo angepasst werden. Hierzu gibt es die Funktion `Wettkampf-Logo laden` im Toolbar.

Die Datei muss eine der folgenden Datei-Endungen haben:

* "`.svg`" \(Vectorgraphic-Files\)
* "`.png`" \(Portable Networkgraphic-Files\)
* "`.jpg`" \(Joint Photographic Experts Group Graphic-Files\)
* "`.jpeg`" \(Joint Photographic Experts Group Graphic-Files\)

Bevorzugt werden "`.svg`"-Dateien, weil diese besser auf hochauflösenden Druckern dargestellt werden.

Die Dimensionen des Logos werden automatisch in die gewünschte Grösse skaliert. Zu kleine Bilder könnten dadurch verpixelt dargestellt werden.

Die ausgewählte Datei wird in den Wettkampf-Ordner kopiert und auf den Dateinamen `logo` mit gleicher Datei-Endung wie das Original umbenannt.

## Grundsätzliche Einstellungen zum Wettkampf

Weitere Einstellungen zum Wettkampf können im Wettkampf-Bearbeiten Dialog gemacht werden:
* [Rangierung bei Punktegleichstand](punktgleichstand.md)
* [Wettkampf-übergreifende Riegen Rotationsregel](riegenrotation.md)
* [Verwendung von Altersklassen](altersklassen.md)

## Teamregelung

Sofern Teamregeln definiert sind, wird eine Aufstellung gemacht, ob es gemäss den bisherigen Anmeldungen passende Team-Zusammenstellungen geben kann.
Siehe auch die detailierte Beschreibung für die [Definition von Team Zusammenstellungsregeln](teamregeln.md)

![](/assets/team-stats-extended.png)

Bei explizit definierten Gruppenzusammenfassungen, werden diese hier ebenfalls aufgelistet und in der Zusammenstellung der Teams berücksichtigt.
Auf den aufgelisteten Teams kann auch die Mitglieder-Liste ein- und ausgeblendet werden.

Sollten Mitglieder im Wettkampf von keiner Teamregel in ein Team zugeordnet werden können, werden diese hier ebenfalls in einger eigenen Gruppierung angezeigt.
Dies soll helfen, ungewollte Konstellationen zu erkennen.

## Nützliche Links

Es werden weitere Links bereitgestellt, die z.B. auf der Wettkampf Homepage hinterlegt werden können, so dass die Teilnehmenden online auf die aktuellsten Daten zugreifen können.

* Online Vereinsanmeldung
* Online Teilnehmerliste
* Online Wettkampfresultate

Die Links können nur verwendet werden, wenn der Wettkampf im Netz bereitgestellt wurde (siehe [Wettkampf über das Internet bereitstellen](../wettkampf-durchfuhrung/wettkampf-netzwerk.md)).

## Darstellung exportieren

Um die angezeigte Darstellung ausserhalb der App nutzen zu können lassen sich die Daten via `Übersicht drucken...` exportieren.

