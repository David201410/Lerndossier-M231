# Der eigene Passwort-Manager
In diesem Auftrag geht es darum, einen geeigneten Passwortmanager für uns auszusuchen. Dabei lernen wir, worauf wir bei der Auswahl eines geeigneten, achten müssen.

## Austausch
Da ich diese Aufgabe relativ spät mache, konnte ich den Austausch nicht mit jemandem machen, der so weit ist wie ich. Aus diesem Grund führte ich das Gespräch mit Davud.

**Was uns bei einem Passwortmanager wichtig ist:**
- Wir möchten einen Manager, den wir auf verschiedenen Plattformen nutzen können, wie z.B. IOS, Android, Windows und Linux. Denn wenn man ihn nur am Computer nutzen kann, können wir unsere Passwörter auf dem Handy nur schlecht verwenden, wenn sie komplex sind.
- Es wäre praktisch wenn es im Manager einen Passwort Generator gibt. Damit können wir komplexe Passwörter einfach und schnell generieren. Die meisten, oder sagen wir die seriösen, Passwort-Manager nutzen auch bestimmte Algorithmen für diese Passwörter.

## Vergleich
- In den Kriterien liegen wir richtig mit Synchronisation und automatische Sperre. Jedoch gibt es noch viele Punkte, über die wir nicht nachdachten. 
- Kriterien wie ein verfügbarer Quellcode oder Brute-Force-Schutz sind natürlich sehr wichtig, soweit haben wir jedoch nicht gedacht.

## Eigenen Passwortmanager auswählen
Nun starte ich damit einen Passwortmanager auszusuchen. Dafür definiere ich als erstes meine Anforderungen für den Manager.

- **Anforderung Synchronisation**: Der Manager sollte für mich mindestens auf meinem Handy und auf meinem Laptop verfügbar sein.
- **Anforderung Open-Source**: Wenn der Quellcode des Programms frei verfügbar ist, wird das Programm sicherer, weil mehr Leute diesen kontrollieren und verbessern können.
- **Anforderung Verschlüsselungsalgorithmus**: Der Manager sollte einen sicheren Algorithmus wie AE-256 oder ChaCha20 verwenden und nicht sowas wie MD-5.
- **Anforderung Ablageort Datenbank**: Kann ich meine Daten Lokal und in der Cloud speichern?

|                | **SecureSafe** | **Wertung** | **lastpass** | **Wertung** | **Bitwarden** | **Wertung** |
|----------------|-------------|---------------|-------------|---------------|-------------|---------------|
| Link | [securesafe.com](https://www.securesafe.com) | |[lastpass.com](https://lastpass.com) | | [bitwarden.com](https://bitwarden.com) | |
| Verschlüsselung | AES256 | ✓ | AES256 | ✓ | AES256 | ✓ |
| OpenSource | Nicht verfügbar | ╳ | Ist verfügbar | ✓ | Ist verfügbar | ✓ |  
| Synchronisation | Ja ausser Linux | ✓ | Ja (Linux Add On) | ✓ | Ja | ✓ |
| Ablageort Datenbank | Schweizer Cloud | ╳ | Nur in der Cloud | ╳ | Beides möglich, lokal aber kompliziert | ✓ / ╳ |

**Die Entscheidung fällt für mich auf:**
![](/images/bitwarden_logo.png)

Anhand der verschiedenen Kriterien war die Entscheidung nicht ganz einfach. Ich bin jedoch ein Fan von Bitwarden's Design und seinem Ruf.

## Passwortmanager einrichten
- **Was werde ich tun, wenn ich mein Master-Passwort vergesse?** Ich muss in erster Linie dafür sorgen, dass das gar nicht erst passiert. Das Passwort an einem sicheren Ort speichern oder sich aufschreiben würde ich sagen.
- **Wie erstelle ich ein Backup von meiner Passwortdatenbank?** Als erstes brauche ich ein Speichermedium. Danach muss ich den Bitwarden Vault exportieren, wo ich das Backup in .json bzw. Encrypted speichern kann. Bevor ich das aber machen kann, muss ich mein Speichermedium formatieren. Am besten mit dem exFAT Format zusammen mit dem GUID Partition Table.