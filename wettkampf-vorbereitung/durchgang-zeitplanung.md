## Durchgang-Zeitplanung

Für die Planung der Durchgänge sind dessen Durchlaufzeiten entscheidend. Die App kann diese anhand vorgegebenen Zeit-Bestandteilen pro Programm/Kategorie und Gerät, sowie der momentan im Durchgang zugewiesenen Riegen-Grössen berechnen.

Im `Planzeiten`-Tab (1) innerhalb der Riegeneinteilung lassen sich alle Zeitbestandteile auflisten und bearbeiten:
![](/assets/planzeiten.png)

Zeit-Bestandteil | Beschreibung 
----------------:|:-------------
Wechsel (2)      | Zeitbedarf pro Teilnehmer für den Gerätewechsel
Einturnen (3)    | Zeitbedarf pro Teilnehmer für Einturnen am Gerät
Übung (4)        | Zeitbedarf pro Teilnehmer für das Turnen der Übung
Wertung (5)      | Zeitbedarf pro Teilnehmer für die Bewertung der Übung

### Standard-Vorbelegungen (Zeitangaben in Sekunden)

|Wettkampf-Art|Wechsel|Einturnen|Übung|Wertung|
|-|-:|-:|-:|-:|
|GeTu|30''|30''|K1-K4: 40'', ab K5: 50''|K1-K4: 40'', ab K5: 50''|
|KuTu|30''|30''|60''|60''|
|KuTuri|30''|30''|60''|60''|
|Athletiktest|30''|30''|50''|50''|


### Verwendung der Planzeiten bei der Durchgangsplanung

Im `Durchgänge`-Tab wird der hochgerechnete Zeitbedarf angezeigt. Ein verschieben der Riegenzuteilungen kann zur Folge haben, dass sich diese Zeit verändert. Die Zeiten werden dann am geringsten, wenn die Riegenverteilung möglichst gleichmässig erfolgt. Wenn es z.B. eine grosse Geräte-Riege gibt, bestimmt diese normalerweise den Zeitbedarf für den ganzen Durchgang. Verschiebungen bei den kleineren Geräteriegen haben dann keinen Einfluss auf die Gesammt-Durchgangszeit.

![](/assets/durchgang-zeitbedarf.png)

Zeitbedarf-Bestandteil | Beschreibung 
----------------------:|:-------------
Tot                    | Zeitbedarf für den ganzen Durchgang
Eint                   | Zeitbedarf für das Einturnen pro Gerätewechsel (für alle Teilnehmer einer Geräteriege zusammengefasst)
Gerät                  | Zeitbedarf für für das Turnen der Übungen pro Gerät (für alle Teilnehmer einer Geräteriege zusammengefasst)
Nicht angegeben<br>(in Tot enthalten) | Zeitbedarf für den Gerätewechsel

### Verwendung der Planzeiten bei der Wettkampf-Durchführung im Netzwerk-Dashboard

Die Plandauer eines Durchganges wird auch im Netzwerk-Dashboard angezeigt. Neben der Start-, Ende- und Dauer-Anzeige dient dies nicht zuletzt auch der Kontrolle, ob die Planzeiten korrekt eingeschätzt worden sind. Bei wiederholt grösseren Abweichungen sollten die Planzeiten justiert werden.

![](/assets/planzeiten-netzwerkdashboard.png)