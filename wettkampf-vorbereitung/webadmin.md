# Admin-Web-App

Die Verwaltung eines Wettkampfes (Wettkampf anlegen/bearbeiten, Anmeldungen, Riegeneinteilung, Drehbuch, Ranglisten, Formulare) erfolgt in der **Admin-Web-App**, welche in jedem aktuellen Browser auf dem Desktop oder auf einem Tablet bedient werden kann. Sie ist die standardmässige Verwaltungsoberfläche und benötigt keine Installation.

Für Funktionen, welche die Admin-Web-App nicht abdeckt, kommt die [Desktop-App](../README.md) zum Einsatz. Welche Funktionen davon betroffen sind, wird unter [Wann braucht es die Desktop-App?](#wann-braucht-es-die-desktop-app) beschrieben.

## Zugang zur Admin-Web-App

Die Admin-Web-App wird über die Web-Adresse des zentralen Servers aufgerufen, zum Beispiel:

* Test-Umgebung: `https://kutuapp-test.sharevic.net`
* Produktions-Umgebung: `https://kutuapp.sharevic.net`

Der Admin-Bereich wird über den URL-Pfad `admin` aktiviert. Die Adresse lautet damit:

```
https://kutuapp-test.sharevic.net/admin
```

Der Admin-Modus kann zusätzlich mit dem Abfrage-Parameter `?admin=true` erzwungen werden. Solange der Admin-Modus aktiv ist, erscheinen im Menu die Einträge `Meine Wettkämpfe`, `Neuer Wettkampf` und `Sicherheit`.

## Anmelden mit einem Admin-Secret

Der Zugriff auf einen Wettkampf als Administrator/-In erfolgt über ein **Admin-Secret**. Dieses Secret erhält man von dem Gerät, auf dem der Wettkampf ursprünglich angelegt wurde, oder aus einer Sicherung des Wettkampfes. Es wird über eine URL, einen QR-Code oder per E-Mail weitergegeben.

Der tief verlinkte Admin-Zugang ist als base64-codierter Query-Parameter aufgebaut:

```
https://kutuapp-test.sharevic.net/?<base64("admin&uuid=<Wettkampf-UUID>&secret=<Admin-Secret>")>
```

Beim ersten Aufruf wird das Secret im Browser gespeichert (`localStorage`). Danach erscheint der Wettkampf unter `Meine Wettkämpfe` in der Admin-Web-App, ohne dass der Link erneut aufgerufen werden muss.

## Meine Wettkämpfe

Unter `Meine Wettkämpfe` werden alle Wettkämpfe aufgelistet, für die ein Admin-Secret im Browser gespeichert ist:

![](/assets/webadmin-meine-wettkaempfe.png)

Mit dem Plus-Button unten rechts wird ein [neuer Wettkampf angelegt](wettkampf_anlegen.md). Mit dem Upload-Button in der Kopfzeile kann ein ZIP-Backup importiert werden. Ein Klick auf einen Wettkampf öffnet die [Wettkampf-Übersicht](wettkampf_uebersicht.md) mit den Verwaltungsfunktionen.

## Sicherheit

Auf der Seite `Sicherheit` werden alle im Browser gespeicherten Wettkampf-Secrets aufgelistet:

![](/assets/webadmin-sicherheit.png)

Pro Wettkampf werden Titel, Datum und die Wettkampf-UUID angezeigt. Mit dem Papierkorb-Button wird das Secret aus dem Browser entfernt. Damit wird der Zugriff auf den betreffenden Wettkampf in der Admin-Web-App auf diesem Gerät beendet.

## Wann braucht es die Desktop-App?

Die Admin-Web-App deckt die zentralen Verwaltungsaufgaben ab. Folgende Funktionen stehen weiterhin **nur in der Desktop-App** zur Verfügung:

* Pflege der Stammdaten (Vereine, Turner/-Innen) – siehe [Stammdatenpflege](../stammdatenpflege/README.md)
* [Notenblätter / Riegennotenblätter erstellen](notenblatter_riegennotenblatter_erstellen.md) (Druck)
* [Wettkampf-Modus einschalten](../wettkampf-durchfuhrung/wettkampf-modus.md) und [Wettkampf im Netz bereitstellen](../wettkampf-durchfuhrung/wettkampf-netzwerk.md)
* [Besten-Listen für die Durchsage nach Gerätewechsel](../wettkampf-durchfuhrung/besten-listen_fur_die_durchsage_nach_geratewechsel.md)
* [Resultat-Analysen](../resultatanalysen/README.md)
* [Bodenmusik katalogisieren](bodenmusik.md) und Bodenmusik-Player
* CSV-/Excel-Import von Anmeldungen
