# GEO/AEO-checklist: gevonden worden in ChatGPT, Copilot en Google AI-overzichten

Praktische checklist (Nederlands) om je website vindbaar en citeerbaar te maken voor AI-zoekmachines. Gebaseerd op officiële documentatie en wat we zelf op [joepify.nl](https://www.joepify.nl) hebben toegepast. Laatst gecontroleerd: 22 oktober 2026.

> Niemand kan een vermelding in ChatGPT of AI-overzichten garanderen. Deze checklist haalt de technische en inhoudelijke drempels weg.

## 1. Toegang voor AI-crawlers
- [ ] **robots.txt** staat de zoekbots toe: `OAI-SearchBot` (ChatGPT search), `ChatGPT-User`, `PerplexityBot`, `Claude-SearchBot`, `bingbot`, `Googlebot`. Training-bots (`GPTBot`, `ClaudeBot`, `CCBot`, `Google-Extended`) zijn een aparte keuze. Bronnen: [OpenAI bots](https://platform.openai.com/docs/bots), [Google common crawlers](https://developers.google.com/search/docs/crawling-indexing/google-common-crawlers)
- [ ] **Test wat bots écht krijgen**: een firewall, CDN of host kan een 403 geven terwijl robots.txt de bot toelaat. Tool: [ai-crawler-access-check](https://github.com/Joepify/ai-crawler-access-check)
- [ ] **Geen JavaScript nodig** voor de hoofdtekst: de tekst staat in de HTML-bron.
- [ ] **UTF-8** als charset in de HTTP-header (anders worden € en é verminkt door simpele fetchers).

## 2. Google AI-overzichten
- [ ] Google stelt **geen extra eisen**: een pagina moet geïndexeerd zijn en in aanmerking komen voor een snippet. Je hebt geen speciale AI-bestanden of schema nodig. Bron: [Google: AI features and your website](https://developers.google.com/search/docs/appearance/ai-features)
- [ ] Geen `nosnippet` / `max-snippet:0` op pagina's die je in AI-antwoorden wilt.

## 3. Copilot en Bing
- [ ] Site verifiëren in **Bing Webmaster Tools**; het **AI Performance**-rapport toont citaties in Copilot. Bron: [Bing Webmaster Blog](https://blogs.bing.com/webmaster)
- [ ] **IndexNow** voor snelle indexering van nieuwe en gewijzigde pagina's: [indexnow.org](https://www.indexnow.org/)
- [ ] **Bing Places** (import uit Google Bedrijfsprofiel).

## 4. Content die AI kan citeren
- [ ] **Antwoord eerst**: direct onder de H1 een zin of blok van 35-45 woorden dat de hoofdvraag beantwoordt (wat, kosten, tijd, wie).
- [ ] **Koppen als vragen** die mensen echt stellen (Search Console en Google autocomplete).
- [ ] **Zelfstandige secties** van ongeveer 120-170 woorden; de eerste zin beantwoordt de kop zonder "dit" of "dat".
- [ ] **Cijfers en citaten met bron**: het GEO-onderzoek van Aggarwal e.a. (KDD 2024) vond tot 40% meer zichtbaarheid in generatieve antwoorden; statistieken, citaten en bronvermelding werkten het best, keyword stuffing niet. Bron: [arXiv 2311.09735](https://arxiv.org/abs/2311.09735)
- [ ] **Eigen data** (onderzoek, metingen): uniek en daardoor citeerbaar. Voorbeeld: [webshop-onderzoek-2026](https://github.com/Joepify/webshop-onderzoek-2026)
- [ ] **Zichtbare FAQ** met dezelfde tekst in FAQPage-schema.

## 5. Entiteit en structured data
- [ ] Eén **Organization/LocalBusiness**-entiteit met vaste `@id`, adres, telefoon, KvK, `sameAs` (LinkedIn, Google Maps, GitHub). Sjablonen: [schema-templates-nl](https://github.com/Joepify/schema-templates-nl)
- [ ] **Auteur** (Person) en **dateModified**, ook zichtbaar op de pagina.
- [ ] Prijzen in schema gelijk aan de prijzen op de pagina.

## 6. Bestanden voor AI-agents (optioneel)
- [ ] `llms.txt` (voorstel van [llmstxt.org](https://llmstxt.org/), geen standaard; Google gebruikt het niet) en eventueel `llms-full.txt`.
- [ ] RSS/Atom-feed voor blog en kennisbank.

## 7. Merk buiten je site
- [ ] Reviews (Google Bedrijfsprofiel en minstens één ander platform), vermeldingen in vakmedia, profielen op platforms die AI-antwoorden citeren (bijv. Sortlist, Trustoo, Clutch, LinkedIn).

Uitgebreide uitleg: https://www.joepify.nl/gevonden-worden-in-chatgpt · Gratis check: https://www.joepify.nl/website-apk

Licentie: CC BY 4.0. Gemaakt door [Joepify](https://www.joepify.nl), Rotterdam.
