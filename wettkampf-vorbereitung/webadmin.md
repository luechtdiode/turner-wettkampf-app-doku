# Admin-Web-App

Die Verwaltung eines Wettkampfes (Wettkampf anlegen/bearbeiten, Anmeldungen, Riegeneinteilung, Drehbuch, Ranglisten, Formulare) erfolgt in der **Admin-Web-App**, welche in jedem aktuellen Browser auf dem Desktop oder auf einem Tablet bedient werden kann. Sie ist die standardmässige Verwaltungsoberfläche und benötigt keine Installation.

Für Funktionen, welche die Admin-Web-App nicht abdeckt, kommt die [Desktop-App](../README.md) zum Einsatz. Welche Funktionen davon betroffen sind, wird unter [Wann braucht es die Desktop-App?](#wann-braucht-es-die-desktop-app) beschrieben.

## Zugang zur Admin-Web-App

Die Admin-Web-App wird über die Web-Adresse des zentralen Servers aufgerufen, zum Beispiel:

* Test-Umgebung: `https://test-kutuapp.sharevic.net`
* Produktions-Umgebung: `https://kutuapp.sharevic.net` (noch nicht installiert)

Der Admin-Bereich wird über den URL-Pfad `admin` aktiviert. Die Adresse lautet damit:

```
https://test-kutuapp.sharevic.net/admin
```

Der Admin-Modus kann zusätzlich mit dem Abfrage-Parameter `?admin=true` erzwungen werden. Solange der Admin-Modus aktiv ist, erscheinen im Menu die Einträge `Meine Wettkämpfe` und `Neuer Wettkampf`.

## Anmelden mit einem Admin-Secret

Der Zugriff auf einen bereits existierenden Wettkampf als Administrator/-In erfolgt über ein **Admin-Secret**. Dieses Secret erhält man von dem Gerät, 
auf dem der Wettkampf ursprünglich angelegt wurde, oder aus einer Sicherung des Wettkampfes.

Beim ersten Aufruf wird das Secret im Browser gespeichert (`localStorage`). Danach erscheint der Wettkampf unter `Meine Wettkämpfe` in der Admin-Web-App, ohne dass der Link erneut aufgerufen werden muss.

Ein somit initial angelegtes Admin-Secret z.B. bei der Neuanlage eines Wettkampfes ist **zeitlich unbegrenzt gültig**. Beim [Übertragen des Admin-Zugangs](wettkampf_uebersicht.md#admin-zugang-übertragen) kann die Gültigkeitsdauer des ausgegebenen Links festgelegt werden. Abgelaufene Secrets (bzw. die zugehörigen Wettkämpfe) werden automatisch aus `Meine Wettkämpfe` entfernt, sobald sie geladen werden. Ein betroffener Wettkampf kann jederzeit über einen neu ausgestellten admin-access Link wieder hinzugefügt werden.

## Meine Wettkämpfe

Unter `Meine Wettkämpfe` werden alle Wettkämpfe aufgelistet, für die ein Admin-Secret im Browser gespeichert ist:

![](/assets/webadmin-meine-wettkaempfe.png)

Mit dem Plus-Button unten rechts wird ein [neuer Wettkampf angelegt](wettkampf_anlegen.md). Mit dem Upload-Button in der Kopfzeile kann ein ZIP-Backup importiert werden. Ein Klick auf einen Wettkampf öffnet die [Wettkampf-Übersicht](wettkampf_uebersicht.md) mit den Verwaltungsfunktionen.

Über `Wettkampf` → `Wettkampf löschen` in der [Wettkampf-Übersicht](wettkampf_uebersicht.md) kann ein Wettkampf aus der Liste entfernt oder vollständig vom Server gelöscht werden – siehe [Wettkampf löschen](wettkampf_uebersicht.md#wettkampf-löschen).

## Wann braucht es die Desktop-App?

Die Admin-Web-App deckt die zentralen Verwaltungsaufgaben ab. Folgende Funktionen stehen weiterhin **nur in der Desktop-App** zur Verfügung:

* Pflege der Stammdaten (Vereine, Turner/-Innen) – siehe [Stammdatenpflege](../stammdatenpflege/README.md)
* Individuelle Riegen- Riege2- und Teamzuteilungen
* Individuelle Zeiten pro Kategorie und Disziplin
* [Notenblätter / Riegennotenblätter erstellen](notenblatter_riegennotenblatter_erstellen.md) (Druck)
* [Wettkampf-Modus einschalten](../wettkampf-durchfuhrung/wettkampf-modus.md) und [Wettkampf im Netz bereitstellen](../wettkampf-durchfuhrung/wettkampf-netzwerk.md)
* explizites Auslösen für die Erstellung der [Besten-Listen für die Durchsage nach Gerätewechsel](../wettkampf-durchfuhrung/besten-listen_fur_die_durchsage_nach_geratewechsel.md) (ist implizit in der Drehbuch-Ansicht implementiert, beim Gerätewechsel)
* [Resultat-Analysen](../resultatanalysen/README.md)
* [Bodenmusik katalogisieren](bodenmusik.md) und Bodenmusik-Player
* CSV-/Excel-Import von Anmeldungen
