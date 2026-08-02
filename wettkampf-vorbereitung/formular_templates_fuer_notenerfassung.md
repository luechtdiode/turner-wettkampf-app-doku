# Formular Templates für die Notenerfassung

Wenn die normale Notenerfassung mit den möglichen Teilwerten A/D-Wert und B/E-Wert nicht ausreichen, können mit Hilfe von Templates
Formulare für die Notenerfassung hinterlegt werden.

## Bereitstellung in der Admin-Web-App

Die Formulare werden in der [Admin-Web-App](webadmin.md) verwaltet. In der [Wettkampf-Übersicht](wettkampf_uebersicht.md) 
unter `Verwaltung` → `Formulare (Notenerfassung)` werden die verfügbaren Formulare aufgelistet:

![](/assets/webadmin-formulare.png)

Mit `Neues Formular` wird ein neues Formular angelegt, mit dem Stift-Button ein bestehendes bearbeitet. Die Liste kann mit dem Suchfeld gefiltert werden. Formulare sind entweder `Global` (wettkampfübergreifend bereitgestellt) oder `Wettkampf`-spezifisch.

Im Formular-Editor werden die drei Formeln für den A/D-Wert, den B/E-Wert und den Penalty-Wert erfasst. Die eingegebenen Formeln werden sofort validiert und in einem Vorschau-Formular zum Ausprobieren angezeigt:

![](/assets/webadmin-formular-editor.png)

### Hinweise

1) Die in der Admin-Web-App gemachten Anpassungen werden nicht automatisch in die Datenbank der lokalen Desktop-App synchronisiert.
Hierzu muss der Benutzer den Wettkampf vom Server herunterladen (via Netzwerk Dashboard der Desktop-App, oder via Backup download aus der 
Admin-Web-App mit anschliessendem Import in der Desktop-App).
2) Sollten bereits Wertungen zu einer Disziplin erfasst sein, zu welcher ein Formular gespeichert wurde, werden diese Wertungen
zurückgesetzt. Diese Aktion sollte also nur in der Wettkampf-Vorbereitung genutzt werden.

## Notenerfassung in der lokalen Wettkampf-App

![](/assets/wk-formular-noteneingabe.png)

## Notenerfassung in der mobilen Web-App

![](/assets/wk-formular-mobile-noteneingabe.png)

# Bereitstellung eigener Formulare

Ein Formular besteht aus drei Formeln, in denen beliebig Variablen verwendet werden können, die für die Berechnung einer der Werte A/D-Wert, B/E-Wert oder Penalty benötigt werden.

![](/assets/wk-formular-admin-newform.png)

Die im Template definierten Variablen werden im Formular als Eingabefeld bereitgestellt.

Eine Variable besteht aus einem Prefix, einem Namen, der im Formular angezeigt wird und optional eine Angabe, mit wievielen Nachkommastellen gearbeitet wird.

Die Variablen werden in einer mathematischen Formel verwendet, um den A/D-Wert, den B/E-Wert oder den Penalty-Wert zu berechnen.

Die im Bearbeitungs-Dialog eingegebenen Formeln werden sofort validiert und in einem Vorschau-Formular zum ausprobieren angezeigt.

## Variablen-Format
`<Prefix><Name>[.<Kommastellen>]`

### Prefixe
| Prefix | Bedeutung |
| -------: | :---------------------- |
| `$D`     | Variable für den D-Wert |
| `$A`     | Variable für den A-Wert |
| `$E`     | Variable für den E-Wert |
| `$B`     | Variable für den B-Wert |
| `$P`     | Variable für den Penalty-Wert |

### Namensgebung

Die Zeichenkette muss mit Buchstaben beginnen und darf danach Buchstaben, Leerzeichen und Zahlen enthalten. 

Umlaute sind nicht erlaubt.

### Präzision

Kommastellen 0-3 möglich

### Regular Expression

Regex: `\$([ADBEP]{1})([\w]+[\w\d]*)(.([0123]+))?`

### Beispiele:

