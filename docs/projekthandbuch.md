# Nachbarhand – Projekthandbuch

Oct 25, 2026 · @Alexander Hirsekorn

## Überblick

Nachbarhand vermittelt geprüfte Helfer für Alltagsaufgaben in der Nachbarschaft und verdient 15 % Provision an jedem Auftrag, der über die App läuft. Damit sich das trägt, muss die App für beide Seiten so viel Nutzen bringen, dass niemand an ihr vorbei abrechnen will.

- **Zielgruppe:** ältere Menschen, vor allem aber Angehörige, die für sie Aufträge anlegen, und Berufstätige ohne Zeit. Die App wird ausdrücklich nicht als Rentner-App vermarktet.
- **Beispiele für Aufträge:** Rasen mähen, Hund ausführen, Einkaufen, Begleitung zum Arzt, kleine Reparaturen, Hilfe am Computer.
- **Kernidee der Bedienung:** Der Assistent (eine Alleskönner-Figur mit Werkzeuggürtel, die aus einer Lampe aufsteigt) fragt im Dialog alles ab. Die Helfer finden Aufträge auf einem Monitor mit Filter, schlagen einen Preis vor und besiegeln den Auftrag per Handschlag.
- **Stand 25.10.2026:** Name steht, erste klickbare Mockups sind gebaut ([Mockups ansehen](https://claude.ai/artifact/QmPPE7rqwjs5Bt7mRpQeZq)). Es gibt noch keinen Code, keine Firma und kein Budget.

## Projektplan

Vorschlag: Pilot in einer Stadt ab April 2027, Ausbau in weitere Städte erst, wenn der Pilot die Gewinnschwelle von rund 1.300 Aufträgen im Monat erreicht. Die Termine sind Annahmen und hängen davon ab, wer die App baut.

> **Projektplan (4 Phasen, 3 Prüfpunkte):** Die Grafik ist nur in der [Online-Version des Handbuchs](https://claude.ai/artifact/LjmEC3wqi8KE2JkTok7LfA) zu sehen.

Jede Phase endet mit einem Prüfpunkt. Erst wenn er erreicht ist, beginnt die nächste Phase.

## Funktionen

Der Kern ist ein Auftrag, der von der Anfrage bis zur Bezahlung komplett in der App bleibt. Jeder Schritt erzeugt Daten, die für Abrechnung, Versicherung und Statistik gebraucht werden.

### Auftrag anlegen und vergeben

1. Kunde oder Angehöriger beschreibt im Dialog, was gebraucht wird („Ich muss Rasen mähen“).
2. Der Assistent fragt Ort, Umfang, Zeitpunkt und Preisrahmen ab und zeigt eine Zusammenfassung.
3. Nach dem Absenden erscheint der Auftrag im Helfer-Monitor, filterbar nach Entfernung, Art, Zeit und Preis.
4. Ein Helfer nimmt den Preis an oder macht einen Gegenvorschlag. Der Kunde bestätigt.
5. Handschlag: „Auftrag ist platziert“. Erst jetzt sehen beide die genaue Adresse und den Vornamen.

### Regelmäßige Aufträge

- Ein Auftrag kann als Serie angelegt werden, zum Beispiel „jeden Freitag 15 bis 16 Uhr Hund ausführen“.
- Der Helfer übernimmt die ganze Serie und sieht sie in seinem Wochenplan. So kann er sich aus mehreren Serien einen festen Plan aufbauen.
- Einzelne Termine lassen sich absagen oder an einen Vertretungshelfer geben, ohne die Serie zu beenden.
- Serien sind der wichtigste Hebel gegen Umgehung: Wer jede Woche über die App bucht, braucht einen guten Grund, sie zu verlassen.

### Auftrag beginnen und beenden

- Vor Ort tippt der Helfer auf **Auftrag beginnen**. Die App gleicht seinen GPS-Standort mit der Auftragsadresse ab (zum Beispiel Umkreis 150 m), so wie es OnLogist bei Fahrzeugüberführungen macht.
- Liegt er außerhalb, kann er trotzdem starten, der Auftrag wird aber markiert und der Kunde gefragt.
- Mit **Auftrag beenden** wird wieder der Standort geprüft und die Dauer gespeichert. Optional lädt der Helfer ein Foto hoch (gemähter Rasen).
- Der Kunde oder Angehörige bekommt beim Beginn und beim Ende eine Mitteilung. Gerade Angehörige, die weit weg wohnen, wissen dann, dass jemand da war.

### Erinnerung bei vergessenem Abschluss

- Ist das Zeitfenster vorbei und der Auftrag nicht beendet, fragt die App den Helfer: „Ist der Auftrag erledigt?“
- Antwortet er nicht, folgt nach einer Stunde eine zweite Erinnerung und danach eine Frage an den Kunden.
- Wurde der Auftrag gar nicht begonnen, fragt die App beide Seiten, ob er ausgefallen ist, und bietet einen Ersatzhelfer an.

### Bezahlung und Bewertung

- Der Kunde hinterlegt beim ersten Auftrag ein Zahlungsmittel. Abgebucht wird erst nach dem Beenden, die Provision wird automatisch einbehalten.
- Beide Seiten bewerten sich. Helfer mit vielen Aufträgen und guten Bewertungen stehen im Monitor weiter oben.

## Plattformbindung: warum alles über die App läuft

Verbieten lässt sich die Umgehung kaum, sie muss sich für beide Seiten schlicht nicht lohnen. Rover und Taskrabbit lösen das mit Schutz, der nur bei Buchung über die Plattform gilt. Das ist auch für Nachbarhand der stärkste Hebel.

### Was der Kunde nur über die App bekommt

- **Absicherung:** Haftpflicht für Schäden, die der Helfer verursacht, gilt nur bei gebuchten und per GPS begonnenen Aufträgen.
- **Geprüfte Helfer:** Ausweis, Führungszeugnis und Bewertungen. Außerhalb der App fällt diese Sicherheit weg.
- **Nachweis für Angehörige:** Mitteilung bei Beginn und Ende, Dauer, Foto. Das ist der Kern des Versprechens an Angehörige.
- **Ersatz bei Ausfall:** Fällt der Helfer aus, schlägt die App einen anderen vor.
- **Rechnung:** Eine ordentliche Rechnung, zum Beispiel für die Steuerermäßigung für haushaltsnahe Dienstleistungen (§ 35a EStG) oder später für den Entlastungsbetrag der Pflegekasse.

### Was der Helfer nur über die App bekommt

- **Sichere Bezahlung:** Das Geld ist vor dem Auftrag reserviert, kein Hinterherlaufen.
- **Eigene Absicherung:** Unfall- und Haftpflichtschutz während des Auftrags.
- **Ranking:** Nur Aufträge in der App zählen für Bewertungen und Platzierung, also für künftige Aufträge.
- **Wochenplan und Serien:** Planbare Einnahmen aus regelmäßigen Aufträgen.

### Technische und vertragliche Maßnahmen

- Telefonnummern und E-Mail bleiben verborgen. Der Chat läuft in der App und erkennt Nummern oder „ruf mich an“ und weist freundlich auf den Schutz hin.
- Die Adresse wird erst nach dem Handschlag angezeigt.
- In den AGB steht ein Abwerbeverbot für 12 Monate nach dem ersten Kontakt, ersatzweise eine Ablösegebühr. Das ist rechtlich zu prüfen.
- Bei Serien sinkt die Provision, zum Beispiel ab dem 10. Termin auf 10 %. So lohnt sich der Wechsel nach draußen noch weniger.
- Auffällige Muster werden sichtbar: Eine Serie, die plötzlich endet, obwohl beide gut bewertet haben, löst eine kurze Nachfrage aus.

## Bezahlung und Provision

Empfehlung: Bezahlt wird grundsätzlich in der App über einen Zahlungsdienstleister für Marktplätze, der das Geld automatisch aufteilt. Der Helfer bekommt 85 %, Nachbarhand behält 15 %. So macht es auch OnLogist, und wir müssen nie einer Provision hinterherlaufen.

### So läuft es in der App

1. Beim Handschlag wird der Betrag beim Kunden reserviert, noch nicht abgebucht.
2. Nach **Auftrag beenden** wird abgebucht. Der Dienstleister zahlt dem Helfer 85 % aufs Konto aus und schreibt uns 15 % gut.
3. Der Kunde kann mit Karte, PayPal, Apple Pay, Google Pay oder SEPA-Lastschrift zahlen. PayPal läuft dann *innerhalb* der App, nicht privat von Konto zu Konto.
4. Bei Serien wird jeder Termin einzeln nach dem Beenden abgebucht. Angehörige können ihr eigenes Zahlungsmittel hinterlegen.

Geeignete Anbieter sind zum Beispiel Stripe Connect, Mollie Connect oder Mangopay. Sie übernehmen die Identitätsprüfung der Helfer für die Auszahlung und haben die nötige Zahlungslizenz, wir brauchen also keine eigene. Welche Zahlarten jeder Anbieter genau unterstützt und was er kostet, ist noch zu prüfen.

### Wenn doch bar bezahlt wird

Bargeld lässt sich nicht ganz verhindern, gerade bei älteren Kunden. Dafür gibt es zwei einfache Wege:

- **Provision per Lastschrift vom Helfer:** Jeder Helfer erteilt bei der Registrierung ein SEPA-Lastschriftmandat. Markiert er einen Auftrag als „bar bezahlt“, ziehen wir die 15 % einmal im Monat von seinem Konto ein. So machen es Fahrdienste wie Uber oder Bolt bei Barfahrten.
- **Verrechnung mit dem Guthaben:** Hat der Helfer auch App-Aufträge, wird die offene Bar-Provision einfach von seiner nächsten Auszahlung abgezogen.

Damit Barzahlung die Ausnahme bleibt:

- Versicherungsschutz und Ersatz bei Ausfall gelten nur bei Zahlung in der App.
- Nur bei Zahlung in der App gibt es eine Rechnung, mit der der Kunde die Steuerermäßigung für haushaltsnahe Dienstleistungen nutzen kann. Dafür verlangt das Finanzamt ohnehin eine unbare Zahlung, bar bezahlte Leistungen zählen nicht.
- Baraufträge zählen nicht für Bewertung und Ranking des Helfers.
- Für Kunden ohne Karte und Konto-App: Angehörige zahlen, oder einmalig SEPA-Lastschrift per Formular einrichten.

Gar nicht abgefangen wird damit der Fall, dass Kunde und Helfer sich ganz außerhalb der App verabreden. Dagegen helfen nur die Vorteile und Maßnahmen aus dem Abschnitt oben.

## Helferprüfung und regionale Administratoren

Jeder Helfer wird vor dem ersten Auftrag von einem Menschen freigegeben. Das schützt ältere Kunden und ist zugleich das wichtigste Verkaufsargument gegenüber Kleinanzeigen und Nachbarschaftsgruppen.

### Ablauf der Freigabe

1. Helfer registriert sich und lädt hoch: Ausweis, erweitertes Führungszeugnis, bei Bedarf Nachweise (Führerschein, Erste-Hilfe-Kurs, Gewerbeschein).
2. Automatische Prüfung von Ausweis und Selfie durch einen Dienstleister.
3. Der regionale Administrator prüft die Unterlagen und führt ein kurzes Video- oder Persönlichgespräch.
4. Freigabe des Helfers, zunächst mit einer Probephase (zum Beispiel die ersten 5 Aufträge mit Nachfrage beim Kunden).
5. Das Führungszeugnis wird alle 2 Jahre erneuert.

### Rolle der regionalen Administratoren

- Ein Freiberufler pro Großstadt oder Region, abgerechnet pro Freigabe und mit einer kleinen Monatspauschale.
- Aufgaben: Helfer freigeben, bei Beschwerden vermitteln, lokale Werbung (Seniorentreffs, Vereine, Kirchengemeinden, Hausverwaltungen).
- Start mit 1 Administrator in der Pilotstadt, der Gründer kann diese Rolle anfangs selbst übernehmen.
- Später Richtwert: 1 Administrator pro etwa 300 bis 500 aktive Helfer (Annahme, noch nicht geprüft).

## Statistik und Nachfrageauswertung

Weil jeder Auftrag mit Kategorie, Ort, Zeit, Preis und Dauer durch die App läuft, sehen wir laufend, wofür Hilfe gebraucht wird. Daraus leiten wir neue Schwerpunkte und Dienstleistungen ab.

- **Nachfrage je Kategorie und Region:** Welche Hilfe wird wo am häufigsten angefragt (Hund, Garten, Einkauf, Begleitung, Technik)?
- **Unerfüllte Nachfrage:** Aufträge, die keinen Helfer finden. Sie zeigen, wo Helfer fehlen und wo der Administrator gezielt werben sollte.
- **Preisniveau:** Durchschnittlicher Preis und tatsächliche Dauer je Kategorie (aus GPS-Beginn und -Ende). Damit schlägt der Assistent künftig realistische Preise vor.
- **Saison und Wochentage:** etwa Gartenarbeit im Frühjahr, Schneeräumen im Winter, Hundeausführen freitags.
- **Bindung:** Anteil der Serienaufträge, Wiederbuchungen beim selben Helfer, abgebrochene Serien als Warnsignal für Umgehung.
- **Freitext aus dem Dialog:** Wünsche, die in keine Kategorie passen, werden gesammelt. Häufen sie sich, wird daraus eine neue Kategorie.

Alle Auswertungen laufen anonymisiert und zusammengefasst, nie auf einzelne Kunden bezogen (DSGVO).

## Konkurrenz und Preisniveaus

Die 15 % Provision liegen im Marktrahmen: Rover nimmt je 15 % von Kunde und Sitter, Helpling bis zu einem Drittel. Keiner der Anbieter deckt die Mischung aus Alltagshilfe, geprüften Helfern und Nachweis für Angehörige ab.

| Anbieter | Schwerpunkt | Preisniveau für Kunden | Gebührenmodell |
| --- | --- | --- | --- |
| [Rover](https://www.rover.com/de/mulheim-an-der-ruhr--nordrhein-westfalen--gassi-service/) | Hundesitting, Gassi | 11 bis 19 € pro Spaziergang, im Schnitt 14 € (Beispiel Mülheim) | 15 % Buchungsgebühr für Kunden, Sitter behalten 85 % ([Rover-Hilfe](https://help-ch.rover.com/hc/en-gb/articles/35769539813908)) |
| [Careship](https://careship.de/preise/pflegekasse) | Alltagshilfe für Senioren | ab 33 € pro Stunde | Agenturpreis, teils direkte Abrechnung mit der Pflegekasse |
| [Helpling](https://www.test.de/Putz-Portale-im-Test-4767070-5381379/detail/2018237000!3/) | Reinigung | etwa 15 bis 21 € pro Stunde (Stand Test 2018) | bis zu ein Drittel Provision vom Helfer |
| [Taskrabbit](https://www.taskrabbit.com/press/release/taskrabbit-announces-launch-into-germany) | Montage, Umzug, Handwerk (IKEA-Tochter) | Stundensatz des Taskers | Servicegebühr in Prozent plus Trust-&-Support-Gebühr ([Taskrabbit-Hilfe](https://support.taskrabbit.com/hc/en-gb/articles/204411610)) |
| [Betreut.de](https://www.erfahrungen.com/mit/betreut-de/kosten-preise-premiummitgliedschaft-kontakt-aufnehmen/) | Kinder-, Senioren-, Tierbetreuung | frei verhandelt | Abo für Kontaktaufnahme, keine Provision. Preis nicht geprüft |
| [MyHammer](https://www.erfahrungen.com/mit/myhammer/gebuehren-auftraege-kostenlos/) | Handwerker | Angebote der Handwerker | für Kunden kostenlos, Handwerker zahlen. Höhe nicht geprüft |
| nebenan.de | Nachbarschaftsnetz | meist kostenlos | keine Vermittlung oder Bezahlung (aus dem Gedächtnis, nicht geprüft) |

**Wichtig für Nachbarhand:** Pflegebedürftige ab Pflegegrad 1 haben einen Entlastungsbetrag von bis zu 131 € im Monat ([Careship](https://careship.de/preise/pflegekasse)). Den können sie aber nur für anerkannte Angebote zur Unterstützung im Alltag einsetzen. Eine Anerkennung wäre ein starkes Argument für Angehörige und ist als offene Frage vermerkt.

Preise abgerufen am 25.10.2026.

## Kalkulation

Bei 1.000 Aufträgen à 20 € im Monat macht Nachbarhand noch rund 500 € Verlust. Die Gewinnschwelle liegt bei etwa 1.300 Aufträgen in einer Stadt, ab 5.000 Aufträgen bleiben gut 2.600 € im Monat. Alle Kosten sind grobe Schätzungen und müssen mit echten Angeboten ersetzt werden.

### Pro Auftrag

| Posten | Betrag |
| --- | --- |
| Auftragswert | 20,00 € |
| Provision 15 % (inkl. 19 % USt) | 3,00 € |
| davon Umsatzsteuer | −0,48 € |
| Zahlungsabwicklung (etwa 1,5 % + 0,25 €) | −0,55 € |
| **Deckungsbeitrag pro Auftrag** | **1,97 €** |

Die Zahlungsgebühr ist ein Richtwert aus dem Gedächtnis für europäische Karten bei Anbietern wie Stripe. Bei kleinen Aufträgen frisst sie fast ein Fünftel der Provision.

### Monatliche Kosten und Ergebnis nach Größe

| Posten pro Monat | 1.000 Aufträge, 1 Stadt | 5.000 Aufträge, 3 Städte | 20.000 Aufträge, 10 Städte | 50.000 Aufträge, 25 Städte |
| --- | --- | --- | --- | --- |
| Umsatz der Helfer (Auftragswert) | 20.000 € | 100.000 € | 400.000 € | 1.000.000 € |
| Deckungsbeitrag (1,97 € je Auftrag) | 1.970 € | 9.850 € | 39.400 € | 98.500 € |
| Server, Karten-API, Push | 150 € | 400 € | 1.200 € | 2.500 € |
| Wartung und Weiterentwicklung | 800 € | 2.000 € | 6.000 € | 12.000 € |
| Anwalt und Steuerberater | 300 € | 500 € | 1.000 € | 2.000 € |
| Versicherung | 250 € | 600 € | 2.000 € | 4.500 € |
| Identitätsprüfung neuer Helfer | 50 € | 120 € | 500 € | 1.200 € |
| Regionale Administratoren | 425 € | 1.500 € | 5.750 € | 14.000 € |
| Kundensupport | 0 € | 600 € | 3.000 € | 6.000 € |
| Marketing | 500 € | 1.500 € | 6.000 € | 15.000 € |
| App-Stores | 10 € | 10 € | 10 € | 10 € |
| **Kosten gesamt** | **2.485 €** | **7.230 €** | **25.460 €** | **57.210 €** |
| **Ergebnis vor Steuern** | **−515 €** | **+2.620 €** | **+13.940 €** | **+41.290 €** |

### Annahmen

- Ein aktiver Helfer erledigt etwa 10 Aufträge im Monat, jeden Monat kommen rund 12 bis 15 % neue Helfer zur Freigabe dazu.
- Administratoren: 200 € Pauschale pro Stadt plus 15 € pro Freigabe.
- Wartung: anfangs ein Freiberufler mit etwa 10 Stunden im Monat, ab 20.000 Aufträgen ein angestellter Entwickler.
- Einmalkosten für die Entwicklung der ersten Version, AGB, Datenschutz und Firmengründung sind nicht enthalten. Ein Gründergehalt auch nicht.

### Hebel

- **Servicegebühr für Kunden:** 1,49 € pro Auftrag (auch bei Rover und Taskrabbit zahlen Kunden eine Servicegebühr) brächte netto etwa 1,25 € mehr je Auftrag. Bei 1.000 Aufträgen wäre die App damit im Plus.
- **Höherer Auftragswert:** Bei 30 € statt 20 € steigt der Deckungsbeitrag auf etwa 3,10 €.
- **Serien:** senken Marketing- und Freigabekosten pro Auftrag, weil Kunden und Helfer bleiben.

## Offene Fragen

### Plattformbindung und Recht

- [ ] Ist ein Abwerbeverbot mit Ablösegebühr in den AGB gegenüber Privatkunden wirksam?
- [ ] Sind Helfer selbstständig, Minijobber oder Nachbarschaftshelfer? Wie vermeiden wir Scheinselbstständigkeit?
- [ ] Brauchen Helfer ab einem bestimmten Umsatz einen Gewerbeschein, und wer weist sie darauf hin?
- [ ] Welche Versicherung gibt es für Plattformen (Gruppenhaftpflicht für Helfer, Unfallschutz), und was kostet sie wirklich?
- [ ] Wer haftet, wenn beim Auftrag etwas passiert: Helfer, Plattform oder Versicherung?
- [ ] Ab wann brauchen wir als Zahlungsvermittler eine Lizenz, oder reicht ein Anbieter wie Stripe Connect?
- [ ] Welcher Zahlungsdienstleister passt (Stripe Connect, Mollie Connect, Mangopay): Gebühren, PayPal-Unterstützung, Auszahlung an Privatpersonen?
- [ ] Erlauben wir Barzahlung überhaupt, und wenn ja: Provision per Lastschrift vom Helfer?

### Angebot und Preise

- [ ] Provision nur vom Helfer, oder zusätzlich eine Servicegebühr vom Kunden?
- [ ] Lohnt sich die Anerkennung als Angebot zur Unterstützung im Alltag, damit Kunden den Entlastungsbetrag von 131 € nutzen können? Was verlangt das Bundesland dafür?
- [ ] Gibt es einen Mindestpreis pro Auftrag, damit Helfer nicht unter Wert arbeiten?
- [ ] Welche Kategorien gibt es zum Start, und welche schließen wir aus (Pflege, Medikamente, Auto fahren)?

### Betrieb

- [ ] In welcher Stadt starten wir den Pilot?
- [ ] Wie finden und bezahlen wir die regionalen Administratoren, und wer prüft deren Arbeit?
- [ ] Welcher GPS-Radius gilt beim Beginnen und Beenden, und was passiert bei schlechtem Empfang?
- [ ] Wie gehen wir mit Kunden ohne Smartphone um? Reicht es, wenn Angehörige alles in der App erledigen?
- [ ] Wer baut die App: selbst, Freiberufler oder Agentur? Und mit welchem Budget?
