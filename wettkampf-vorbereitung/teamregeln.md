# Teams / Mannschaften

## Erfassung der Team-Regel(n)

Mit den Teamregeln lassen sich Regeln aufstellen, wie sich die Teams im Wettkampf
zusammenstellen.

###  Erfassung der Team-Regel(n) in der Admin-Web-App

Die Regeln für die Teamzusammenstellung werden in der [Admin-Web-App](webadmin.md) in 
der [Anlegen-/Bearbeiten-Maske](wettkampf_anlegen.md) unter `Team-Regel` erfasst oder bearbeitet. 
Über den Editor-Button kann die Regel aus einer Liste von Vorgaben ausgewählt oder individuell zusammengestellt werden:

![](/assets/webadmin-editor-teamregel.png)

»Siehe auch: [Regel Syntax](#regel-syntax) für die individuelle Teamregel Definition

###  Erfassung der Team-Regel(n) in der Desktop-App

Die Regeln für die Teamzusammenstellung müssen im Wettkampf-Bearbeiten Dialog erfasst oder bearbeitet werden.
»Siehe auch: [Wettkampf anlegen](../stammdatenpflege/wettkampf_anlegen.md)

![](/assets/team-define.png)

»Siehe auch: [Regel Syntax](#regel-syntax) für die individuelle Teamregel Definition

## Zusammenstellung der Teams

Sobald mindestens eine Teamregel hinterlegt ist, kann eine Teamrangliste erstellt werden.
Die Team-Zusammenstellung erfolgt entweder automatisch, oder explizit via Teamzuordnung.
Zusätzlich müssen die definierten Teams den Teamregeln entsprechen. Wenn ein Team zu klein oder zu gross
zusammengestellt wird, wird es von der Teamregel nicht in die Teamzusammenstellung aufgenommen.

### Automatische Teamselektion
Solange noch kein Teilnehmer oder keine Teilnehmerin eine expliziten Teamzuteilungen hat, werden die 
Teams anhand der natürlichen Selektionskriterien in ein Team eingeteilt:
* Verein
* Geschlecht
* Altersklasse
* Kategorie/Programm

### Explizite Teamselektion
Oft ist dies aber zu ungenau, oder es entstehen zu kleine oder zu grosse Teams.
Deshalb kann grundsätzlich bei jedem Teilnehmer oder Teilnehmerin eine Teamnummer erfasst werden.

Die Nummer kann als Teamnummer auf Vereins- oder Verbands-Ebene interpretiert werden.
Zudem gilt sie normalerweise pro Programm/Kategorie und Geschlecht.
Wenn Altersklassen definiert wurden, wirken diese ebenfalls als Abgrenzungskriterium.

Bei einer Turnerin im K3 wirkt sich dann die Teamnummer z.B. so aus, dass
sie mit anderen Turnerinnen aus K3 und aus dem selben Verein mit der selben Teamnummer 
zu einem Team zusammengestellt wird.

#### Reserve

Mit dem Reserve-Feld lassen sich nachrückende Teilnehmer/-Innen erfassen, falls es für ein Team unverhofft
Abmeldungen fix zugeordneter Teilnehmer/-Innen gibt.

### Zu kleine Teams

Unabhängig davon, ob die Teams automatisch oder explizit zusammengestellt werden,
kann es zu wenige Telnehmer/-Innen für eine Teamzusammenstellung innerhalb der
Geschlechts- und Programm/Kategorie/Altersklasse-Gruppierung geben.

Es lassen sich in so einem Fall die Teams in der Ranglisten-Konfiguration auch Geschlechts- und/oder Programm/Kategorie/Altersklasse übergreifend
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

Für die Team-Gesamtwertung gibt es zwei mögliche Ebenen, auf denen die Resultate ermittelt werden,
bevor sie mit einer wählbaren Aggregatsfunktion wie z.B. die Summe aller Wertungen 
das Teamresultat berechnet wird.

### Gesamtwertungen (Gesamt)

Aus einem Team werden die n besten Gesamtwertungen für das Teamresultat verwendet.

Die besten n Athleten pro Team werden anhand ihrer Gesamtpunktzahl
ermittelt; deren Einzelresultate fliessen in die Teamwertung ein.

### Gerätewertungen (Gerät)

Aus einem Team werden die n besten Wertungen pro Gerät herangezogen, um das Teamresultat zu berechnen.

Pro Gerät werden die besten n Einzelwertungen eines Teams herangezogen.

### Aggregatsfunktione für die Teamwertung

Auf beiden Ebenen kann optional eine Aggregatfunktion angegeben werden (standardmässig `sum`):

| Funktion  | Beschreibung |
|-----------|-------------|
| `sum`     | Summe der zählenden Resultate (default) |
| `avg`     | Durchschnittswert der zählenden Resultate |
| `median`  | Median der zählenden Resultate |
| `min`     | Niedrigster Wert der zählenden Resultate |
| `max`     | Höchster Wert der zählenden Resultate |
| `devmin`  | Standardabweichung (kleinere Abweichung gewinnt) |
| `devmax`  | Standardabweichung (grössere Abweichung gewinnt) |

Weitere Details zur Syntax im Abschnitt [Regel-Syntax](#regel-syntax).

Hier eine Visualisierung, wie für eine Teamwertung der Durchschnitt (`avg`) aus den jeweils besten `Geräte`-Wertungen berechnet wird:
![Unlimitierte Anzahl Teammitglieder aus dem Verein, wobei aus allen geturnten Resultaten über alle Kategorien und unabhängig
vom Geschlecht der Durchschnitt aus den besten drei Geräte-Wertungen die Teamwertung berechnet wird](/assets/team-scores-concept-calc-total.png)
_Unlimitierte Anzahl Teammitglieder aus dem Verein, wobei aus allen geturnten Resultaten über alle Kategorien und unabhängig
vom Geschlecht der Durchschnitt aus den besten drei Geräte-Wertungen die Teamwertung berechnet wird._

## <a href="#regel-syntax" id="regel-syntax">Regel-Syntax</a>

### Legende

* In der Syntax-Beschreibung kennzeichnen eckige Klammern `[]` optionale Bestandteile. 
  Ausser am Regelname selbst (z.B. für Gruppierungen) werden eckige Klammern in der effektiven Formel **nicht** ausgeschrieben, 
  also z.B. `VereinGerät[K5+K6](3/*)`.
* `*` ein Stern bedeutet `unbegrenzt` und kann sowohl für die Mindestanzahl- als auch für die Maximalanzahl-Teammitglieder verwendet werden.
* `...` mit 3 Punkten wird die `Fortsetzung einer Reihe` angedeutet (Verkettung von Elementen). Die Punkte werden in der effektiven Formel nicht verwendet.
* `,` mit Komma werden weitere `Teamregeln` voneinander getrennt.
* `/` mit Slash werden weitere `Gruppierungen` und `Parameter` voneinander getrennt.
* `+` mit Plus werden mehrere `mixed Teams` voneinander getrennt.

### Aufbau

`Regelname[Gruppierung]([Aggregat/]Zählende[/Max][/MixedTeam1[+MixedTeam2...]])[,Regel2...]`

1) **Regelname** (Pflicht): `VereinGerät`, `VereinGesamt`, `VerbandGerät` oder `VerbandGesamt`.
    * Der Regelname beginnt mit der **Abgrenzug** auf `Verein`s- oder `Verband`s-Ebene.
    * Anschliessend folgt die **Berechnungsmethode**, ob die Punkte der besten `Gerät` oder der besten `Gesamtwertungen` addiert werden sollen.

2) **Gruppierung** (optional): In eckigen Klammern, z.B. `[K5+K6+K7]`. Damit lassen sich Kategorien, Programme oder Geschlechter zusammenfassen.
    * Eine Zusammenfassung enthält Kategorie-Begriffe (z.B. `K5`) oder Geschlechts-Abkürzungen (`W`, `M`).
    * Begriffe innerhalb einer Gruppe werden mit `+` verbunden. `K5+K6+K7` bedeutet, dass sich ein Team aus diesen drei Kategorien zusammensetzen kann. Nicht erwähnte Kategorien bleiben separat.
    * Mehrere Gruppen werden mit `/` getrennt, z.B. `[K5+K6+K7/KH+KD]`.

3) **Parameter** in runden Klammern `([AggregatFn/]Min[/Max][/MixedTeams])`, die Parameter getrennt mit `/`:
    * _Optional_ die **Aggregatfunktion**: `sum`, `avg`, `median`, `min`, `max`, `devmin`, `devmax`. Ohne Angabe wird `sum` verwendet.
    * **Zählende Resultate**: Anzahl der pro Gerät (`Gerät`) bzw. pro Athlet (`Gesamt`) gewerteten Resultate. `*` bedeutet, dass alle Resultate zählen. Dieser Wert dient zugleich als Mindestteamgrösse.
    * _Optional_ die **Maximale Teamgrösse** (`Max`): `*` = unbegrenzt.
    * _Optional_ **Mixed-Team-Namen** (vereinsübergreifend), mit `+` getrennt.

