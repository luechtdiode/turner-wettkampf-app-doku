# Teamregeln

Mit den Teamregeln lassen sich Regeln aufstellen, wie sich die Teams im Wettkampf 
zusammenstellen.

## Zusammenstellung der Teams

Grundsätzlich kann bei jedem Teilehmer oder Teilnehmerin eine Teamnummer erfasst werden.
Die Nummer kann als Teamnummer auf Vereins- oder Verbands-Ebene gesehen werden.
Zudem gilt sie normalerweise pro Programm/Kategorie und Geschlecht.

Bei einer Turnerin im K3 wirkt sich dann die Teamnummer z.B. so aus, dass
sie mit anderen Turnerinnen aus K3 und aus dem selben Verein mit der selben Teamnummer 
zu einem Team zusammengestellt wird.

Wenn es zu wenige Telnehmer/-Innen für eine Teamzusammenstellung innerhalb der
Geschlechts- und Programm/Kategorie-Gruppierung ergeben, lassen sich die
Teams in der Ranglisten-Konfiguration auch Geschlechts- und/oder Programm/Kategorie übergreifend
zusammenstellen.

Über die Filter- und Gruppierungsfunktionen der Rangliste lassen sich beliebig weitere
Kombinationen erreichen.

## Berechnung der Teamwertung

Es gibt aktuell folgende Formeln, die für die Team-Gesamtwertung verwendet werden können:

1. Die besten n Gesamtwertungen werden zur Teamwertung zusammenaddiert.
2. Die besten n Geräte Einzelwertungen werden zur Teamwertung zusammenaddiert.

### Besten n Gesamtwertungen

Aus einem Team werden die n besten Gesamtwertungen für das Teamresultat verwendet.

### Besten n Gerätewertungen

Aus einem Team werden die n besten Wertungen pro Gerät herangezogen, um das Teamresultat zu berechnen.

## Regel-Syntax

### Legende

* `[]` in eckien Klammern sind optionale Bestandteile. Die eckigen Klammern selbst kommen in der Formel nicht zum Einsatz.
* `|` Optionale Alternativen. Vor dem `|` Symbol ist z.B. Variante 1 und hinter dem Symbol ist Variante 2. Eine der beiden muss verwendet werden.
* `<>` in spitzen Klammern sind variable Bestandteile. Der darin vermerkte Text entspricht dem Variablennamen. Die spitzen Klammern selbst kommen in der Formel nicht zum Einsatz.
* `*` ein Stern bedeutet unbegrenzt und kann für die Maximalanzahl-Teammitglieder verwendet werden.
* `...` mit 3 Punkten wird die Fortsetzung einer Reihe angedeutet (verkettung von Elementen). Die Punkte werden in der konkreten Formel nicht verwendet.
* `,` mit Komma werden weitere Teamregeln voneinander getrennt.

### Aufbau

`[Verein|Verband][Gerät|Gesamt](<Mindestanzahl-Teammitglieder>/[<Maximalanzahl-Teammitglieder>|*])[,...]`

Die Regel beginnt mit der Abgrenzug auf Vereins- oder Verbandsebene. Darauf folgt direkt anschliessend die Berechnungsmethode, ob auf Gerät oder Gesamtwertungen addiert werden soll.
Danach wird angegeben, wieviele Teilnehmer mindestens ein Team bestücken. Optional kann auch eine Obergrenze definiert werden.


### Beispiele

_Team auf Vereins-Ebene mit den besten 3 Gerätenoten_
`VereinGerät(3/*)`

_Team auf Vereins-Ebene mit den besten 3 Gerätenoten_ mit maximal 4 Teamteilnehmer/-Innen
`VereinGerät(3/4)`

_Team auf Vereins-Ebene mit den besten 3 Gersamtwertungen_
`VereinGesamt(3/*)`

_Team auf Vereins-Ebene mit den besten 3 Gesamtwertungen_ mit maximal 4 Teamteilnehmer/-Innen
`VereinGesamt(3/4)`

_Team auf Verband-Ebene mit den besten 4 Gerätenoten_
`VerbandGerät(4/*)`

_Team auf Verband-Ebene mit den besten 2 Gerätenoten_ mit maximal 4 Teamteilnehmer/-Innen
`VerbandGerät(2/4)`

_Team auf Verband-Ebene mit den besten 3 Gersamtwertungen_
`VerbandGesamt(3/*)`

_Team auf Verband-Ebene mit den besten 3 Gesamtwertungen_ mit maximal 4 Teamteilnehmer/-Innen
`VerbandGesamt(3/4)`

_Teams auf Verband-Ebene mit den besten 3 Gesamtwertungen, sowie Teams auf Vereins-Ebene mit den besten 2 Gerätenoten
`VerbandGesamt(3/*),VereinGerät(2/*)`