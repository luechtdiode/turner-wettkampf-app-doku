# Rangierung bei Punktegleichstand

Wenn zwei mit dem gleichen End-Punktstand in der Rangliste aufgeführt werden, kann mittels Regeln definiert werden, wer in dem Fall vor dem anderen rangiert wird.

Die Punktegleichstands-Regel wird in der [Admin-Web-App](webadmin.md) in 
der [Anlegen-/Bearbeiten-Maske](wettkampf_anlegen.md) unter `Punktegleichstands-Regel` erfasst. 
Über den Editor-Button kann die Regel aus einer Liste von Vorgaben ausgewählt oder individuell zusammengestellt werden:

![](/assets/webadmin-editor-punktegleichstandsregel.png)

Der folgende Abschnitt beschreibt das Regelset und die Syntax der Punktegleichstandsregel.

## Regelset

### Ohne (Punktegleichstand ist gleicher Rang)

_Code_: `Ohne` 

Beide Teilnehmer werden gleichbereichtigt in der Rangliste aufgeführt. Sie belegen denselben Rang, wenn sie dieselbe Punktzahl erreicht haben.

### Jugend vor Alter

_Code_: `JugendVorAlter`

Der jüngere Teilnehmer bekommt den Vorrang vor dem Älteren.

### Beste E-Note (execution)

_Code_: `E-Note-Best`

Der Teilnehmer mit der besten E-Note, egal an welchem Gerät, bekommt den Vorrang.

### Beste E-Note-Summe (execution)

_Code_: `E-Note-Best-Summe`

Der Teilnehmer mit der höheren Summe aller E-Noten bekommt den Vorrang.

### Beste D-Note (difficulty)

_Code_: `D-Note-Best`

Der Teilnehmer mit der besten D-Note, egal an welchem Gerät, bekommt den Vorrang.

### Beste D-Note-Summe (difficulty)

_Code_: `D-Note-Best-Summe`

Der Teilnehmer mit der höheren Summe aller D-Noten bekommt den Vorrang.

### Disziplin (bessere Note auf Geräteebene)

_Code_: `Disziplin(<Gerät1>[,<Gerät2>,...])`

Die Endnoten der aufgeführten Diszipline werden der Reihe nach verglichen. Die erste Differenz entscheidet, wer vor dem anderen Rangiert wird.

### StreichDisziplin (streicht Note auf Geräteebene)

_Code_: `StreichDisziplin(<Gerät1>[,<Gerät2>,...])`

Die Endnoten der aufgeführten Diszipline werden der Reihe nach gestrichen. Die erste Differenz in der Gesamntnote der restlichen Wertungen entscheidet, wer vor dem anderen Rangiert wird.

### StreichWertungen (streicht die jeweils schlechteste oder beste Note)

_Code_: `StreichWertungen(<Endnote|E-Note|D-Note>[,<Min|Max>])`

Die kleinsten oder höchsten Endnoten, E-Noten oder D-Noten der aufgeführten Diszipline werden der Reihe nach gestrichen. Die erste Differenz in der Gesamtnote (Total Endnote, E-Note oder D-Note der restlichen Wertungen) entscheidet, wer vor dem anderen Rangiert wird.

**Beispiele**

* `StreichWertungen(Endnote,Min)` streicht der Reihe nach die schlechtesten Endnoten.
* `StreichWertungen(E-Note,Min)` streicht der Reihe nach die schlechtesten E-Noten.
* `StreichWertungen(D-Note,Max)` streicht der Reihe nach die besten D-Noten.

## Gliederungsmöglichkeiten der Punktegleichstandsregel

Die Regeln können mit dem entspr. _Code_ hintereinander gereiht werden. Die Regeln können mit einem `/` Slash zusammengehängt werden. So wird von vorne nach hinten bei Punktegleichstend die nächste Regel angewendet, bis es einen klaren Vorteil gibt.

Die `Ohne` Regel, wird als Default verwendet:

### Legende

* `[]` in eckigen Klammern sind optionale Bestandteile. Die eckigen Klammern selbst kommen in der Formel nicht zum Einsatz.
* `<>` in spitzen Klammern sind variable Bestandteile. Der darin vermerkte Text entspricht dem Code der Regel. Die spitzen Klammern selbst kommen in der Formel nicht zum Einsatz.
* `|` mit Pipe werden gültige Varianten in einer Auflistung von einander getrennt. Eine davon muss verwendet werden.
* `...` mit 3 Punkten wird die Fortsetzung einer Reihe angedeutet (verkettung von Elementen). Die Punkte werden in der konkreten Formel nicht verwendet.
* `/` mit Slash werden die ganze Regel-Elemente verkettet.

### Aufbau
_Syntax_: `<Regel1>[/<Regel2>/ ...]`.

### Beispiele

#### GeTu Standardregel

Formel: `Disziplin(Schaukelringe,Sprung,Reck)`

#### KuTu Standardregel

Formel: `E-Note-Summe/D-Note-Summe/JugendVorAlter`

#### KuTu STV Standardregel

* `StreichWertungen(Endnote,Min)/StreichWertungen(E-Note,Min)/StreichWertungen(D-Note,Min)` Diese Kombination entspricht der [Ex-aequo Regelung des STV](https://www.stv-fsg.ch/fileadmin/user_upload/stvfsgch/Sportarten/Kunstturnen/Weisungen_und_Reglemente/si_Reglement_ex-aequo_kutu_CD_2019_08_df.pdf)
