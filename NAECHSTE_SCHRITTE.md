# Hebräisch-Vokabeltrainer – Projektnotizen & nächste Schritte

> Diese Datei liegt im Projektordner (`ivrit`) als „Gedächtnis" zwischen den Sitzungen.
> Silvio: Zu Beginn der nächsten Sitzung einfach diese Datei **und** die aktuelle `index.html` anhängen – dann kann Claude nahtlos weitermachen.

## Was die App aktuell kann (Stand: dieser Meilenstein)
- **267 Wörter** (B1–C1), Hebräisch mit Nikud, deutsche Bedeutung, Wortart; Verben mit Binjan + Wurzel und **3 Beispielsätzen** mit rotierenden Formen (Person/Zahl/Zeit), Verb selbst im Infinitiv.
- **Spaced Repetition** (SM-2), Richtungen He→De und De→He, Modi Karteikarte / Multiple Choice / Schreiben.
- **„Übrig"-Zähler** (zählt die Runde runter), **Lernkalender** (Serie 🔥, Lerntage, Rekord), Fortschritt lokal im Browser + Export/Import.
- **Aussprache-Audio** (Carmit): fertige `.m4a`-Dateien im Ordner `audio/`, erzeugt auf dem Mac per `say -v Carmit`. **Wichtig gelernt: Audio MIT Nikud erzeugen** (nicht ohne!), sonst falsche Aussprache (z. B. „sha'ar" statt „se'ar").
- Gehostet über **GitHub Pages**: https://silviowenrix.github.io/ivrit/ — Repo `silviowenrix/ivrit`, Upload via **GitHub Desktop**.

## NÄCHSTER SCHRITT (Silvios Wunsch): C1-Konversations-Paket
Ziel B2 → C1 im **Sprechen**. Nicht nur Masse, sondern die *richtigen* Wörter. Grob ~1.500–2.500 zusätzliche **aktive** Wörter nötig – gezielt in diese Richtungen:

1. **Diskursmarker / Redegliederung** (machen sofort „C1-Sound"):
   - einerseits … andererseits – מִצַּד אֶחָד … מִצַּד שֵׁנִי
   - das hängt davon ab – זֶה תָּלוּי
   - im Gegenteil – לְהֵפֶךְ
   - mit anderen Worten – בְּמִלִּים אֲחֵרוֹת
   - trotzdem / dennoch – בְּכָל זֹאת / אַף עַל פִּי כֵן
   - vor allem – בְּעִקָּר · letztlich – בְּסוֹפוֹ שֶׁל דָּבָר
   - meiner Meinung nach – לְדַעְתִּי · soweit ich weiß – עַד כַּמָּה שֶׁאֲנִי יוֹדֵעַ
2. **Abstrakte Verben & Nomen** fürs Argumentieren/Meinen (einschätzen, betonen, andeuten, voraussetzen, Einfluss, Zusammenhang, Standpunkt, Beleg …).
3. **Kollokationen & feste Wendungen** (typische Wort-Kombinationen, nicht Einzelwörter).
4. **Idiome / Slang** in Maßen (wie מַחְזִיק אֶצְבָּעוֹת, אוֹכֵל סְרָטִים – gefällt Silvio).

→ Vorschlag: als **eigenes Paket „C1-Konversation"** anhängen (Verben mit 3 rotierenden Formen, Rest 1 Beispiel), danach Audio-Neuerzeugung nur für die neuen IDs.

## Wichtige Arbeitsregeln (damit nichts kaputtgeht)
- **Neue Wörter immer HINTEN anhängen**, bestehende IDs 1..N **nie** ändern → Fortschritt + Audio-Zuordnung bleiben stabil.
- Nach dem Anhängen: `index.html` neu bauen (VOCAB-Array ersetzen) + **Inkrement-Audio-Skript** nur für die neuen IDs (`w{id}.m4a`, `s{id}_{k}.m4a`), **mit Nikud**.
- Upload: neue Dateien in `ivrit`-Ordner → GitHub Desktop → Commit → Push. Danach ggf. Homescreen-Icon neu laden (Cache).
- Container wird zwischen Sitzungen geleert → Claude braucht am Anfang die **aktuelle index.html** als Grundlage.

## Ideen-Parkplatz (später, kein Muss)
- Daten aus `index.html` in separate `vocab.json` auslagern (sauberere Updates).
- „Alles-vorab-laden" für komplett offline verfügbares Audio.
- Kalender: Wochenstart wählbar, Jahresübersicht.
- Evtl. Umstieg auf Claude Code (läuft direkt im `ivrit`-Ordner, kein Neu-Anhängen nötig).
