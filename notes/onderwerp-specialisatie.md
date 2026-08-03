# Onderwerp specialisatie: AI & Data Engineering

## Gekozen onderwerp
Kostenoptimalisatie van LLM-agenttoepassingen in productieomgevingen.

## Concreet probleem (bron)
Zhang et al. (2025, NeurIPS) tonen aan dat bestaande LLM-cachingtechnieken
(context caching, semantische caching) ontworpen zijn voor chatbot-toepassingen
en tekortschieten bij AI-agenttoepassingen, omdat de output van een agent
afhangt van externe data en omgevingscontext. Hierdoor blijven de operationele
kosten en de latency van agenttoepassingen onnodig hoog. Zij tonen met hun
eigen oplossing (Agentic Plan Caching) een gemiddelde kostenreductie van
50,31% en een latencyreductie van 27,28% aan, wat het probleem en de
haalbaarheid van een oplossing bevestigt (citationkey: Zhang2025).

Dit is het concrete, benoemde probleem waarop dit onderzoeksvoorstel is
gebaseerd, in plaats van een algemene vraag over LLM-kosten.

## Concreet bedrijf (bron)
Om het probleem te verankeren in een specifieke bedrijfscontext, gebruikt het
voorstel Uber als openingsvoorbeeld. Uber gaf in april 2026 aan dat het
volledige jaarbudget voor AI-tools al opgebruikt was, ondanks een R&D-uitgave
van 3,4 miljard dollar in 2025. Volgens CTO Praveen Neppalli Naga kwam dit
door een sterke stijging van het gebruik van AI-coding-agents zoals Claude
Code en Cursor, waarbij ongeveer 11% van de live backend-code intussen door
AI-agenten geschreven wordt (bron: Yahoo Finance/Benzinga, citationkey:
Jain2026, oorspronkelijk gerapporteerd door The Information). Dit is een
gedocumenteerd, naam-en-toenaam voorbeeld van precies het probleem dat Zhang
et al. (2025) technisch beschrijven, en maakt de doelgroep concreet:
engineering- en platformteams bij bedrijven die AI-coding-agents op schaal
inzetten.

## Probleemstelling
Bedrijven die AI-agenten inzetten in productieomgevingen kampen met hoge en
moeilijk te voorspellen operationele kosten. Klassieke cachingtechnieken, die
wel goed werken bij chatbots, houden onvoldoende rekening met het meerstaps-
en contextafhankelijke karakter van agenttoepassingen. Daarnaast bestaan er
aanvullende technieken zoals prompt-compressie en model-routing, maar een
overzicht dat deze technieken specifiek afweegt voor agenttoepassingen
ontbreekt. IT-professionals die agenttoepassingen ontwikkelen hebben daardoor
weinig onderbouwde houvast bij het maken van een keuze.

## Hoofdonderzoeksvraag
Welke combinatie van kostenoptimalisatietechnieken (agentgeschikte caching,
prompt-compressie en model-routing) is het meest geschikt voor een
platformteam zoals dat van Uber, om de operationele kosten van AI-coding-agents
in een productieomgeving te verlagen, zonder de kwaliteit van de output
significant te verminderen?

De hoofdvraag verwijst nu expliciet naar Uber als bedrijfscontext (naast de
titel en de inleiding), op vraag van de groep. Dit blijft een open vraag
(geen ja-neevraag, geen opzoekvraag), zoals de rubric vereist.

## Deelvragen probleemdomein
- Waarom schieten klassieke context- en semantische caching specifiek tekort
  bij LLM-agenttoepassingen?
- Welke factoren bepalen de kostenstructuur van LLM-agenttoepassingen (bv.
  aantal planningsstappen, promptlengte, modelkeuze per stap)?
- Welke risico's ontstaan wanneer kosten verlaagd worden zonder rekening te
  houden met de specifieke werking van agenttoepassingen?

## Deelvragen oplossingsdomein
- Hoe werkt agentgeschikte caching (bv. het cachen van planstructuren in
  plaats van volledige antwoorden) en wanneer levert dit kostenbesparing op?
- In welke mate is prompt-compressie toepasbaar op de planningsstappen van
  een agent?
- Hoe werkt model-routing voor agenttoepassingen en welke tools ondersteunen
  dit?
- Hoe kan de impact van deze technieken op kosten en kwaliteit gemeten en
  vergeleken worden bij agenttoepassingen?

## Waarom dit onderwerp geschikt is
Het onderwerp vertrekt vanuit een concreet, met naam benoemd probleem uit een
recente, peer-reviewed publicatie (NeurIPS 2025), verankerd in een
naam-en-toenaam bedrijfsvoorbeeld (Uber), in plaats van een brede vraag. Het
raakt aan architectuur en prestatie-evaluatie, is meetbaar (kosten, latency,
kwaliteit zijn kwantificeerbaar), en biedt ruimte voor een eigen technische
bijdrage via een proof-of-concept. Er zijn voldoende kwalitatieve bronnen
beschikbaar.

