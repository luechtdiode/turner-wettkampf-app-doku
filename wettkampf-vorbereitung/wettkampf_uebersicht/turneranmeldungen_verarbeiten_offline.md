# Turneranmeldungen offline verarbeiten

Die Turneranmeldungen kommen normalerweise via Excel-Listen von den Vereinen zugesendet.

Die dort gespeicherten Turner/-Innen Daten können per Copy/Paste aus dem Excel übernommen werden und in dem gewünschten Wettkampf in der App eingefügt werden.

Hierbei müssen folgende Punkte beachtet werden:

|  |  |
| :--- | :--- |
| 1. Der Verein der Turneranmeldungen muss bereits in der App erfasst sein. Sollte dies nicht der Fall sein, muss der Verein zuerst erfasst werden \(siehe [Verein anlegen](https://github.com/luechtdiode/turner-wettkampf-app-doku/tree/4c6a6466d07aa1a687e295023b6e4be4812c7928/stammdatenpflege/stammdatenpflege/verein_anlegen.md)\). | 2. Die Daten im Excel müssen zuvor manuell kontrolliert werden: `Namen` / `Vornamen` in der richtigen Spalte, `Geburtsdatum` im Format `TT.MM.JJJJ` erfasst, `Kategorie-Zuweisung` mit reinen Zahlen \(z.B. 3 für K3\), `Geschlecht` mit `X` in der richtigen Spalte \(`Ti`, `Tu`\) gekennzeichnet? |
| 3. Danach kann der ganze Block der Turner/-Innen Daten markiert und kopiert werden: | ![Turner importieren - copy&amp;paste von Excel](/assets/copy-paste-from-excel.png) |
| 4. Anschliessend können die Daten in der App auf dem gewünschten Wettkampf eingefügt werden \(Button "`Aus Excel einfügen ...`" betätigen\):  | ![Wettkampf exportieren Popup-Menu](/assets/paste-from-excel-2.png) |
| 5. An diesem Punkt kann noch einmal verifiziert werden, ob alle Turner/-Innen richtig identifiziert wurden und ob der Verein richtig ausgewählt wurde. Der Verein wird nur dann automatisch ausgewählt, wenn mind. ein\(e\) Turner/In aus einem Verein bereits in der lokalen Datenbank erkannt wird und so die | Vereinszugehörigkeit implizit für alle gesetzt wird. Sollten nicht alle Turner der Liste aus dem gleichen Verein stammen, können einzelne Turner in der Liste angewählt werden und mit "`OK`" zum oben eingestellten Verein importiert werden. Die Kategorie-Zuteilung findet automatisch statt. |
| 6. Sollte kein Excel-Sheet mit Anmeldedaten vorhanden sein, kann mit der Funktion "`Athlet hinzufügen`" ein\(e\) Turner/In aus der Datenbank ausgewählt oder neu erfasst werden. | ![](/assets/athlet-hinzufuegen.png) |

