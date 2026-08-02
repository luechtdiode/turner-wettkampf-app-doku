# Wettkampf anlegen

»Siehe auch: [Wettkampf anlegen](../stammdatenpflege/wettkampf_anlegen.md)

Ein Wettkampf wird in der [Admin-Web-App](webadmin.md) angelegt. Unter `Meine Wettkämpfe` öffnet der Plus-Button unten 
rechts die Maske `Neuen Wettkampf anlegen`:

![](/assets/webadmin-anlegen.png)

Folgende Werte werden dabei erfasst:

1. **Wettkampf-Datum**, an dem der Wettkampf durchgeführt wird.
2. **Titel** des Wettkampfs, ohne Datum, ev. mit Ortsangabe (z.B. GeTu-Regionalmeisterschaft Basel-Stadt).
3. **Logo** (optional): Es kann eine Bilddatei ausgewählt und wieder entfernt werden. Bevorzugt werden `svg`-Dateien, weil diese besser auf hochauflösenden Druckern dargestellt werden. Zu kleine Bilder können dadurch verpixelt dargestellt werden.
4. **Programm** (Art des Wettkampfs):
   * Geräteturn-Wettkampf (plus eine Variante BLTV mit Altersabgrenzungen in den Kategorien)
   * [Turn10® Programme BS/OS](https://www.turn10.eu)
     * Turn10®-Verein für bis zu 7 Geräte
     * Turn10®-Schule für bis zu 5 Geräte
   * Kunstturn-Wettkampf
     * KuTu-Wettkampf für männliche Gerätebelegung
     * KuTuRi-Wettkampf für die weibliche Gerätebelegung
     * KuTu TG Allgäu Kür & Pflicht (männliche Gerätebelegungsregel)
     * KuTuRi TG Allgäu Kür & Pflicht (weibliche Gerätebelegungsregel)
   * Athletiktest
5. **Benachrichtigungs-Email**: EMail-Adresse, an welche die Mutationen bei Online-Anmeldungen gemeldet werden.
6. **Auszeichnung (%)**: Schwellwert für die Medallien-Bedarfsberechnung. Die Prozent-Angabe darf bis zu drei Stellen nach dem Komma haben.
7. **Auszeichnung Endnote**: Optionaler Mindest-Gerätedurchschnitt für eine Auszeichnung (z.B. 7.5 Punkte bei Geräte-Tests). Die Angaben können kombiniert verwendet werden.
8. **Altersklassen-Regel** (Alter am Wettkampftag) und **Jahrgangs-Altersklassen-Regel** (Alter im Jahr des Wettkampfes): Belegung mit einem vordefinierten Preset, manuell oder mit dem Editor. Siehe [Altersklassen hinterlegen](altersklassen.md).
9. **Punktegleichstands-Regel**: Wie die Rangierung bei Punktegleichstand ermittelt wird. Siehe [Rangierung bei Punktegleichstand](punktgleichstand.md).
10. **Riegen-Rotations-Regel**: Wie von einem Wettkampf zum nächsten die Startreihenfolge der Vereine und deren Teilnehmer rotieren soll. Siehe [Startreihenfolge in den Geräte-Riegen](riegenrotation.md).
11. **Team-Regel**: Regeln, was ein Team ausmacht. Siehe [Teams / Mannschaften](teamregeln.md).

Beim Anlegen werden zusätzlich die **Ersteller-Informationen** (Name, Adresse, Telefon) sowie die Zustimmung zu den 
Nutzungsbedingungen abgefragt. Nach dem Anlegen wird eine Bestätigungs-Email an die angegebene Adresse gesendet. 
Der Wettkampf wird erst nach Bestätigung aktiv. Ohne Bestätigung innerhalb von 24h, wird der Wettkampf wieder gelöscht.

## Wettkampf kopieren

Wenn ein neuer Wettkampf angelegt werden soll, der dieselbe Parametrisierung wie ein bestehender Wettkampf haben sollte, 
kann in der [Wettkampf-Übersicht](wettkampf_uebersicht.md) unter `Wettkampf` → `Wettkampf kopieren` kopiert werden.

In diesem Fall werden folgende Elemente aus dem selektierten Wettkampf übernommen:

* Sämtliche Parameter aus der Anlegen-Maske, mit Ausnahme des Wettkampf-Datums.
* Wettkampf-Logo
* Notenerfassungs-Formulare
* Planzeiten
* Ranglisten-Einstellungen

Für die Parametrisierung in der Desktop-App siehe [Wettkampf anlegen](../stammdatenpflege/wettkampf_anlegen.md).
