## Riegeneinteilung erstellen {#riegeneinteilung-erstellen}

»Siehe auch: Ausnahmen, Limitationen, Seite 22

Die Riegeneinteilung soll helfen, die Turner in möglichst homogenen und gleichmässig grossen Geräteriegen einzuteilen und diese auf Durchgänge zu verteilen. In der angezeigten Liste werden die Durchgänge mit den zugeteilten Riegen inklusive Statistikwerten über Summe, kleinste, grösste Riege und die Durchschnittsgrösse einer Riege angezeigt. Aus diesen Werten liesse sich auch in etwa errechnen, wie lange ein Durchgang dauern sollte (jeweils die grösste Geräteriege mal Anzahl Gerätespezifische Durchlaufzeiten).:

1.  Riegen einteilen: Es werden pro Geschlecht, Kategorie und Verein jeweils eine Riege erstellt. Diese bildet die kleinste verschiebbare Einheit für die Zuweisung auf ein Startgerät in einem Durchgang. Die Funktion kennt momentan nur einen Parameter: Die maximale Gruppengrösse. Sie wird mit 11 vorbelegt und kann vom Benutzer individuell angepasst werden. Danach werden die Gruppen so verteilt, dass pro Durchgang möglichst gleichgrosse Geräteriegen existieren und dass Riegen von einem Verein möglichst zusammenbleiben (z.B. Turner und Turnerinnen). Danach können die Zuteilungen in der oberen Liste beliebig verändert werden.
2.  Das Resultat, welches die Riegen-Einteilenfunktion für sich zum Starten erstellt (die Riegen pro Geschlecht, Kategorie und Verein) kann in einer CSV-Datei zur weiteren Verarbeitung im Excel exportiert werden.
3.  Wenn mindestens ein Durchgang (Multiselektion mittels CTRL+linke Maustaste oder SHIFT+linke Maustaste erweitern) in der Liste selektiert ist, können darauf diverse Überarbeitungsfunktionen angewendet werden.

Die selektierten Durchgänge können mit angepassten Parameter neu eingeteilt werden. Die nicht selektierten Durchgänge werden dabei nicht verändert.

1.  Wenn mindestens zwei Durchgänge selektiert sind, dann können diese mit dieser Funktion zusammengelegt werden. Die Turner-/Innen bleiben dabei bei ihrem eingeteilten Startgerät. Für den zusammengelegten Durchgang kann eine neue Bezeichnung gewählt werden.
2.  Wenn genau ein Durchgang selektiert ist, dann kann diesem hiermit ein neuer Name vergeben werden. Sollte dabei ein bereits existierender Name vergeben werden, so kommt dies einer Durchgangs-Zusammenlegung gleich.
3.  Wenn genau ein Durchgang selektiert ist, dann können zugeteilte Riegen in andere Durchgänge verschoben werden. Es klappt ein Untermenü mit allen Riegennamen aus dem Durchgang auf. Die kleinste Riege ist zu oberst, die grösste zu unterst. Wird eine Riege ausgewählt kann im weiteren Untermenü der Ziel-Durchgang ausgewählt werden.
4.  Wenn genau ein Durchgang selektiert ist, dann können zugeteilte Riegen in eine andere Startgerät-Riege verschoben werden. Es klappt ein Untermenü mit allen Riegennamen aus dem Durchgang auf. Die kleinste Riege ist zu oberst, die grösste zu unterst. Wird eine Riege ausgewählt kann im weiteren Untermenü der Ziel-Startgeräteriege ausgewählt werden. Die Ziel-Startgeräteriegen sind mit ihrer aktuellen Grösse gekennzeichnet.
5.  Mit dieser Funktion lässt sich der gesamte Inhalt der Liste in eine CSV-Datei exportieren. So lässt sich die Einteilung, die initial von der App gemacht wurde, ev. einfacher oder übersichtlicher im Excel nachbearbeiten.
6.  Mit dieser Funktion lassen sich alle Riegenblätter erstellen. Die Riegenblätter sind Notenblätter pro Geräte-Riege. Sie werden pro Gerät und Riege erstellt und beinhalten alle Turner-/Innen der Riege. Diese werden nach jedem Gerätewechsel von den Kampfrichtern eingesammelt, so dass die Resultate schon frühzeitig im Rechnungsbüro erfasst werden können.

### Mustervorgehen für Athletiktest-Riegenverteilung {#mustervorgehen-f-r-athletiktest-riegenverteilung}

Für einen Athletiktest gibt es in der Regel die Rangierung pro Jahrgang. Die initiale Riegenaufteilung wird mit dem Button &quot;Riegen einteilen&quot; eingeleitet.

Diese Funktion gruppiert primär nach Geschlecht und nach Jahrgang. Zu grosse Gruppen werden gesplittet, so dass eine pro Stationen im Durchgang gleichmässige Verteilung möglich wird. Wenn wie im Beispiel die Vorbelegung mit 0 verwendet wird, so werden für den Athletiktest standardmässig zwei Durchgänge eingerichtet. Die Gruppengrössen ergeben sich dadurch von selbst:

1.  Beweglichkeits-Stationen
2.  Kraft-Stationen

Danach können folgende Kriterien in die Verteilung eingearbeitet werden:

*   Maximale Gruppengrösse limitieren, was zu mehr Durchgängen führen kann.
*   Geschlechter in eigene Durchgänge trennen, was zu einer Verdoppelung der Durchgänge führt.

