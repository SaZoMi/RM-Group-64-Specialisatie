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
prompt-compressie en model-routing) is het meest geschikt om de operationele
kosten van LLM-agenttoepassingen in een productieomgeving te verlagen, zonder
de kwaliteit van de output significant te verminderen?

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
recente, peer-reviewed publicatie (NeurIPS 2025), in plaats van een brede
vraag. Het raakt aan architectuur en prestatie-evaluatie, is meetbaar (kosten,
latency, kwaliteit zijn kwantificeerbaar), en biedt ruimte voor een eigen
vergelijkende bijdrage. Er zijn voldoende kwalitatieve bronnen beschikbaar.

## Bronnen (in `prep/references.bib`)
Zeven bronnen verzameld en individueel geverifieerd (bestaan echt, auteurs en
titel en jaar gecontroleerd op de bronpagina zelf), via de kanalen die de
cursus (Hoofdstuk 2, Informatie en bronnen) aanbeveelt: wetenschappelijke
databanken en AI-research-assistenten, aangevuld met arXiv-preprints op basis
van eigen ervaring met dit onderwerp.

| Citationkey | Type | Bron | Onderwerp |
| :--- | :--- | :--- | :--- |
| Zhang2025 | peer-reviewed conference proceedings (NeurIPS 2025) | Agentic Plan Caching | kernprobleem: caching bij agenten |
| Jiang2023 | preprint (arXiv) | LLMLingua | prompt-compressie |
| Regmi2024 | preprint (arXiv) | GPT Semantic Cache | caching |
| Liu2025 | preprint (arXiv) | Semantic Caching for Low-Cost LLM Serving | caching |
| Dekoninck2024 | preprint (arXiv) | A Unified Approach to Routing and Cascading for LLMs | model-routing |
| Chen2024 | peer-reviewed tijdschrift (TMLR) | FrugalGPT | caching, routing, prompt-adaptatie |
| Zhen2025 | peer-reviewed conference proceedings (ACL/INLG 2025) | Taming the Titans: A Survey of Efficient LLM Inference Serving | overzicht kostenefficiëntie |

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
