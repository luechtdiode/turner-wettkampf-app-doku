## Riegeneinteilung erstellen {#riegeneinteilung-erstellen}

Die Riegeneinteilung soll helfen, die Turner in möglichst homogenen und gleichmässig grossen Geräteriegen einzuteilen und diese auf Durchgänge zu verteilen. In der angezeigten Liste werden die Durchgänge mit den zugeteilten Riegen inklusive Statistikwerten über Summe, kleinste, grösste Riege und die Durchschnittsgrösse einer Riege angezeigt. Aus diesen Werten liesse sich auch in etwa errechnen, wie lange ein Durchgang dauern sollte (jeweils die grösste Geräteriege mal Anzahl gerätespezifische Durchlaufzeiten):

![](/assets/suggest-riegen-planning.png)

1.  `Riegen- & Durchgänge frisch einteilen`: Es werden pro Geschlecht, Kategorie und Verein jeweils eine Riege erstellt. Diese bildet die kleinste verschiebbare Einheit für die Zuweisung auf ein Startgerät in einem Durchgang. Die Funktion kennt momentan nur einen Parameter: Die maximale Gruppengrösse. Sie wird mit 11 vorbelegt und kann vom Benutzer individuell angepasst werden. Danach werden die Gruppen so verteilt, dass pro Durchgang möglichst gleichgrosse Geräteriegen existieren und dass Riegen von einem Verein möglichst zusammenbleiben (z.B. Turner und Turnerinnen). Danach können die Zuteilungen in der oberen Liste beliebig verändert werden.
2.  `Einteilung von Riegen & Durchgängen zurücksetzen`: Es werden alle Riegen- und Durchgangs- und Startgeräte-Einteilungen zurückgesetzt.

Wenn mindestens ein Durchgang (Multiselektion mittels `CTRL+linke Maustaste` oder `SHIFT+linke Maustaste` erweitern) in der Liste selektiert ist, können darauf diverse Überarbeitungsfunktionen angewendet werden:

![](/assets/edit-riegen-planning.png)

1.  <img align="right" src="../assets/durchgang-partiell-neuverteilen.png" width="30%">`Durchgang neu einteilen`: Die selektierten Durchgänge können mit angepassten Parameter neu eingeteilt werden. 
    Die nicht selektierten Durchgänge werden dabei nicht verändert.<br/>
    Im Dialog werden die neuen Parameter angegeben. Siehe [Details zu Durchgang neu einteilen](./durchgang-neu-einteilen.md)
2.  `Durchgänge zusammenlegen`: Wenn mindestens zwei Durchgänge selektiert sind, dann können diese mit dieser Funktion zusammengelegt werden. Die Turner-/Innen bleiben dabei bei ihrem eingeteilten Startgerät. Für den zusammengelegten Durchgang kann eine neue Bezeichnung gewählt werden.
3.  `Durchgang umbenennen`: Wenn genau ein Durchgang selektiert ist, dann kann diesem hiermit ein neuer Name vergeben werden. Sollte dabei ein bereits existierender Name vergeben werden, so kommt dies einer Durchgangs-Zusammenlegung gleich.
4.  `In anderen Durchgang verschieben`: Wenn genau ein Durchgang selektiert ist, dann können zugeteilte Riegen in andere Durchgänge verschoben werden. Es klappt ein Untermenü mit allen Riegennamen aus dem Durchgang auf. Die kleinste Riege ist zu oberst, die grösste zu unterst. Wird eine Riege ausgewählt kann im weiteren Untermenü der Ziel-Durchgang ausgewählt werden.
5.  `Auf anderes Startgerät verschieben`: Wenn genau ein Durchgang selektiert ist, dann können zugeteilte Riegen in eine andere Startgerät-Riege verschoben werden. Es klappt ein Untermenü mit allen Riegennamen aus dem Durchgang auf. Die kleinste Riege ist zu oberst, die grösste zu unterst. Wird eine Riege ausgewählt kann im weiteren Untermenü der Ziel-Startgeräteriege ausgewählt werden. Die Ziel-Startgeräteriegen sind mit ihrer aktuellen Grösse gekennzeichnet.

## Zusammenfassen von Durchgängen zu einer Durchgang-Gruppe

Bei der Wettkampfdurchführung können Durchgägne parallel durchgeführt werden. Mit dieser Funktion lassen sich solche parallel durchgeführten Durchgänge mit der funktion `Durchgänge in Gruppen zusammenfassen ...` zusammenfassen.
Die Zeitangaben auf der Durchgang-Gruppe entspricht dann immer der Zeit, die beim "langsamsten" Durchgang in der Gruppe berechnet wurde.

![Durchgang gruppieren](/assets/durchgang-gruppieren.png)

![Durchganggruppe bezeichnen](/assets/name-durchganggruppe.png)

![Gruppierte Durchgänge](/assets/gruppierte-durchgaenge.png)


## Drag & Drop Unterstützung bei der Durchgang-Planung

Die Riegen können auch mittels Drag & Drop auf ein anderes Startgerät oder in einen anderen Durchgang verschoben werden:

`Riege auf anderes Startgerät verschieben`

![Riegen & Durchgänge Einteilung nachbearbeiten](/assets/drag-drop-startgeraetriege.gif)

`Riege in anderen Durchgang verschieben`

![Riegen & Durchgänge Einteilung nachbearbeiten](/assets/drag-drop-durchg.gif)

Mit gruppierten Durchgängen ist darauf zu achten, dass beim Fallenlassen (drop) der Riege die Durchgang-Gruppe aufgeklappt ist. Auf zugegklappte Durchgangs-Gruppen kann keine Riege zugeteilt werden.

### Export-Funktionen
<img align="right" src="../assets/riegen-export-funktionen.png">

1.  `Riegen Einheiten export`: Das Resultat, welches die Riegen-Einteilenfunktion für sich zum Starten erstellt (die Riegen pro Geschlecht, Kategorie und Verein) kann in einer CSV-Datei zur weiteren Verarbeitung im Excel exportiert werden.
2.  `Durchgang-Planung export`: Mit dieser Funktion lässt sich die Durchgangsplanung in eine CSV-Datei exportieren. So lässt sich die Einteilung, die initial von der App gemacht wurde, ev. einfacher oder übersichtlicher im Excel nachbearbeiten.
3.  `Riegenblätter erstellen`: Mit dieser Funktion lassen sich alle Riegenblätter erstellen. Die Riegenblätter sind Notenblätter pro Geräte-Riege. Sie werden pro Gerät und Riege erstellt und beinhalten alle Turner-/Innen der Riege. Diese werden nach jedem Gerätewechsel von den Wertungsrichtern eingesammelt, so dass die Resultate schon frühzeitig im Rechnungsbüro erfasst werden können.

### Mustervorgehen

* [Mustervorgehen für Athletiktest-Riegeneinteilung](/wettkampf-vorbereitung/riegeneinteilung_erstellen_mustervorgehen_att.md)
* [Mustervorgehen für KuTu-Riegeneinteilung](/wettkampf-vorbereitung/riegeneinteilung_erstellen_mustervorgehen_kutu.md)
* [Mustervorgehen für GeTu-Riegeneinteilung](/wettkampf-vorbereitung/riegeneinteilung_erstellen_mustervorgehen_getu.md)
