### Ausnahmen, Limitationen {#ausnahmen-limitationen}

#### Durchgang, in dem nicht jedes Gerät eine Startriege hat
![](/assets/not-all-startgeraete-assigned-issue.png)
Wenn in einem Durchgang nicht alle benötigten Geräte mit einer Riege als Startgerät verknüpft werden (weil es z.B. nicht genügend Riegen gibt), 
dann kann die App nicht erkennen, welche Geräte ausser den als Startgerät verknüpften im Durchgang wirklich geturnt werden sollen.
Es macht also ein Turnus mit allen als Startgerät verknüpften Geräten (grün) und die restlichen (rot) werden ignoriert.

#### Lösung mit leeren Riegen auf dem Startgerät
Eine andere Möglichkeit ist, im Durchgang beim Stargerät, wo keine Riege zugeteilt ist, eine leere Riege explizit zu setzen:

![](/assets/durchgang-leere-startriege-fix.png) 

Die Riegenbezeichnung `Leere Riege [Durchgang/Gerät] (0)` wird automatisch generiert, so dass es keine Namenskonflikte geben sollte, wenn z.B. mehrere solche leeren Riegen eingefügt werden müssten:

![](/assets/durchgang-leere-startriege-fixed.png)

Mit dieser leeren Riege im Startgerät des Durchganges wird sichergestellt, dass auch dieses Gerät in der Durchgangs-Rotation berücksichtigt ist.

#### Lösung mit Notenblätter (Riegenblätter werden nicht verwendet)
Da die Notenblätter pro Turner aufbereitet werden, und die Erfassung der Resultate dann nicht Riegen-orientiert sondern Turner-orientiert stattfindet, spielt die Durchgangsplanung keine Rolle.


