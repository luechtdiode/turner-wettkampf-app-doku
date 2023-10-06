# Teams / Mannschaften

## Zusammenstellung der Teams

Grundsätzlich kann bei jedem Teilehmer oder Teilnehmerin eine Teamnummer erfasst werden.
Die Nummer kann als Teamnummer auf Vereins- oder Verbands-Ebene interpretiert werden.
Zudem gilt sie normalerweise pro Programm/Kategorie und Geschlecht.
Wenn Altersklassen definiert wurden, wirken diese ebenfalls als Abgrenzungskriterium.

Bei einer Turnerin im K3 wirkt sich dann die Teamnummer z.B. so aus, dass
sie mit anderen Turnerinnen aus K3 und aus dem selben Verein mit der selben Teamnummer 
zu einem Team zusammengestellt wird.

Wenn es zu wenige Telnehmer/-Innen für eine Teamzusammenstellung innerhalb der
Geschlechts- und Programm/Kategorie/Altersklasse-Gruppierung ergeben, lassen sich die
Teams in der Ranglisten-Konfiguration auch Geschlechts- und/oder Programm/Kategorie/Altersklasse übergreifend
zusammenstellen.

Über die Filter- und Gruppierungsfunktionen der Rangliste lassen sich beliebig weitere
Kombinationen erreichen.

### Erfassung im Online Registrierungs-Formular

![](/assets/team-assignement-online-reg.png)

### Erfassung in der Wettkampf-App

![](/assets/team-assignements-column.png)

### Aktion für Synchronisierung Online-Registrierung zur Wettkampf-Einteilung

![](/assets/team-snc.png)

## Berechnung der Teamwertung

Es gibt aktuell folgende Formeln, die für die Team-Gesamtwertung verwendet werden können:

1. Die besten n Gesamtwertungen werden zur Teamwertung zusammenaddiert.
2. Die besten n Geräte Einzelwertungen werden zur Teamwertung zusammenaddiert.

### Besten n Gesamtwertungen

Aus einem Team werden die n besten Gesamtwertungen für das Teamresultat verwendet.

### Besten n Gerätewertungen

Aus einem Team werden die n besten Wertungen pro Gerät herangezogen, um das Teamresultat zu berechnen.

## Erfassung der Team-Regel(n)

Mit den Teamregeln lassen sich Regeln aufstellen, wie sich die Teams im Wettkampf 
zusammenstellen.

Die Regeln für die Teamzusammenstellung müssen im Wettkampf-Bearbeiten Dialog vorgenommen werden.
»Siehe auch: [Wettkampf anlegen](../../stammdatenpflege/wettkampf_anlegen.md)

![](/assets/team-define.png)

## Regel-Syntax

### Legende

* `[]` in eckigen Klammern sind `optionale Bestandteile`. Die eckigen Klammern selbst kommen in der Formel nicht zum Einsatz.
* `|` Optionale `Alternativen`. Vor dem `|` Symbol ist z.B. Variante 1 und hinter dem Symbol ist Variante 2. Eine der beiden muss verwendet werden.
* `<>` in spitzen Klammern sind variable Bestandteile. Der darin vermerkte Text entspricht dem `Variablennamen`. Die spitzen Klammern selbst kommen in der Formel nicht zum Einsatz.
* `*` ein Stern bedeutet `unbegrenzt` und kann für die Maximalanzahl-Teammitglieder verwendet werden.
* `...` mit 3 Punkten wird die `Fortsetzung einer Reihe` angedeutet (verkettung von Elementen). Die Punkte werden in der konkreten Formel nicht verwendet.
* `,` mit Komma werden weitere `Teamregeln` voneinander getrennt.
* `+` mit Plus werden mehrere `mixed Teams` voneinander getrennt.

### Aufbau

`[Verein|Verband][Gerät|Gesamt](<Mindestanzahl-Teammitglieder>/[<Maximalanzahl-Teammitglieder>|*][/<Mixed Team1>[+<Mixed Team n>...]])[,...]`

