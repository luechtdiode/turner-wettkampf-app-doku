# Startreihenfolge in den Geräte-Riegen

Bei der Startreihenfolge in den Geräte-Riegen ist darauf zu achten, dass nicht immer der selbe Verein resp. der selbe Turner am Startgerät als Erster beginnen muss.

Innerhalb des Wettkampfes ist eine Standard-Rotation sichergestellt, so dass von Gerät zu Gerät der letzte beim nächsten Gerät als Erster startet.

Bei mehreren Wettkämpfen, die in einer Saison geturnt werden, kann mit sogenannten Riegen Rotationsregeln sichergestellt werden, dass auch wettkampf-übergreifend eine Rotation stattfindet.

## Bisherige Überlegungen

Traditionell werden sogenannte Startnummern bei der Anmeldung vergeben. Diese können dann vom Organisator auf Wunsch oder im eigenen Ermessen ausgetauscht werden. Über die Startnummer wird dann die initiale Reihenfolge festgelegt. Dieser Ansatz kann sehr gut ohne EDV angewendet werden, ist jedoch nicht agil, wenn kurz vor dem Wettkampf Abmeldungen, Umteilungswünsche, Neuanmeldungen etc. berücksichtigt werden sollen. Bereits ausgedruckte Listen müssen von Hand korrigiert oder neu ausgedruckt werden.

In einer EDV gestützten Anwendung ist eine manuelle Sortierung komplexer, als man zunächst vermutet. Auch wenn nicht alles ausgedruckt wird, muss dennoch sichergestellt werden, dass im Zusammenhang mit bestehenden Funktionen wie dezentrale und zentrale Riegenerfassung, An-/Abmeldungen bis zum Wettkampf-Tag mit automatischer Einteilungs-Nachführung etc. immer noch konsistent funktioniert.
Zudem garantiert eine manuelle Sortierung nicht, dass die Reihenfolge dann "gerecht" ist und führt bei grösseren Teilnehmerzahlen zu hohem administrativ Aufwand.

Die aktuelle Lösung verfolgt deshalb den rein regelbasierten Ansatz, wobei die anzuwendenden Regeln vom Organisator zusammengestellt werden können.

## Regelset

Der Wettkampforganisator kann bestimmen, nach welcher Rotationsregel die Startreihenfolge in den Geräteriegen berechnet werden soll. Es macht Sinn, in einer Wettkampf-Saison in allen Wettkämpfen dieselbe Regelkonfiguration zu verwenden.

### Vereinsname (normalisiert)

_Code_: `Verein`

Vereinsnamen werden vor der Sortierung um die vorangestestellen Vereinsart-Bezeichnungen bereinigt (BTV, DTV, STV, GETU, TSV, TV und TZ).
Es wird z.B. aus `TV Aarau` `Aarau`

### Alter aufsteigend mit Altersbegrenzung

_Code_: `AlterAufsteigend`

Wenn das Alter am Wettkampf 16+ ist, spielt der Jahrgang keine Rolle mehr für die Reihenfolge. Ansonsten starten **Jüngere vor Älteren**.

### Alter absteigend mit Altersbegrenzung

_Code_: `AlterAbsteigend`

Wenn das Alter am Wettkampf 16+ ist, spielt der Jahrgang keine Rolle mehr für die Reihenfolge. Ansonsten starten **Ältere vor Jüngeren**.

### Name

_Code_: `Name`

Es wird der Name des Turners/der Turnerin für die Sortierung verwendet.

### Vorname

_Code_: `Vorname`

Es wird der Vorname des Turners/der Turnerin für die Sortierung verwendet.

### Geschlecht

_Code_: `Geschlecht`

Es wird das Geschlecht des Turners/der Turnerin für die Sortierung verwendet.

### Alternierend Invertiert

_Code_: `AltInvers`

Wenn der aktuelle Tag im Jahr durch 2 teilbar ist, dann werden alphabetische Reihenfolgen umgekehrt. 

Es wird z.B. aus `Aarau` `uaraA`. Werte die rein numerisch sind, werden nicht invertiert. Z.B. wird der Jahrgang `2024` so belassen.

Dies macht die Regel auf allen voran ermittelten Sortierkriterien. Die Regel kann deshalb nicht alleine verwendet werden. Es muss zwingend zuvor mindestens eine Regel stehen, welche ein Sortierkriterium extrahiert.

### Verschiebende Rotation

_Code_: `Rotierend`

Die Alphabetische Sortierung verschiebt den Anfangsbuchstaben im Alphabet pro Tag um 1 Zeichen (rotierend). Gross-/Kleinbuchstaben werden nicht mehr differenziert.

Es wird z.B. aus dem Namen `Alvarez` mit 1 Zeichen verschoben in den Sortierbegriff `BMWBSFA` umgewandelt, weil `A`+1 = `B`, ... `Z`+1 = `A`.

Dies macht die Regel auf allen voran ermittelten Sortierkriterien. Die Regel kann deshalb nicht alleine verwendet werden. Es muss zwingend zuvor mindestens eine Regel stehen, welche ein Sortierkriterium extrahiert.

## Gliederungsmöglichkeiten der Rotationsregeln

Die Regeln können mit dem entspr. _Code_ hintereinander gereiht werden.

### Legende

* `[]` in eckigen Klammern sind optionale Bestandteile. Die eckigen Klammern selbst kommen in der Formel nicht zum Einsatz.
* `<>` in spitzen Klammern sind variable Bestandteile. Der darin vermerkte Text entspricht dem Code der Regel. Die spitzen Klammern selbst kommen in der Formel nicht zum Einsatz.
* `...` mit 3 Punkten wird die Fortsetzung einer Reihe angedeutet (verkettung von Elementen). Die Punkte werden in der konkreten Formel nicht verwendet.
* `/` mit Slash werden die ganze Regel-Elemente verkettet.

### Aufbau
_Syntax_: `<Regel1>[/<Regel2>/ ...]`.

### Beispiele

Die `Einfach` Regel, welche der voreingestellten Sortierung entspricht, setzt intern folgende Regeln um:

Formel: `Kategorie/Verein/AlterAbsteigend/Geschlecht/Name/Vorname`

