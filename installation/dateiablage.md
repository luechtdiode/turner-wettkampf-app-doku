# Dateiablage

## Programminstallation <a id="programminstallation"></a>

## Windows

Die Installationsdatei ist ein Windows-Installationspaket (msi), mit welchem ein Assistenz-gestütztes Installieren der App möglich ist.

_(der Stern `*` steht für die Versionsbezeichung)_

**Dateiname** : `TurnerWettkampf-App_v*.msi`

### Programm

Die Programmdateien werden unter Windows in das Verzeichnis **`%programfiles%\TurnerWettkampf-App`** gespeichert.

Sie beinhalten eine eigenständige Java Virtual Machine (JVM Version 21) sowie die notwendigen Programm-Dateien für die Ausführung der App.

### Daten <a id="daten"></a>

Die Datenbank wird automatisch angelegt. Sie befindet sich in folgendem Verzeichnis:

**`%userprofile%\kutuapp\db`**

Darüber hinaus werden vom Programm Dateien angelegt, die für zum Drucken oder für den Datenaustausch benötigt werden.

Diese Dateien befinden sich alle im Benutzerverzeichnis: **`%userprofile%\kutuapp\data`** resp. den darunter liegenden Verzeichnissen.

Pro Wettkampf wird von der App ein eigenes Verzeichnis darin angelegt und die dazu gehörenden Dateien werden darin abgelegt.

## Mac OS

Die Installationsdatei ist ein Mac OS Installationspaket (pkg), mit welchem ein Assistenz-gestütztes Installieren der App möglich ist.

_(der Stern `*` steht für die Versionsbezeichung)_

**Dateiname** : `TurnerWettkampf-App_v*.pkg`

### Programm

Die Programmdateien werden unter Mac OS in das Applikations-Verzeichnis **`/Applications/TurnerWettkampf-App-*.app`** gespeichert.

Sie beinhalten eine eigenständige Java Virtual Machine (JVM Version 21) sowie die notwendigen Programm-Dateien für die Ausführung der App.

### Daten

Die Datenbank wird automatisch angelegt. Sie befindet sich in folgendem Verzeichnis:

**`~\kutuapp\db`**

Darüber hinaus werden vom Programm Dateien angelegt, die für zum Drucken oder für den Datenaustausch benötigt werden.

Diese Dateien befinden sich alle im Benutzerverzeichnis: **`~\kutuapp\data`** resp. den darunter liegenden Verzeichnissen.

Pro Wettkampf wird von der App ein eigenes Verzeichnis darin angelegt und die dazu gehörenden Dateien werden darin abgelegt.

## Linux

Die Installationsdatei ist ein Linux amd64bit Installationspaket (deb), mit welchem ein Assistenz-gestütztes Installieren der App möglich ist.

_(der Stern `*` steht für die Versionsbezeichung)_

**Dateiname** : `turnerwettkampf-app_v*amd64.deb`

### Programm

Die Programmdateien werden unter Linux in das opt Verzeichnis **`/opt/turnerwettkampf-app-*`** gespeichert.

Sie beinhalten eine eigenständige Java Virtual Machine (JVM Version 21) sowie die notwendigen Programm-Dateien für die Ausführung der App.

### Daten

Die Datenbank wird automatisch angelegt. Sie befindet sich im User-Home unter folgendem Verzeichnis:

**`~\kutuapp\db`**

Darüber hinaus werden vom Programm Dateien angelegt, die für zum Drucken oder für den Datenaustausch benötigt werden.

Diese Dateien befinden sich alle im Benutzerverzeichnis: **`~\kutuapp\data`** resp. den darunter liegenden Verzeichnissen.

Pro Wettkampf wird von der App ein eigenes Verzeichnis darin angelegt und die dazu gehörenden Dateien werden darin abgelegt.
