# Altersklassen

Altersklassen sind ein Gruppierungs-Hilfsmittel sowohl für die Riegen-Zusammenstellung, als auch für die Ranglistenerstellung.

## Einteilung in Riege für die Durchgangsplanung

Es können damit alle Teilnemher/-Innen einer Altersklasse in einer Riege im Durchgang eingeteilt werden. Dies ermöglicht die Planung, wie die Wertungs-/Kampfrichter aufgestellt werden müssen. Diese müssen dann jeweils alle einer Altersklasse bewerten, so dass es konsistente Bewertungungen geben kann.

## Berechnung des Medallienbedarfs

Wenn die Ranglisten anhand der Altersklassen gruppiert werden, sind die erforderlichen Medallien nicht ausschliesslich aus den Wettkampf-Programmen abzuleiten, sondern zusätzlich auch noch pro existierender Altersklasseneinteilung.

## Zusammenfassung in der Rangliste

Es können damit alle Teilnehmer/-Innen einer Altersklasse in einer gemeinsamen Rangierung aufgelistet werden.

## Berechnungsarten

### Alter am Wettkampf-Tag

Die Altersklasse berechnet sich anhand des effektiven Geburtsdatums des Teilnehmers, der Teilnehmerin. Dieses wird gegenüber dem Wettkampfdatum gestellt. Die Differenz in ganzen Jahren ist die relevante Zahl für die Eingliederung in die Altersklasse.

### Alter nach Differenz aus Wettkampf-Jahr minus Jahrgang

Die Jahrgangs-Altersklasse berechnet sich anhand des Jahrgangs des Teilnehmers, der Teilnehmerin. Dieses wird gegenüber dem Jahr im Wettkampf-Datum gestellt. Die Differenz ist die relevante Zahl für die Eingliederung in die Altersklasse.

## Gliederungsmöglichkeiten der Altersklassen

Die Alterklassen werden im Grunde anhand von Altersgrenzen mit numerischen Angaben und komma-separiert festgelegt (`<Altersgrenze1>[,<Altersgrenze2>, ...]`).
Die Altergrenzen `7,10,16,25` ergeben damit folgende Altersklassen:
* Altersklasse bis 6
* Altersklasse 7-9
* Altersklasse 10-15
* Altersklasse 16-24
* Altersklasse ab 25

Um komplexere Strukturen zu definieren, gibt es zusätzlich folgende Möglichkeiten:
* Explizite Angabe der Altersklassenbezeichnung (vorangestellte Buchstaben `<Bezeichnung><Altersgrenze>`)
* Range-Angabe für automatische Inkrements um 1 Jahr zwischen zwei Altersgrenzen (verbinden der Altersgrenze mit Bindestrich `<von>-<bis>`)
* Explzite Inkrement-Angabe, sofern in einem Range nicht jedes Jahr eine neue Altersgrenze generieren soll (verbinden mit Division und Inkrement-Wert `/<Inkrement-Wert>`)

Zusammengesetzt ergibt sich volgener Syntax:

`[<Bezeichnung>]<VonAlter>[-<BisAlter>[/<InkrementWert]]`

## Altersklasse als Wettkampf-Bestandteil

Wenn die Altersklassen im Erfassungsdialog zum Wettkampf definiert oder ausgewählt werden, werden sie sowohl in der Wettkampfübersicht als auch bei der Riegeneinteilung und in der Rangliste integriert angewendet.

In der Wettkampf-Übersicht werden die Wettkampf-Altersklassen aufgeführt, und die Gliederungen mit den Altersklassen erweitert:
Beispiel mit Turn10:

![](/assets/Turn10-Wettkampfuebersicht-Altersklassen.png)

Beispiel TG Allgäu:

![](/assets/TGAllgaeu-Wettkampfuebersicht-Altersklassen.png)

Die Riegeneinteilung erfolgt anhand der hinterlegten Altersklassen.

Beispiel TG Allgäu mit Pflicht und Kür und Riegen mit Altersklassen-Bezeichnungen:

![](/assets/TGAllgaeu-WertungTab-Pflicht-Kuer-Altersklassen-Riegen.png)

## Altersklasse als dynamisch hinzugefügter Filter/Gruppierer in der Rangliste

Sofern nicht primär nach Altersklassen dividiert wird, kann es immer noch sinnvoll sein, die Altersklassen-Gliederung in der Rangliste zu verwenden. Diese Möglichkeit besteht dann (ohne Wettkampf-Altersklassen) mit den vordefinierten Altersklassen.

![](/assets/rangliste-altersklasse-grouper.png)