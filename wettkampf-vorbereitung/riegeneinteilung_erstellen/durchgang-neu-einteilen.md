# Details zu Durchgang neu einteilen

Die selektierten Durchgänge können mit angepassten Parameter neu eingeteilt werden. Die nicht selektierten Durchgänge
werden dabei nicht verändert. Bisherige Geräte-Zuweisungen werden vorbelegt.

In der [Admin-Web-App](../webadmin.md) werden dazu in der [Riegeneinteilung](README.md) die gewünschten Durchgänge 
selektiert und `Neu generieren` gewählt. Die Parameter entsprechen den Optionen der Einteilungs-Funktion.

In der Desktop-App erscheint dazu folgender Dialog:

![](/assets/getu-durchgang-partial-replanning-options.png)

| Funktion | Beschreibung |
| :--- | :--- |
| Maximale Gruppengrösse | Limitieren oder erweitern, was zu mehr oder weniger Durchgängen führen kann. Mit dem Wert `0` ist die Gruppengrösse unlimitiert. |
| Max. parallele Durchgänge pro Durchganggruppe | Steuern ob und wieviele parallele Durchgänge in einer Abteilung betrieben werden sollen, sofern aufgrund der Anzahl Teilnehmenden und der Maximal-Anzahl der Riegengruppengrösse ein Druchgang nicht ausreicht und die Geräteriegen auf mehreren Durchgängen verteilt werden müssen. Mit dem Wert `0` werden keine Durchgangsgruppen gebildet und die zusätzlichen Durchgänge werden normal neben allen anderen Durchgängen eingegliedert. |
| Geschlechter-Trennung | Bei `gemischte Geräteriegen` werden geschlecht-gemischte Riegen erstellt. Bei `gemischter Durchgang` werden Riegen ohne Geschlechts-Durchmischung erstellt, innerhalb eines Durchganges werden jedoch Riegen beider Geschlechter eingeteilt. Bei `getrennte Durchgänge` werden Durchgänge ohne Geschlechts-Durchmischung erstellt. Mit `automatisch` entscheidet das Programm anhand der Geräte-Geschlechtszuordnungsregel, ob in einem Durchgang die Geschlechter getrennt werden sollen. Wenn beide Geschlechter dieselben Geräte turnen, wird `gemischte Geräteriegen` verwendet, ansonste `getrennte Durchgänge`. |
| Programme / Kategorien teilen | Wenn diese Option aktiviert ist, dann gibt es pro Programm/Kategorie eigene Durchgänge. Im deaktivierten Zustand können Programme/Kategorien in einem Durchgang gemischt werden. |
| Verteilung auf Diszipline | Einzelne `Geräte` im Durchgang `ausschliessen` oder mit `einschliessen`, was zu grösseren oder kleineren Gruppen führt und dadurch ev. mehr oder weniger Durchgängen. |

