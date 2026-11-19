---
name: discovery-plan
description: Maakt een discovery-plan via het intake-canvas (brandende vraag, aannames, prioriteit, modus, hypothese, deelnemers en methode, wat doen we met de uitkomst), in chat of vanuit een teamworkshop (foto van de poster of export van een board). Gebruik bij onderzoek opzetten, research plan, studie starten of een workshop verwerken.
---

# discovery-plan

Zet input om in `intake.md` en daarna in `plan.md` in de studiemap. Het team beslist; Copilot bereidt voor. Deze skill werft niemand, besteedt geen geld en neemt geen contact op met klanten of respondenten.

Uitgangspunten:
- Begin bij een vraag of aannames, niet bij een beslissing. De beslissing komt als laatste.
- Maak aannames expliciet en onderzoek de riskantste eerst.
- Leg vooraf vast wanneer je gelijk hebt (toetsen) of wanneer je klaar bent (verkennen).
- Gedrag boven mening. Zoek naar wat je ongelijk geeft, niet naar bevestiging.

## Regels voor data en compliance

Deze regels gaan voor alles hieronder.
- Zet nooit persoonsgegevens van klanten of respondenten in `intake.md`, `plan.md` of chat: geen namen, e-mailadressen, klantnummers of rekeningnummers. Gebruik rollen of codes (R01, R02).
- `deelnemers/` blijft buiten Git. Controleer dat `.gitignore` de regel `studies/*/deelnemers/*` bevat; voeg hem anders toe en meld dat.
- Stel geen externe tools, panels of platforms voor die de organisatie niet heeft goedgekeurd. Schrijf "goedgekeurde testtool" of "goedgekeurd panel" en zet de keuze onder open punten.
- Werving van eigen klanten gaat via de officiële kanalen van de organisatie. Noem in het plan dat consent en de interne privacyrichtlijnen gelden.
- Volg de dataclassificatie van de organisatie. Twijfel je of iets in de repo mag, vraag het en schrijf het niet op.

## Stap 1: Route bepalen

- **Chat:** iemand vult het canvas met Copilot in. Ga naar stap 2.
- **Workshop:** er is een foto van de poster of een export van een board als afbeelding toegevoegd. Ga naar stap 3.

De vakken, hulpvragen en methodekaart staan in `references/intake-canvas.md`. Het draaiboek voor een workshop staat in `references/workshop-draaiboek.md`.

## Stap 2: Chatroute

Haal eerst uit het gesprek wat er al is, en vraag kort naar de context als die ontbreekt: over welk product of welke flow gaat het, en wat zijn de tijd en het budget?

Loop daarna de zeven vakken in volgorde af. Stel hooguit twee vragen tegelijk. Laat na vak 3 en na vak 6 kort de tussenstand zien. Vul niets in wat de gebruiker niet zei: vraag het, of zet het onder open punten.

1. **Brandende vraag.** Wat wil je weten dat je nu niet weet? Benoem het type: behoefte, gebruikers, huidige oplossing, workflow, wil, bruikbaarheid of vindbaarheid. Is de vraag een oplossing in vermomming ("willen klanten feature X?"), herformuleer dan samen naar het onderliggende probleem.
2. **Aannames.** Wat denk je nu al? Vraag door tot er minimaal vijf zijn, verdeeld over bedrijf (waarde, kosten, kanaal, regelgeving) en klanten (wie, waarom, wanneer, wat ze nu doen). Schrijf ze als "We denken dat...".
3. **Prioriteren.** Scoor elke aanname op risico als hij niet klopt (hoog/laag) en bewijs nu (sterk/zwak). Hoog risico plus zwak bewijs gaat door, maximaal drie. Laat de gebruiker de keuze bevestigen.
4. **Modus.** Kan de gebruiker opschrijven wat hij denkt dat waar is? Ja: toetsen. Nee: verkennen.
5. **Hypothese of klaar-criterium.** Toetsen: "We denken dat [aanname] voor [wie]. Dat klopt als we [gedrag of signaal] zien bij [aantal of aandeel]." Verkennen: "We zijn klaar als we [...] kunnen beschrijven." Leg dit vast voordat er data is.
6. **Deelnemers en methode.** Maximaal twee segmenten op gedrag of aanleiding. Aantallen: usabilitytest 5 per segment, interviews 6 tot 8. Methode volgens de methodekaart. Nooit direct vragen naar toekomstig gedrag of betalingsbereidheid: vraag naar wat mensen nu doen. Een survey alleen bij een concrete telvraag.
7. **Wat doen we met de uitkomst?** Welke keuzes kan dit veranderen, wie moet het horen, en wanneer?

## Stap 3: Workshoproute

Bekijk de toegevoegde afbeelding en schrijf de post-its per vak over:
- De kleur van een post-it bepaalt de kolom bij aannames (bedrijf of klanten).
- De positie op de 2x2 bepaalt de prioriteit.
- Neem tekst letterlijk over. Verbeter geen formuleringen.
- Wat onleesbaar of dubbelzinnig is, krijgt `[?]`. Gok nooit.
- Lege vakken blijven leeg en komen onder open punten.
- Staan er persoonsgegevens op de foto, neem die dan niet over en meld het.

Stel daarna in chat alleen vragen over de `[?]`-punten en lege vakken, maximaal drie tegelijk.

## Stap 4: intake.md

Schrijf `studies/JJJJ-MM-<slug>/intake.md` volgens `references/intake-template.md`.

## Stap 5: plan.md

Maak `plan.md` in dezelfde map:

```markdown
# <Studienaam>

Status: plan · <datum> · eigenaar: <rol> · bron: <workshop of chat>

## Brandende vraag
<vraag> (type: <type>)

## Riskantste aannames
| Aanname | Kolom | Risico | Bewijs |
| --- | --- | --- | --- |

## Modus
Verkennen / toetsen, omdat ...

## Hypothese of klaar-criterium
- ...

## Methode
<methode> omdat <reden, gekoppeld aan het type vraag>.

## Deelnemers
- Segmenten: ...
- Aantal: ...
- Werving: goedgekeurd panel / eigen klanten via officiële kanalen
- Screenercriteria: moet ..., sluit uit ...
- Consent en privacy: volgens de interne richtlijnen

## Planning
| Stap | Datum |
| --- | --- |

## Wat doen we met de uitkomst
- Keuzes die dit kan veranderen: ...
- Wie moet het horen: ...
- Wanneer: ...

## Open punten
- ...
```

Controleer voor je afrondt:
- Kan de uitkomst nog iets veranderen? Zo niet: zeg dat eerlijk en stel voor de studie te schrappen of te verkleinen.
- Staat er al iets in eerdere studies (`studies/*/inzichten/`) dat de vraag beantwoordt?
- Staan er geen persoonsgegevens in de bestanden?

Zet daarnaast `status.md` met `fase: plan-klaar`, de datum en de volgende stap, en maak de mappen `instrumenten/`, `deelnemers/`, `sessies/`, `snapshots/`, `inzichten/` en `readout/` aan als ze er nog niet zijn.

## Afronden

Vat het plan in chat kort samen en stel voor het via een pull request te laten reviewen door het team. Begin geen volgende fase zonder akkoord.