### Umgang mit explizit erfassten mixed Teams

* Wenn in mehreren TeamRegeln Team-Namen aufgelistet werden, wird daraus eine Gesamtliste erstellt.
* Die mixed Teams in der Gesamtliste bekommen einen Index, über den die Zuweisungen hergestellt werden. Es ist deshalb darauf zu achten, dass einmal aufgelistete Teams nicht mehr in ihrer Position in der Gesamtliste ändern. Wenn also vorne ein Team herausgelöscht wird, stimmen die nachfolgenden Indicies nicht mehr. Aktuell gibt es von der App noch 
keine Unterstützung für stabilere Team-Zuweisungen.
* **Es gilt also grösste Vorsicht bei der nachträglichen Bearbeitung dieser mixed Teams Auflistung. Am sichersten ist es, wenn nur noch neue Teams am Ende einer Liste eingetragen werden**.

### Prioritätsregelung bei gemischten Teamregeln

Wenn eine gemischte Liste von Teamregeln (auf Vereins-Ebend und auf Verbans-Ebene) definiert wird, werden die Teamzuordnungen standardmässig auf Vereins-Ebene gemacht. Die Verbands-Team Zuteilung erfolgt dann ausschliesslich über die explizit definierten mixed Teams.

### Beispiele

| Formel | Beschreibung |
|--------|-------------|
| `VereinGerät(3/*)` | Team auf Vereins-Ebene mit den besten 3 Gerätenoten |
| `VereinGerät(median/*/4)` | Team auf Vereins-Ebene, Median der Gerätewertungen bei maximal 4 Teammitgliedern (alle Scores zählen) |
| `VereinGerät(3/4)` | Team auf Vereins-Ebene mit den besten 3 Gerätenoten mit maximal 4 Teamteilnehmer/-Innen |
| `VereinGerät[K6+K7+KD+KH](3/4)` | Team auf Vereins-Ebene, zusammengefasste Kategorien K6, K7, KD, KH mit den besten 3 Gerätenoten mit maximal 4 Teamteilnehmer/-Innen |
| `VereinGesamt(3/*)` | Team auf Vereins-Ebene mit den besten 3 Gesamtwertungen |
| `VereinGesamt(avg/*/*)` | Team auf Vereins-Ebene mit dem Durchschnittswert aller Gesamtwertungen |
| `VereinGesamt(3/4)` | Team auf Vereins-Ebene mit den besten 3 Gesamtwertungen mit maximal 4 Teamteilnehmer/-Innen |
| `VerbandGerät(4/*)` | Team auf Verband-Ebene mit den besten 4 Gerätenoten |
| `VerbandGerät(2/4)` | Team auf Verband-Ebene mit den besten 2 Gerätenoten mit maximal 4 Teamteilnehmer/-Innen |
| `VerbandGesamt(3/*)` | Team auf Verband-Ebene mit den besten 3 Gesamtwertungen |
| `VerbandGesamt(3/4)` | Team auf Verband-Ebene mit den besten 3 Gesamtwertungen mit maximal 4 Teamteilnehmer/-Innen |
| `VerbandGesamt(3/*),VereinGerät(2/*)` | Teams auf Verband-Ebene mit den besten 3 Gesamtwertungen, sowie Teams auf Vereins-Ebene mit den besten 2 Gerätenoten |
| `VereinGerät(3/*/Mixed Team 1+Mixed Team 2+Mixed Team 3+Mixed Team 4)` | Teams auf Vereins-Ebene mit den besten 3 Gerätenoten und mit 4 vordefinierten mixed Teams |
| `VereinGerät(3/4/Mixed Team 1+Mixed Team 2+Mixed Team 3)` | Teams auf Vereins-Ebene mit den besten 3 Gerätenoten mit maximal 4 Teamteilnehmer/-Innen und mit 3 vordefinierten mixed Teams |