Zum Schluss können einzelne Einteilungen von Hand verschoben werden:

### Mustervorgehen für KuTu-Riegenverteilung {#mustervorgehen-f-r-kutu-riegenverteilung}

Die KuTu oder KuTuri Riegenverteilung verteilt standardmässig mit einer Gruppengrösse von maximal 11 Turner/-Innen pro Startgerät:

Danach kann es pro Programm mehrere Durchgänge geben:

Diese können mit folgenden Kriterien einzeln oder mit Multiselection auf mehreren Durchgängen neu verteilt werden:

*   Maximale Gruppengrösse limitieren, was zu mehr oder weniger Durchgängen führen kann.
*   Programme zusammenfassen (indem sie nicht aufgeteilt werden).
*   Einzelne Geräte im Durchgang ausschliessen, was zu grösseren Gruppen führt und dadurch ev. mehr Durchgängen.
*   Die Aufteilung auf Geschlechts-Ebene macht in diesem Programm keinen Sinn, weil ein KuTuri-Wettkampf nur Turnerinnen kennt, und der KuTu-Wettkampf nur Turner (unterschiedliche Gerät-Zusammensetzung).

Zum Schluss können einzelne Einteilungen von Hand verschoben werden:

### Mustervorgehen für GeTu-Riegenverteilung {#mustervorgehen-f-r-getu-riegenverteilung}

Die Getu Riegenverteilung verteilt standardmässig mit einer Gruppengrösse von maximal 11 Turner/-Innen pro Startgerät. Es werden alle Geräte ausser dem Barren für die Verteilung verwendet:

Danach kann es pro Kategorie mehrere Durchgänge geben:

Diese können mit folgenden Kriterien einzeln oder mit Multiselection auf mehreren Durchgängen neu verteilt werden:

*   Maximale Gruppengrösse limitieren oder erweitern, was zu mehr oder weniger Durchgängen führen kann.
*   Programme zusammenfassen (indem sie nicht aufgeteilt werden).
*   Einzelne Geräte im Durchgang ausschliessen oder mit einschliessen (Barren), was zu grösseren oder kleineren Gruppen führt und dadurch ev. mehr oder weniger Durchgängen.

Die Aufteilung auf Geschlechts-Ebene kann helfen, die Turner in einen separaten Durchgang zu ziehen, in welchem dann z.B. auch Barren verwendet wird.

Zum Schluss können einzelne Einteilungen von Hand verschoben werden:

Im GeTu ist es bei geschlechts-gemischten Durchgängen üblich, dass die Barren-Station am Ende eines Durchgangs für alle Turner aus dem Durchgang durchgeführt wird. Diese Einteilung lässt sich mit folgendem Trick erreichen:

Schritt 1: Markieren aller Turner-Riegen (alle mit einem M am Riegen-Namensanfang):

Danach den &quot;2\. Riege&quot; -Button benutzen:

und schliesslich die Barren-Riege benennen:

In der Riegeneinteilung wird nun diese Barren K1 Riege mit aufgelistet. Jetzt muss nur noch der Durchgang und das Startgerät (Barren) verknüpft werden:

Das Ergebnis davon lässt sich auch in der Durchgang-Ansicht anzeigen:

Mit dem &quot;Riegenblätter-Erstellen&quot; Button werden somit auch Riegenblätter für das Barren-Gerät generiert - und bei der Resultaterfassung kann damit gefiltert werden:

Zum Schluss macht es Sinn, die Durchgänge für die Erkennung der chronologische Zugehörigkeit so zu benennen, dass es auch für die Turner und Betreuer verständlich wird, wie diese Einteilung zu verstehen ist:

### Ausnahmen, Limitationen {#ausnahmen-limitationen}

Wenn in einem Durchgang Kategorien/Programme gemischt werden, wird die Erfassung in der App dabei erschwert, weil in der App die Resultate strikt pro Kategorie/Programm erfasst werden müssen. Es kann also beim Erfassen der Resultate nicht einmal pro Riegen-Notenblatt der Filter mit den Turner/-Innen eingestellt und dann die Resultate von oben nach unten erfasst werden, weil die Turner/-Innen aus den anderen Kategorien/Programmen nicht angezeigt werden. Um die Erfassung dennoch zu erleichtern, wird zu diesem Zweck werden auf den Riegen-Notenblätter pro Turner/-In auch dessen Kategorie-/Programmeinteilung aufgedruckt. Dies soll dabei unterstützen, alle Resultate einer Kategorie/eines Programmes in einem Erfassungsdurchgang aus dem Riegen-Notenblatt heraussuchen zu können.Einteilung gemäss Durchgangs-Planung: Gemischte Riege mit K3, K6 und K7 Turnern am Barren.Gegenüber den Listen für die Resultaterfassung pro Kategorie/Programm:

Wenn in einem Durchgang nicht alle benötigten Geräte mit einer Riege als Startgerät verknüpft werden (weil es z.B. nicht genügend Riegen gibt), dann kann die App nicht erkennen, welche Geräte ausser den als Startgerät verknüpften im Durchgang wirklich geturnt werden sollen.Es macht also ein Turnus mit allen als Startgerät verknüpften Geräten (grün) und die restlichen (rot) werden ignoriert. In solchen Fällen wäre es besser, die Erfassung mit Notenblätter pro Turner durchzuführen, oder aber dass der Durchgang mit weiteren Kategorien zusammengefasst wird, so dass es für alle notwendigen Geräte auch eine Start-Riege geben kann.