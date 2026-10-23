# Localis

**Kleine, kostenlose Werkzeuge für Windows – alles bleibt auf Ihrem Computer.**

Localis ist ein privates Hobbyprojekt von grammok – gedacht für Freunde und Bekannte, keine offizielle Software. Diese
Fassung ist eine **Vorschau**: Es kann noch hier und da haken, und mit Updates ändert sich noch einiges.

## Herunterladen

**[Localis für Windows herunterladen](https://github.com/grammok/localis/releases/latest/download/Localis-Setup.exe)**
(Setup-Datei, ca. 45 MB)

- Windows 11, 64 Bit. Windows 10 ab Version 1809 sollte gehen, ist aber nicht getestet.
- Installiert wird nur für Ihr Benutzerkonto – ohne Administratorrechte.
- Alle Versionen mit Neuigkeiten und Prüfsummen: [Releases](https://github.com/grammok/localis/releases). Die Einträge
  „Source code“ dort legt GitHub selbst an – sie werden nicht gebraucht.

### Warnungen beim ersten Start

Localis ist nicht mit einem gekauften Zertifikat signiert. Deshalb warnen Browser und Windows beim ersten Mal:

- Der Browser meldet eventuell, die Datei werde nicht häufig heruntergeladen. Dann „Behalten“ wählen (in Edge über
  „…“ neben dem Download).
- Windows zeigt eventuell „Der Computer wurde durch Windows geschützt“. Dann auf „Weitere Informationen“ und
  „Trotzdem ausführen“ klicken.

Wer sichergehen möchte, dass die Datei unverändert ist, vergleicht vorher die Prüfsumme:

1. PowerShell öffnen (im Startmenü „PowerShell“ eintippen).
2. Eingeben: `Get-FileHash "$env:USERPROFILE\Downloads\Localis-Setup.exe"`
3. Der angezeigte Wert muss zur Zeile `Localis-Setup.exe` in der Datei `SHA256SUMS` des
   [neuesten Release](https://github.com/grammok/localis/releases/latest) passen (Groß- und Kleinschreibung spielen
   keine Rolle).

## Was drin ist

- **CutOut** – den Hintergrund aus Fotos und Grafiken entfernen, mit Werkzeugen für saubere Umrisse.
- **ImageBatch** – viele Bilder auf einmal verkleinern, drehen und umwandeln; die Originale bleiben unverändert.
- **FileRename** – viele Dateien nach Regeln umbenennen, mit Vorschau und „Rückgängig“.
- **HashTools** – mit Prüfsummen prüfen, ob ein Download oder eine Sicherung unverändert ist.
- **PasswordGenerator** – sichere Passwörter, Passphrasen und PINs erzeugen, ohne sie zu speichern.
- **QrTools** – QR-Codes für Text, Links, WLAN, Kontakte und mehr.
- **TextTools** – Text bereinigen, sortieren, doppelte Zeilen entfernen, suchen und ersetzen.
- **ColorTools** – Farben vom Bildschirm aufnehmen, umrechnen und als Paletten sammeln.

## Datenschutz

Localis arbeitet offline: Ihre Dateien bleiben auf Ihrem Computer. Es gibt keine Telemetrie, kein Konto, keine Werbung
und keine KI. Ins Internet geht Localis nur für Updates – von selbst nur, wenn Sie die automatische Suche einschalten.
Dabei ruft es eine kleine Datei hier bei GitHub ab; GitHub sieht, wie bei jeder Webseite, Ihre IP-Adresse, den
Zeitpunkt und welche Datei abgerufen wird. Localis sendet keine Kennung und nichts über Sie oder Ihre Dateien. GitHub
zählt außerdem, wie oft eine Datei heruntergeladen wurde – nur die Zahl, ohne Namen; sie ist öffentlich abrufbar.

## Updates

Beim ersten Start fragt Localis einmal, ob es automatisch nach Updates suchen darf (etwa einmal am Tag) oder nur, wenn
Sie selbst „Jetzt prüfen“ wählen. Ein neues Update erscheint auf der Startseite; geladen und installiert wird es erst
auf Ihren Klick. Updates sind abgesichert: Localis installiert nur, was zu einer mit meinem Schlüssel signierten
Update-Information passt (Größe und Prüfsumme).

In den Einstellungen unter „Updates“ bitte **„Stabile Versionen“** lassen. Die Testfassungen (Beta) sind nur zum
Mittesten gedacht und können Fehler enthalten.

## Deinstallieren

Windows-Einstellungen → Apps → Installierte Apps → Localis → Deinstallieren. Dabei fragt Localis, ob Ihre Einstellungen
und selbst angelegten Farbpaletten mit entfernt werden sollen (vorgewählt: „Nein“, sie bleiben).

## Bekannte Grenzen

- Nur auf Deutsch.
- Nicht signiert – daher die Warnungen oben.
- Vorschau: Es kann noch Fehler geben.
- CutOut: Bei Autos und unruhigem Hintergrund braucht es oft noch Handarbeit (Rechteck, „Teil wählen“, Pinsel).
- Ersetzen beim Speichern: Wählen Sie, dass eine vorhandene Datei ersetzt wird (Rückfrage von Windows beim Speichern, in
  CutOut auch die Einstellung „Früheres Ergebnis ersetzen“), wird sie endgültig überschrieben – nicht über den
  Papierkorb. Das gilt für alle Werkzeuge; ImageBatch ersetzt nie.
- FileRename: zuerst mit der Kopie eines Ordners ausprobieren; „Rückgängig“ geht nur, bis Localis geschlossen wird.
- HEIC- und AVIF-Fotos (z. B. vom iPhone) liest Localis nur mit den passenden Bilderweiterungen von Windows.
- Auf Dienst- oder Firmenrechnern bitte nur mit Erlaubnis Ihrer IT installieren.

## Rückmeldungen

Fehler gefunden oder eine Idee? Sagen Sie mir gern direkt Bescheid – auf dem Weg, auf dem Sie den Link bekommen haben,
am besten mit einem Bildschirmfoto und der Version (Einstellungen → Über Localis).

## Hinweise

Localis ist ein privates, kostenloses Hobbyprojekt – ohne Gewähr, die Nutzung erfolgt auf eigene Verantwortung.
Localis überschreibt Originale nie ungefragt; sichern Sie wichtige Dateien trotzdem, bevor Sie sie bearbeiten. Die
Setup-Datei darf nur unverändert und kostenlos weitergegeben werden. Localis enthält Bestandteile anderer Hersteller
unter deren eigenen Lizenzen; die Texte liegen nach der Installation im Programmordner im Ordner „licenses“.
