### Ausnahmen, Limitationen {#ausnahmen-limitationen}

#### Durchgang, in dem nicht jedes Gerät eine Startriege hat

**Problemstellung**<br>Wenn in einem Durchgang nicht alle benötigten Geräte mit einer Riege als Startgerät verknüpft werden (weil es z.B. nicht genügend Riegen gibt), dann kann die App nicht erkennen, welche Geräte ausser den als Startgerät verknüpften im Durchgang wirklich geturnt werden sollen.<br>Es macht also ein Turnus mit allen als Startgerät verknüpften Geräten (grün) und die restlichen (rot) werden ignoriert:

![](/assets/not-all-startgeraete-assigned-issue.png)

##### a) Lösung mit alternativer Durchgang-Riegeneinteilung
Mit der Reorganisation der Durchgang-Riegeneinteilung (z.B. Durchgänge zusammenfassen) lassen sich wiedr mehr Riegen zu einem Durchgang finden, wodurch möglicherweise alle Startgeräte belegt werden können.
![](/assets/not-all-startgeraete-assigned-issue.png)
Wenn in einem Durchgang nicht alle benötigten Geräte mit einer Riege als Startgerät verknüpft werden (weil es z.B. nicht genügend Riegen gibt), 
dann kann die App nicht erkennen, welche Geräte ausser den als Startgerät verknüpften im Durchgang wirklich geturnt werden sollen.
Es macht also ein Turnus mit allen als Startgerät verknüpften Geräten (grün) und die restlichen (rot) werden ignoriert.

##### b) Lösung mit leeren Riegen auf dem Startgerät
|||
|-|-|
|Bei allen nicht besetzten Startgeräten (wo keine Riege zugeteilt ist), wird explizit eine leere Riege zugewiesen.<br>Mit dieser leeren Riege im Startgerät des Durchganges wird sichergestellt, dass auch dieses Gerät in der Durchgangs-Rotation berücksichtigt ist.|![](/assets/durchgang-leere-startriege-fix.png)|
|Die Riegenbezeichnung `Leere Riege [Durchgang/Gerät] (0)` wird automatisch generiert, so dass es keine Namenskonflikte geben sollte, wenn z.B. mehrere solche leeren Riegen eingefügt werden müssten.|![](/assets/durchgang-leere-startriege-fixed.png)|
|Zum entfernen einer nicht mehr benötigten leeren Riege muss in den `Riegen`-Tab gewechselt werden. Dort kann die Riege selektiert und dann gelöscht werden.|![](/assets/remove-empty-squad.png)|
|||

##### c) Lösung mit Notenblätter (Riegenblätter werden nicht verwendet)
Sofern es noch überschaubar bleibt (kleinerer Wettkampf), empfiehlt sich auch die Erfassung mit Notenblätter pro Turner durchzuführen.

#### Resultat-Erfassung bei Riegen mit gemischten Kategorien

|||
|-|-|
|**Problemstellung**<br>Bei den Listen pro Kategorie/Programm kann es vorkommen, dass mit dem Riegenfilter (hier K7) nicht alle Turner-/Innen für die Erfassung zur Verfügung stehen (hier fehlen die K6 Barrenturner).|![](/assets/gemischte-kategorien-issue2.png)|
|**Hilfestellung**<br>Für die Erfassung der Resultate mit Riegen gemischter Kategorien, soll die **ungefilterte Liste** der Turner (Tab `Alle`) verwendet werden.|![](/assets/gemischte-kategorien-solution.png)|
|Zur Orientierung, dass es sich bei einer Riege um eine "gemischte" Riege handelt, werden auf den Riegen-Notenblätter pro Turner/-In jeweils dessen Kategorie-/Programmeinteilung aufgedruckt.|![](/assets/gemischte-kategorien-issue.png)|