## SMART-toetsing
- **Specific**: beperkt tot drie met naam benoemde technieken (agentgeschikte
  caching, prompt-compressie, model-routing) binnen één concreet probleem
  (kostenbeheersing bij AI-coding-agents).
- **Measurable**: kostenbesparing, latency en kwaliteitsbehoud zijn
  kwantificeerbaar, zowel uit de literatuur als uit de eigen PoC.
- **Achievable**: gebaseerd op publiek beschikbare tools, frameworks en
  gepubliceerde datasets, geen interne bedrijfsdata nodig.
- **Realistic/Relevant**: het probleem is recent aangetoond in peer-reviewed
  onderzoek en doet zich voor bij een publiek gedocumenteerd bedrijf (Uber).
- **Time-bound**: volledige aanpak (literatuurstudie, PoC, eindredactie)
  uitgewerkt binnen 12 weken (1 semester), zie fasering hieronder.

## Methodologie: fasering (12 weken) en technisch luik
Vier fasen, elk twee tot vier weken, samen passend binnen de beschikbare 12
weken van dit onderzoekstraject.

Fase 1 (weken 1 tot 3) richt zich op het probleemdomein: via
literatuuronderzoek wordt uitgezocht waarom caching tekortschiet bij agenten,
met als milestone een probleembeschrijving inclusief kostenanalyse.

Fase 2 (weken 4 tot 6) richt zich op het oplossingsdomein vanuit de
literatuur: caching, prompt-compressie en model-routing worden beschreven en
vergeleken, met als milestone een literatuurgebaseerd afwegingskader.

Fase 3 (weken 7 tot 10) is het technisch/praktisch luik: agentgeschikte
caching wordt zelf geïmplementeerd op een testscenario en gemeten
(tokenverbruik, kost, latency), met als milestone de gemeten PoC-resultaten.
Dit vult het cesuur-criterium "technische component, geen louter
theoretisch/academisch werk" in.

Fase 4 (weken 11 tot 12) is de synthese: literatuur en PoC worden samengebracht
tot een afwegingskader, met als milestone het eindrapport.

## Specifieke doelgroep
Platformteams en engineering-leads bij middelgrote tot grote
softwareorganisaties die verantwoordelijk zijn voor de interne uitrol en het
kostenbeheer van AI-coding-agents (bv. Claude Code, Cursor). Dit is dus niet
"IT-professionals" in het algemeen, maar specifiek de teams die de
infrastructuurkeuzes rond agentgebruik maken.

## Bronnen (in `prep/references.bib`)
Acht bronnen verzameld en individueel geverifieerd (bestaan echt, auteurs en
titel en jaar gecontroleerd op de bronpagina zelf), via de kanalen die de
cursus (Hoofdstuk 2, Informatie en bronnen) aanbeveelt: wetenschappelijke
databanken en AI-research-assistenten, aangevuld met arXiv-preprints en een
actueel nieuwsbericht op basis van eigen zoekwerk naar een concreet
bedrijfsvoorbeeld.

Jain2026 is een nieuwsbericht (Yahoo Finance/Benzinga) over Uber's AI-budgetprobleem
en dient als concreet bedrijfsvoorbeeld. Zhang2025 is peer-reviewed conference
proceedings (NeurIPS 2025), namelijk Agentic Plan Caching, en vormt het
kernprobleem rond caching bij agenten. Jiang2023 is een arXiv-preprint,
LLMLingua, over prompt-compressie. Regmi2024 is een arXiv-preprint, GPT
Semantic Cache, over caching. Liu2025 is een arXiv-preprint, Semantic Caching
for Low-Cost LLM Serving, eveneens over caching. Dekoninck2024 is een
arXiv-preprint, A Unified Approach to Routing and Cascading for LLMs, over
model-routing. Chen2024 is een peer-reviewed tijdschriftartikel (TMLR),
FrugalGPT, over caching, routing en prompt-adaptatie. Zhen2025 is peer-reviewed
conference proceedings (ACL/INLG 2025), Taming the Titans, met een overzicht
van kostenefficiëntie.

Bewust een mix van brontypes opgenomen, niet enkel preprints. De cursusrubric
beoordeelt expliciet diversiteit in brontype naast kwaliteit (CRAAP-test). De
dummy-bronnen (Moore2002, LewisFowler2014, Hykes2013) in `references.bib`
horen bij de placeholder-tekst van het LaTeX-template en zijn niet langer
relevant nu de echte hoofdtekst geschreven is.

## Volgende stappen
1. Informatiezoekopdracht formeel afronden (luik 1, luik 2a, luik 2b) en
   bevindingen loggen in de activiteitenlog.
2. Methodologie verder concretiseren: welke experimentele resultaten uit de
   literatuur precies vergeleken worden, en op welke criteria.
3. Onderwerp 2 (interprofessioneel/maatschappelijk) kiezen en uitwerken,
   eveneens vertrekkend vanuit een concreet, benoemd probleem.
