# Localis

Localis ist eine Sammlung von Werkzeugen für Windows, mit denen sich alltägliche Aufgaben rund um Bilder, Dateien, Texte, Passwörter und Farben erledigen lassen. Ich entwickle es als privates Projekt und gebe es kostenlos an Freunde und Bekannte weiter. Die aktuelle Fassung ist eine Vorschau: Einzelne Abläufe können noch Fehler enthalten, und Funktionen wie Oberfläche entwickeln sich mit den kommenden Updates weiter.

## Herunterladen

**[Localis für Windows herunterladen](https://github.com/grammok/localis/releases/latest/download/Localis-Setup.exe)** (Installationsdatei, etwa 45 MB)

* **Voraussetzung:** Windows 11 mit 64 Bit. Unter Windows 10 ab Version 1809 lässt sich Localis ebenfalls installieren, ist dort aber nicht getestet.
* **Installation:** nur für dein Benutzerkonto und ohne Administratorrechte, standardmäßig in den Ordner `%LOCALAPPDATA%\Programs\Localis`. Angelegt werden ein Eintrag im Startmenü und auf Wunsch eine Verknüpfung auf dem Desktop; einen Autostart oder Hintergrunddienst richtet Localis nicht ein.
* **Alle Versionen** mit ihren Neuigkeiten und Prüfsummen stehen unter [Releases](https://github.com/grammok/localis/releases). Die dort aufgeführten Archive „Source code“ erzeugt GitHub automatisch; für die Installation werden sie nicht benötigt.

### Warnungen von Browser und Windows

Die Installationsdatei ist nicht digital signiert, weil dafür ein kostenpflichtiges Zertifikat nötig wäre, und wird in jeder neuen Version anfangs nur selten heruntergeladen. Browser und Windows stufen sie deshalb zunächst als unbekannt ein:

* **Chrome** zeigt gegebenenfalls im Downloadbereich eine entsprechende Warnung. Über „Behalten“ beziehungsweise „Trotzdem herunterladen“ bleibt die Datei erhalten; andere Browser verfahren ähnlich.
* **Windows SmartScreen** kann beim Öffnen „Der Computer wurde durch Windows geschützt“ melden. Über „Weitere Informationen“ und anschließend „Trotzdem ausführen“ startet die Installation.

### Prüfsumme vergleichen

Ob die Datei unverändert bei dir angekommen ist, kannst du vor der Installation anhand ihrer Prüfsumme (SHA256) feststellen:

1. Öffne PowerShell, etwa über die Suche im Startmenü.
2. Führe den folgenden Befehl aus. Liegt die Datei in einem anderen Ordner, passe den Pfad an.

   ```powershell
   Get-FileHash "$env:USERPROFILE\Downloads\Localis-Setup.exe"
   ```

3. Vergleiche den angezeigten Wert mit der Zeile `Localis-Setup.exe` in der Datei `SHA256SUMS` des [neuesten Releases](https://github.com/grammok/localis/releases/latest). Ob die Buchstaben groß oder klein geschrieben sind, spielt dabei keine Rolle.

## Werkzeuge

Jedes Werkzeug erklärt sich selbst: Über „?“ oben rechts oder mit F1 öffnet sich eine kurze Anleitung mit allen Tastenkürzeln.

* **CutOut** entfernt den Hintergrund aus Fotos und Grafiken. Für schwierige Umrisse stehen Rechteck, „Teil wählen“, Zauberstab und die Pinsel „Zurückholen“, „Entfernen“ und „Feine Kanten“ bereit; bewährte Einstellungen lassen sich als eigenes Profil speichern.
* **ImageBatch** ändert in einem Durchgang Größe und Format vieler Bilder und dreht oder spiegelt sie bei Bedarf. Die Vorschau zeigt genau die Datei, die entstehen wird. Vorhandene Dateien, die Originale eingeschlossen, überschreibt es nie, und Metadaten wie Aufnahmeort oder Kameramodell übernimmt es nicht.
* **SketchTools** verwandelt Fotos und Bilder in schwarzweiße Zeichnungen, wahlweise als Bleistift, Skizze, Graphit, Kohle, Tusche, Comic, Schraffur oder Punkte. Linien und Schatten stammen aus dem Bild selbst und werden mit klassischer Bildverarbeitung berechnet. Der Hintergrund kann weiß, papierfarben oder durchsichtig sein; mit CutOut freigestellte Motive ergeben so saubere Strichzeichnungen. Gespeichert wird eine neue Datei, das Original bleibt unverändert.
* **FileRename** benennt viele Dateien nach kombinierbaren Regeln um, etwa nach Aufnahmedatum, mit fortlaufender Nummer oder durch Ersetzen von Text. Jeder neue Name ist vorab zu sehen, und „Rückgängig“ stellt die alten Namen wieder her.
* **HashTools** prüft anhand von Prüfsummen, ob ein Download oder eine Sicherung unverändert ist, auch mit Listen wie `SHA256SUMS`, und vergleicht ganze Ordner Byte für Byte. Die geprüften Dateien liest es nur.
* **PasswordGenerator** erzeugt Passwörter, Passphrasen aus deutschen Wörtern, PINs und Zufallswerte wie Hex, Base64 oder UUID, ausschließlich aus kryptografisch sicherem Zufall. Bei Passwörtern lassen sich einzelne Zeichen ausschließen oder ergänzen. Erzeugte Werte werden nirgends gespeichert. Kopierte Werte gelangen weder in den Verlauf der Zwischenablage noch in die Cloud; Localis entfernt sie nach einer einstellbaren Zeit, spätestens beim Beenden, wieder aus der Zwischenablage, sofern sie noch darin liegen.
* **QrTools** erzeugt QR-Codes für Texte, Links, WLAN, Kontakte, Mails, Telefonnummern, SMS, Messenger und soziale Netzwerke und speichert sie als PNG oder SVG.
* **TextTools** bearbeitet Texte in einer festen Folge von Schritten: überflüssige Leerzeichen, leere und doppelte Zeilen entfernen, suchen und ersetzen (auch mit regulären Ausdrücken), Buchstaben groß oder klein schreiben, sortieren und nummerieren.
* **ColorTools** nimmt Farben vom Bildschirm oder aus Bildern auf, rechnet sie in gängige Schreibweisen von Hex bis OKLCH um, prüft den Kontrast nach WCAG und sammelt Farben in Paletten, die sich in verbreiteten Formaten austauschen lassen.

## Datenschutz

Localis verarbeitet deine Dateien ausschließlich auf deinem Rechner, benötigt kein Konto und enthält keine Telemetrie; es überträgt weder Dateien noch Einstellungen oder Angaben zur Nutzung. Was Localis selbst speichert, etwa Einstellungen, eigene Profile, Farbpaletten und heruntergeladene Updates, liegt im Ordner `%LOCALAPPDATA%\Localis`. Alle Werkzeuge funktionieren ohne Internetverbindung.

Eine Verbindung ins Internet stellt Localis nur für Updates her: Es ruft bei GitHub eine kleine Datei mit den Angaben zur neuesten Version ab und lädt von dort auch die Installationsdatei eines Updates. Diese Anfragen enthalten weder eine Kennung noch die installierte Version. GitHub sieht dabei, wie bei jedem Abruf aus dem Internet, deine IP-Adresse, den Zeitpunkt und die abgerufene Datei; außerdem zählt GitHub die Downloads jeder Datei und macht diese Zahlen ohne Bezug zu Personen öffentlich abrufbar.

## Updates

Beim ersten Start fragt Localis auf der Startseite, ob es automatisch nach Updates suchen soll oder nur, wenn du in den Einstellungen „Jetzt prüfen“ wählst; bis zu deiner Antwort stellt es keine Verbindung her. Die automatische Suche prüft etwa einmal am Tag, solange Localis geöffnet ist. Unter Einstellungen → Updates lässt sich die Wahl jederzeit ändern.

Ein verfügbares Update erscheint mit seinen Neuigkeiten auf der Startseite. Heruntergeladen wird es erst auf deinen Klick, installiert erst nach deiner Bestätigung. Localis schließt sich dafür und startet danach neu; deine Einstellungen und alles, was du in Localis angelegt hast, bleiben erhalten. Die Angaben zu jeder Version, darunter Größe und Prüfsumme der Installationsdatei, signiere ich mit einem Schlüssel, der nicht auf GitHub liegt. Localis prüft diese Signatur, bevor es ein Update anbietet, und vergleicht die heruntergeladene Datei vor der Installation mit den signierten Angaben; bei jeder Abweichung wird nichts installiert.

Bei „Versionen“ in denselben Einstellungen sollte „Stabile Versionen“ gewählt bleiben. Testfassungen (Beta) enthalten neue Funktionen schon vor ihrer Freigabe und sind entsprechend weniger erprobt.

## Deinstallieren

Öffne in Windows Einstellungen → Apps → Installierte Apps, wähle bei Localis das Menü „…“ und dann „Deinstallieren“. Entfernt werden das Programm, seine Verknüpfungen und heruntergeladene Updates. Anschließend fragt die Deinstallation, ob auch Einstellungen, eigene Profile und Farbpaletten gelöscht werden sollen; vorgewählt ist „Nein“, damit eine spätere Installation sie weiterverwenden kann. Dateien, die du mit Localis in eigenen Ordnern gespeichert hast, bleiben in jedem Fall erhalten.

## Bekannte Grenzen

* Localis gibt es derzeit nur auf Deutsch.
* CutOut arbeitet mit klassischen Verfahren der Bildverarbeitung, nicht mit KI. Bei Autos und unruhigem Hintergrund ist deshalb oft Nacharbeit von Hand nötig.
* SketchTools zeichnet nach, was im Bild zu sehen ist; neue Details oder den Stil eines bestimmten Künstlers erzeugt es nicht. Bilder mit mehr als 4000 Pixeln an der langen Seite werden dafür verkleinert.
* Ungefragt überschreibt Localis keine Datei. Lässt du jedoch eine vorhandene Datei ersetzen, sei es über die Rückfrage von Windows beim Speichern oder in CutOut über die Einstellung „Früheres Ergebnis ersetzen“, wird sie endgültig überschrieben und nicht in den Papierkorb verschoben.
* FileRename ändert die Namen der Dateien direkt, und „Rückgängig“ steht nur zur Verfügung, bis Localis geschlossen wird. Probiere es deshalb zuerst an der Kopie eines Ordners aus.
* Fotos im Format HEIC (etwa vom iPhone) oder AVIF liest Localis nur, wenn die nötigen Erweiterungen von Windows aus dem Microsoft Store installiert sind: die Bilderweiterung für HEIF und zusätzlich die Videoerweiterung für HEVC beziehungsweise AV1. Fehlt eine davon, nennt Localis sie beim Öffnen mit Namen.

## Rückmeldungen

Ich freue mich über jede Rückmeldung, ganz gleich, worum es geht: Ideen für völlig neue Werkzeuge oder Bereiche, Vorschläge zur Verbesserung bestehender Funktionen, Fehler oder Stellen, an denen die Bedienung unklar ist. Welche Werkzeuge bereits geplant sind, zeigt der Abschnitt „Was noch kommt“ auf der Startseite von Localis.

Schreib mir am besten direkt auf dem Weg, über den du den Link zu dieser Seite bekommen hast. Hilfreich sind die Versionsnummer (Einstellungen → Über Localis) und bei Fehlern ein Bildschirmfoto.

## Hinweise

Localis wird ohne Gewähr bereitgestellt; die Nutzung erfolgt auf eigene Verantwortung. Sichere wichtige Dateien, bevor du sie bearbeitest, und installiere Localis auf beruflich genutzten Rechnern nur mit Zustimmung der zuständigen IT. Die Installationsdatei darf nur unverändert und unentgeltlich weitergegeben werden. Localis enthält Bestandteile anderer Hersteller, die unter ihren eigenen Lizenzen stehen. Die Lizenztexte liegen nach der Installation im Programmordner im Unterordner `licenses`, wo die Datei `LIESMICH.txt` eine Übersicht aller Bestandteile gibt.
