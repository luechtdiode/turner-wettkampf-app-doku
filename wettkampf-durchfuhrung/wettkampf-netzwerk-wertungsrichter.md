# Resultat-Erfassung über Mobile-App

Die Wettkampf-Resultate können anstatt auf Papier auch/alternativ via der Mobile-Browserapp erfasst werden. Auf diese Weise lassen sich die Resultate schneller und sicherer verarbeiten.

Im Falle von Störungen können die Resultate von hand ausgefüllt auf den Riegenblätter in das Rechnungsbüro gemeldet werden.

## Vorbereitungsmassnahmen für jeden Wertungsrichter

### 1\) QR-Code Reader auf dem Mobil-Gerät installiert

Hierzu eignen sich solche, die den Link _direkt_ im Browser öffnen können - also **nicht** innerhalb der QR-Code App, wo deswegen meist weniger Display-Fläche zur Verfügung steht. Der Markt solcher Apps ist sehr lebendig. Wir haben für iOS und für Android folgende Apps getestet, welche diesen Anforderungen genügen:

| Device-OS | QR-Code Reader Empfehlung |
| :--- | :--- |
| iOS | Sofern noch ein älteres iOS betrieben wird, ist noch kein QR-Code Reader direkt in der Kamera integriert. In diesen Fällen hat sich `CMYUK QR Reader` [Link auf Apple iTunes](https://itunes.apple.com/de/app/cmyuk-qr-code-reader/id1083426097?mt=8) in unseren Tests geeignet |
| Android | Der `Tahoe QR Code Reader` [Link auf Google Playstore](https://play.google.com/store/apps/details?id=com.gogoideal.qrcode.reader.barcode.scanner.flashlight&hl=de) von Tahoe Digital LTD ist im Android-Gerät als Freeware ohne lästiger Werbung zu empfehlen |

### 2\) Das Mobil-Gerät muss vollständig aufgeladen mitgebracht werden

Falls befürchtet wird, dass die Akkuladung nicht ausreichen wird, empfiehlt sich ein Akku-Pack oder ein Lade-Adapter mitzunehmen.

### 3\) In der Turnhalle muss ausreichend Signalstärke mit dem eigenen Mobilfunk-Anbieter existieren

Wenn dies nicht gegeben ist, wird möglicherweise in der Turnhalle ein Wireless-Netzwerk bereitgestellt, in welches sich der Wertungsrichter einwählen kann und welches Internet-Zugang gewährt.

## In der Turnhalle bei der Wertungsrichter-Instruktion

<table>
  <thead>
    <tr>
      <th style="text-align:left">1. Zugang zum lokalen Wireless einrichten (sofern die eigene Verbindung
        nicht ausreichend funktioniert)</th>
      <th style="text-align:left">
        <ul>
          <li>Netzwerkname</li>
          <li>Username</li>
          <li>Passwort</li>
        </ul>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">2. QR-Code f&#xFC;r die Berechtigung zur Resultaterfassung scannen. Hierzu
        wird vom Rechnungsb&#xFC;ro entweder ein QR-Code am Bildschirm oder auf
        einem Ausdruck zur Verf&#xFC;gung gestellt</td>
      <td style="text-align:left">
        <img src="/assets/mobile-register.png" alt/>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">3. Das Mobilger&#xE4;t soll gegen Ablenkungen durch Push-Nachrichten aus
        Chats etc in einen &quot;Bitte nicht st&#xF6;ren&quot;-Modus versetzt werden.</td>
      <td
      style="text-align:left">
        <img src="/assets/how-to-config-quiet-mode.png" alt/>
        </td>
    </tr>
  </tbody>
</table>

## Am Wertungstisch

Auf den Riegenblätter ist ein QR-Code aufgedruckt, mit welchem ein Link bereitgestellt wird, welcher die Mobile-Browserapp direkt an der richtigen Stelle öffnet, so dass dort die Resulate der Riegen-Teilnehmer/-Innen in der entpsrechenden Reihenfolge erfasst werden können.

![](/assets/riegenblaetter.png)

## Wertungsrichter initialisiert sein Mobile-Device an seiner Station mit dem [QR-Code vom Riegenblatt](wettkampf-netzwerk-wertungsrichter.md#qrcode-printouts)

|  Auf den Riegenblätter zur manuellen Resultaterfassung, befindet sich jeweils ein QR-Code, mit welchem die Mobile-App direkt am richtigen Ort gestartet werden kann. Zu Beginn kann es sein, dass die Resultaterfassung noch gesperrt ist. Diese wird durch die Wettkampfleitung im Rechnungsbüro freigegeben.  | ![](/assets/resultaterfassen-gesperrt.png) |
| :--- | :--- |


## Wertungsrichter erfasst Wettkampf-Resultate

Mit dem Button `RESULTATE` gelangt man in der Mobile-App zu den Turner/-Innen, die in der Reihenfolge aufgelistet werden, in der sie ihre Wettkampf-Übung vorturnen sollen.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Mit einem Click auf die Person &#xF6;ffnet sich die Noten-Eingabemaske.
        <br
        />
        <br />
      </th>
      <th style="text-align:left">
        <img src="/assets/resultaterfassen-gestartet2.png" alt/>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>Bei Kunstturn-Wettk&#xE4;mpfen kann hier auch eine D-Note erfasst werden.</p>
        <p>Mit einem Click auf die E-Note (1) kann die entsprechende Ausf&#xFC;hrungs-Note
          (E wie Execution) erfasst/korrigiert werden.</p>
        <p>Die Endnote wird beim `Speichern` oder beim `Speichern &amp; Weiter` (2)
          vom Programm berechnet und aktualisiert. Bei Athletiktests gibt es verschiedene
          Multiplikationsfaktoren, die mit der E-Note multipliziert die Endnote ausmachen.
          Bei Kunstturn-Wettk&#xE4;mpfen wird die D-Note und die E-Note zusammengez&#xE4;hlt.</p>
        <p>Es k&#xF6;nnen auch Fehler gemeldet werden. Wenn z.B. die Berechtigung
          f&#xFC;r die Resultat-Erfassung abgelaufen ist oder der Durchgang gerade
          gesperrt ist, k&#xF6;nnen keine Resultate erfasst/korrigiert werden.</p>
        <p> <em>Achtung</em> Wenn die eingeblendete Nummer-Eingabetastatur die Buttons
          &#xFC;berdeckt, muss f&#xFC;r dessen Bet&#xE4;tigung der Bildschirm nach
          oben gescrollt werden, so dass die Buttons wieder sichtbar werden.</p>
      </td>
      <td style="text-align:left">
        <img src="/assets/resultcatcher-wertung-erfassen.png" alt/>
      </td>
    </tr>
  </tbody>
</table>

Wenn alle Resultate einer Riege an einem Gerät erfasst sind, soll die Resultaterfassung für diese Riege an diesem Gerät abgeschlossen werden. Dies wird mittels `Eingaben abschliessen` gemacht und bewirkt zusätzlich, dass die nächste Riege für die Resultaterfassung geladen wird.