| Wert für Endnote       | Beispiel Variablen                |
| ---------------------: | :-------------------------------- |
|D-Variablen: Difficulty | `$DSchwierigkeit.1`, `$DD Wert.1` |
|E-Variablen: Execution  |`$EE-Note.3`, `$EAusfuehrung2.3`   |
|P-Variablen: Penalty    | `$PPenalty`, `$PNeutraler Abzug.0`|

## Math.-Funktionen

Die variablen Werte können mit Hilfe folgender mathematischen Funktionen in einer Formel verwendet werden:

| Funktion | zu verwendendes Zeichen |
| -------: | :---------------------- |
|Multiplikation|`*`|
|Division| `/`|
|Addition| `+`|
|Subtraktion| `-`|
|Summe mehrerer Werte| `sum(a,b,...)`|
|Durchschnitt mehrerer Werte| `avg(a,b,...)`|
|Grösster Wert| `max(a,b,...)`|
|Kleinster Wert| `min(a,b,...)`|

## Formel

Die Formel beschreibt, wie ein A/D-Wert, ein B/E-Wert oder ein P-Wert berechnet wird.

Das Formular kennt somit drei Formeln, die frei definierbar sind.
Bei Wettkampf-Arten, die keine A/D-Note kennen, gibt es nur zwei Formeln (für B/E-Note und für Penalty).

### Anzeige der Teilnoten in der Rangliste

Wenn am Ende der Formel das Dereferenzierungs-Zeichen `^` angehängt wird, werden die einzelnen Werte der Formel in der Rangliste angezeigt.

![Noten Teilwerte Darstellung in der Rangliste](/assets/wk-formular-rangliste-teilwertdarstellung.png)

## Mehrere Gesamtübungsbewertungen

Die drei Teilnoten können maximal 2-Mal (2-Übungen) erfasst werden.

Für die Berechnung der Endnote werden die jeweiligen geturnten Endnoten mit einer Aggregat-Funktion zusammengerechnet (Avg, Sum, Max Min) auf Ebene (DNote, ENote oder Endnote).

### Min/Max

Bedeutet, dass die Teilnoten (A/D, B/E, und P) sowie die Endnote von der Übung mit der **niedrigsten/höchsten Endnote** übernommen wird.

### Sum/Avg

Bedeutet, dass von allen Noten die Summe oder der Durchschnitt aus den einzelnen Übungsbewertungen gerechnet wird.

## Formel Beispiele

```
DNote = max($Dname1.1, $Dname2.1)^
ENote = avg(10 - $Ename1.3, 10 - $Ename2.3)
PNote = ($Pname.0 / 10)^
```

Die Endnote wird automatisch folgendermassen berechnet:

```
Implizit: Endnote = max(0, min(30, DNote) + min(10, ENote) - PNote)

Implizit: Total DNote = Aggregate(max(0, min(30, DNote)), ...)
Implizit: Total ENote = Aggregate(max(0, min(30, ENote)), ...)
Implizit: Total Endnote = Aggregate(max(0, min(30, DNote) + mi (10, ENote) - PNote), ...)
```

## Formularzuordnung auf Disziplin oder Kategorie-Disziplin Ebene

Ein Formular kann auf mehreren Ebenen definiert werden:

![](/assets/wk-formular-admin.png)


### Ebene Wettkampf

Es sind keine expliziten Zuordnungen auf Disziplin oder Kategorie-Disziplin gemacht.

Alle Geräte im Wettkampf verwenden das selbe Formular.

### Ebene Disziplin

Es sind keine expliziten Zuordnungen Kategorie-Disziplin gemacht.

Die angegebene Disziplin bei allen Kategorien im Wettkampf verwendet das selbe Formular.

### Ebene Kategorie-Disziplin

Es existiert eine explizite Zuordnung auf eine Kategorie-Disziplin.

Nur bei der angegebenen Kategorie-Disziplin im Wettkampf wird das Formular verwendet.

## Wettkampfübergreifende Formulare

Es kann auch Formulare geben, die nicht auf Wettkampf-Ebene bereitgestellt werden, sondern übergreifend.

Diese werden fix mit dem Programm installiert und gelten dann bei bestimmmten Wettkampf-Diszipline, wie zum Beispiel dem Trampolin in der Kategorien BS und OS beim Turn10 Wettkampfmodus.

Aktuell sind noch keine solchen Formulare bereitgestellt.