1) Die Regel beginnt mit der **Abgrenzug** auf `Verein`s- oder `Verband`s-Ebene.
2) Anschliessend folgt die **Berechnungsmethode**, ob die Punkte auf `Gerät` oder `Gesamtwertungen` addiert werden sollen.
3) Danach wird in der runden Klammerung angegeben,
    * wieviele `Teilnehmer mindestens` ein Team bestücken. 
    * _Optional_ kann auch eine `Obergrenze` definiert werden.
    * _Optional_ können `Teamnamen aufgelistet` werden, die als mixed Teams (Vereinsübergreifend) benutzt werden können.

### Umgang mit explizit erfassten mixed Teams

* Wenn in mehreren TeamRegeln Team-Namen aufgelistet werden, wird daraus eine Gesamtliste erstellt.
* Die mixed Teams in der Gesamtliste bekommen einen Index, über den die Zuweisungen hergestellt werden. Es ist deshalb darauf zu achten, dass einmal aufgelistete Teams nicht mehr in ihrer Position in der Gesamtliste ändern. Wenn also vorne ein Team herausgelöscht wird, stimmen die nachfolgenden Indicies nicht mehr. Atkuell gibt es von der App noch 
keine Unterstützung für stabilere Team-Zuweisungen.
* **Es gilt also grösste Vorsicht bei der nachträglichen Bearbeitung dieser mixed Teams Auflistung. Am sichersten ist es, wenn nur noch neue Teams am Ende einer Liste eingetragen werden**.

### Prioritätsregelung bei gemischten Teamregeln

Wenn eine gemischte Liste von Teamregeln (auf Vereins-Ebend und auf Verbans-Ebene) definiert wird, werden die Teamzuordnungen standardmässig auf Vereins-Ebene gemacht. Die Verbands-Team Zuteilung erfolgt dann ausschliesslich über die explizit definierten mixed Teams.

### Beispiele

_Team auf Vereins-Ebene mit den besten 3 Gerätenoten_
`VereinGerät(3/*)`

_Team auf Vereins-Ebene mit den besten 3 Gerätenoten mit maximal 4 Teamteilnehmer/-Innen_
`VereinGerät(3/4)`

_Team auf Vereins-Ebene mit den besten 3 Gersamtwertungen_
`VereinGesamt(3/*)`

_Team auf Vereins-Ebene mit den besten 3 Gesamtwertungen mit maximal 4 Teamteilnehmer/-Innen_
`VereinGesamt(3/4)`

_Team auf Verband-Ebene mit den besten 4 Gerätenoten_
`VerbandGerät(4/*)`

_Team auf Verband-Ebene mit den besten 2 Gerätenoten mit maximal 4 Teamteilnehmer/-Innen_
`VerbandGerät(2/4)`

_Team auf Verband-Ebene mit den besten 3 Gersamtwertungen_
`VerbandGesamt(3/*)`

_Team auf Verband-Ebene mit den besten 3 Gesamtwertungen mit maximal 4 Teamteilnehmer/-Innen_
`VerbandGesamt(3/4)`

_Teams auf Verband-Ebene mit den besten 3 Gesamtwertungen, sowie Teams auf Vereins-Ebene mit den besten 2 Gerätenoten_
`VerbandGesamt(3/*),VereinGerät(2/*)`

_Teams auf Vereins-Ebene mit den besten 3 Gerätenoten und mit 4 vordefinierten mixed Teams_
`VereinGerät(3/*/Mixed Team 1+Mixed Team 2+Mixed Team 3+Mixed Team 4)`

_Teams auf Vereins-Ebene mit den besten 3 Gerätenoten mit maximal 4 Teamteilnehmer/-Innen und mit 3 vordefinierten mixed Teams_
`VereinGerät(3/4/Mixed Team 1+Mixed Team 2+Mixed Team 3)`