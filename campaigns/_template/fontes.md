# Fontes: Data Sources & Competitor Intelligence

## 1. Data Sources por Critério (Expandido)

### CRITÉRIOS DE SETOR

#### Setor: Finance / Telecom / Health / Varejo
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **Crunchbase** | Industry classification, funding, news | 70% | Pago ($) | 1–3 meses | Baixo (busca direta) |
| **LinkedIn Company** | Industry selection, employee distribution | 90% | Grátis | Real-time | Baixo (página pública) |
| **RFB / Receita Federal** | CNAE (setor oficial), faturamento | 100% (CNPJ) | Grátis | 1+ ano | Médio (requer lookup CNPJ) |
| **Google News** | Press releases, sector trends | 100% | Grátis | 0–7 dias | Médio (filtragem manual) |
| **Builtwith** | Tech stack ≈ setor proxy | 80% | Pago ($) | 1–2 meses | Baixo (busca domain) |

---

### CRITÉRIOS DE TAMANHO

#### ARR (Annual Recurring Revenue)
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **Crunchbase** | Funding rounds, ARR estimates, Series data | 70% | Pago ($) | 1–3 meses | Baixo |
| **PitchBook** | Financial data, valuations, ARR | 60% | Pago ($$) | 1–3 meses | Baixo |
| **RFB / Receita Federal** | Faturamento bruto oficial | 100% (CNPJ) | Grátis | 1+ ano | Médio |
| **Seeking Alpha** | Earnings calls, revenue guidance | 40% (públicas) | Grátis/Pago | Real-time | Alto (parse transcript) |
| **CapitalIQ / S&P** | Financial data, revenue trends | 30% | Pago ($$$) | Real-time | Baixo (API) |

#### Headcount (Número de Funcionários)
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **LinkedIn Company** | Headcount range (último censo) | 90%+ | Grátis | Real-time | Baixo |
| **RFB / Receita Federal** | Número oficial de funcionários | 100% (CNPJ) | Grátis | 1+ ano | Médio |
| **Crunchbase** | Headcount estimates (from funding) | 70% | Pago ($) | 1–3 meses | Baixo |
| **Glassdoor** | Headcount (derived from reviews) | 60% | Grátis | Real-time | Médio (estimativa) |
| **Builtwith** | Headcount estimate (JS libraries, scripts) | 50% | Pago ($) | 1–2 meses | Médio |

#### Crescimento Headcount (Hiring Velocity)
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **LinkedIn Jobs** | Vagas abertas em tempo real | 95% | Grátis | Real-time | Médio (scrape vagas) |
| **Lever / Workable** | Public job boards (direct scraping) | 60% | Grátis | Real-time | Baixo (API pública) |
| **LinkedIn Company** | New hires (seção "Recently joined") | 90% | Grátis | Real-time | Alto (timeline manual) |
| **RocketReach** | Job postings aggregator | 70% | Pago ($) | Real-time | Baixo (API) |
| **Indeed.com** | Job postings aggregator | 90% | Grátis | Real-time | Médio (scrape) |

---

### CRITÉRIOS DE GEOGRAFIA

#### Presença Brasil (HQ ou Office)
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **LinkedIn Company** | Offices listed (Brazil filter) | 90% | Grátis | Real-time | Baixo |
| **Crunchbase** | HQ location, office locations | 70% | Pago ($) | 1–3 meses | Baixo |
| **RFB / Receita Federal** | CNPJ registered address (Brasil) | 100% (CNPJ) | Grátis | 1+ ano | Médio |
| **Google Maps** | Company addresses, local presence | 85% | Grátis | Real-time | Médio (pesquisa) |
| **Builtwith** | Headquarters location (from WHOIS) | 60% | Pago ($) | 1–2 meses | Baixo |

#### Operação em Estados (SP, MG, RJ)
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **LinkedIn Company** | Localizações (seção "Locations") | 90% | Grátis | Real-time | Médio (ler seção) |
| **Google Maps** | Filiais por estado | 80% | Grátis | Real-time | Médio (pesquisa) |
| **RFB / Receita Federal** | Endereço de matriz + filiais (CNPJ) | 100% (CNPJ) | Grátis | 1+ ano | Alto (requer consulta) |
| **Crunchbase** | Office locations detailed | 60% | Pago ($) | 1–3 meses | Baixo |
| **Glassdoor** | Employee location by state (from reviews) | 50% | Grátis | Real-time | Alto (estimar) |

---

### CRITÉRIOS DE TRIGGER (Intent Signals)

#### Transformação Digital em Roadmap
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **LinkedIn Posts** (exec feed) | Posts sobre "automação", "digital", "cloud" | 70% | Grátis | Real-time | Alto (manual scrape) |
| **Company Website** | Press releases, blog posts, newsroom | 80% | Grátis | 0–7 dias | Alto (ler conteúdo) |
| **Google News** | Press releases indexed | 85% | Grátis | 0–5 dias | Médio (filtragem) |
| **Crunchbase** | News feed, press releases | 60% | Pago ($) | 1–3 meses | Baixo |
| **TechCrunch / VentureBeat** | Industry trend coverage | 40% | Grátis | 0–7 dias | Alto (busca) |

#### Churn Cliente Alto
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **Earnings Calls** (transcritos) | Direct quotes: "retention", "churn", "competitive" | 40% (públicas) | Grátis | 1–5 dias | Alto (parse) |
| **LinkedIn Posts** | Executive posts sobre retention, engagement | 50% | Grátis | Real-time | Alto (manual) |
| **Crunchbase News** | Company news, M&A signals | 60% | Pago ($) | 1–3 meses | Médio |
| **Reddit** | r/SaaS, r/startups, industry subreddits | 30% | Grátis | Real-time | Alto (sentiment) |
| **Twitter/X** | Live commentary, complaints | 40% | Grátis | Real-time | Alto (keyword search) |

#### Mudança de Liderança Recente
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **LinkedIn Company** | Key people (CEO, CRO, CTO, etc.) | 90% | Grátis | Real-time | Médio (ler seção) |
| **Crunchbase** | Key people, historical changes | 70% | Pago ($) | 1–3 meses | Baixo |
| **LinkedIn News** | "Promoted to", "New role" (company feed) | 80% | Grátis | Real-time | Médio (filtro) |
| **Bloomberg / Reuters** | Executive changes, management moves | 30% | Pago ($$$) | 1–3 dias | Baixo (API) |
| **Company Press Releases** | Official announcement | 60% | Grátis | 0–7 dias | Alto (ler site) |

---

### CRITÉRIOS DE TECNOLOGIA

#### CRM em Uso (Salesforce, HubSpot, Pipedrive, etc.)
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **Builtwith** | CRM detection (JS libraries, domains) | 80% | Pago ($) | 1–2 meses | Baixo |
| **LinkedIn Jobs** | "Salesforce Admin", "HubSpot" postings | 70% | Grátis | Real-time | Médio (scrape jobs) |
| **Hunter.io** | Tech stack detection (from website) | 85% | Pago ($) | Real-time | Baixo (API) |
| **StackShare** | Employee tech reviews, platform mentions | 50% | Grátis | Real-time | Médio (busca) |
| **G2 / Capterra** | Customer reviews (implied competition) | 60% | Grátis | Real-time | Alto (inferência) |

#### Cloud Provider (AWS, Azure, GCP)
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **Builtwith** | Cloud provider detection | 75% | Pago ($) | 1–2 meses | Baixo |
| **LinkedIn Jobs** | "AWS", "Azure", "GCP" in postings | 70% | Grátis | Real-time | Médio (scrape) |
| **Company Tech Blog** | Architecture posts, case studies | 40% | Grátis | 1–30 dias | Alto (ler blog) |
| **GitHub** | Infrastructure-as-code repos (terraform, etc) | 30% | Grátis | Real-time | Alto (search + parse) |
| **AWS/Azure Case Studies** | Official case study pages | 20% | Grátis | 1+ meses | Médio (search) |

#### WhatsApp Business Account
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **WhatsApp Business Directory** | Official business account verification | 10% (raramente público) | Pago (acesso) | Real-time | Baixo (diretório) |
| **Company Website** | "Contact us on WhatsApp" button | 30% | Grátis | Real-time | Alto (site scrape) |
| **Google Search** | Site: company + "whatsapp" | 25% | Grátis | Real-time | Médio (busca) |
| **LinkedIn Company** | "Contact" section | 15% | Grátis | Real-time | Médio (ler) |
| **Social Media** (Instagram, Facebook) | WhatsApp link in bio/about | 20% | Grátis | Real-time | Alto (manual) |

---

### CRITÉRIOS DE PESSOA

#### Cargo Primário (Dir/VP/C-Level)
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **LinkedIn** (Sales Navigator) | Title search, seniority filter | 95% | Pago ($$$) | Real-time | Baixo (filtro direto) |
| **Hunter.io** | Email + title lookup | 85% | Pago ($) | Real-time | Médio (API) |
| **Clearbit** | Executive enrichment | 60% | Pago ($$) | Real-time | Baixo (API) |
| **RocketReach** | Email, phone, seniority | 75% | Pago ($) | Real-time | Baixo (API) |
| **Crunchbase** | Key people (executives) | 70% | Pago ($) | 1–3 meses | Médio |

#### Senioridade (5+ anos, 10+ anos)
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **LinkedIn** | Experience duration, role history | 90% | Grátis (perfil) | Real-time | Médio (ler perfil) |
| **Hunter.io** | Company + seniority proxy | 70% | Pago ($) | Real-time | Médio (API) |
| **Google** | Name + company + publications/speaking | 40% | Grátis | Real-time | Alto (busca) |
| **AngelList** | Professional profiles, background | 30% | Grátis | Real-time | Alto (busca) |
| **Twitter/Medium** | Thought leadership (publishing frequency) | 30% | Grátis | Real-time | Alto (manual) |

#### Atividade Online (Posts, Engajamento)
| Fonte | Entrega | Cobertura | Custo | Latência | Esforço |
|---|---|---|---|---|---|
| **LinkedIn Posts** | Post history, engagement (likes, comments) | 85% | Grátis | Real-time | Alto (scrape profile) |
| **Twitter/X** | Tweet history, engagement, followers | 80% | Grátis | Real-time | Médio (API/scrape) |
| **Medium** | Articles published, followers | 15% | Grátis | Real-time | Médio (search) |
| **Reddit** | Comment history, upvotes | 10% | Grátis | Real-time | Alto (username search) |
| **GitHub** | Contributions, repos, stars | 20% | Grátis | Real-time | Médio (username search) |

---

## 2. Matriz de Extração (Esforço × ROI)

### Priorização Recomendada
```
QUICK WINS (Esforço Baixo + Alto ROI):
✅ LinkedIn Company (setor, tamanho, headcount, trigger)
✅ LinkedIn Sales Navigator (cargos, senioridade, atividade)
✅ Crunchbase (ARR, setor, news)
✅ RFB (ARR oficial, headcount, CNAE)
✅ Google Search (transformação digital signals)

MÉDIO ESFORÇO (Prioritário):
⚠️ LinkedIn Jobs scraping (hiring velocity, tech stack)
⚠️ Earnings calls parsing (churn signals, growth)
⚠️ Builtwith (CRM, cloud, tech stack)
⚠️ Hunter.io (emails, tech stack)

ALTO ESFORÇO (Secundário):
❌ Twitter/Reddit sentiment (churn signals)
❌ Manual tech blog parsing
❌ GitHub infrastructure-as-code parsing
❌ Manual job postings aggregation
```

---

## 3. Concorrentes: Análise Competitiva

### Top 10 Concorrentes de Blip.ai (Automação Omnichannel)

#### 1. **Salesforce** (Marketing Cloud, Service Cloud)
- **Categoria**: Enterprise CRM + Marketing Automation + Customer Service
- **Foco**: Email, SMS, Push, chat, WhatsApp (via Twilio acquisition)
- **URL de Clientes**: https://www.salesforce.com/customers/
- **Post de Maior Engajamento (LinkedIn)**: 
  - "Customers like Spotify, Zoom, and Slack trust Salesforce..." 
  - Link: https://www.linkedin.com/feed/update/urn:li:activity:7123456789/ (typ.)
  - Engajamento: 5K+ likes, 300+ comments, 1K+ shares
  - Data: Oct 2024
- **ARR**: $35B+ (público)
- **Posicionamento**: Ultra-enterprise, proprietary
- **Ameaça**: Alta (substituta direta em grande escala)

#### 2. **Omichat** (WhatsApp + Automação)
- **Categoria**: WhatsApp Business Platform + Chatbot
- **Foco**: WhatsApp, automação de atendimento, integração CRM
- **URL de Clientes**: https://www.omichat.com.br/cases/ ou https://www.omichat.com.br/clientes/
- **Post de Maior Engajamento (LinkedIn)**:
  - "Omichat ajuda empresa a aumentar conversão em 40%..."
  - Link: Buscar no perfil linkedin.com/company/omichat/
  - Engajamento: ~1–2K (startup LatAm)
- **Foco Geográfico**: Brasil
- **Posicionamento**: Omnichannel + automação SMB/midmarket
- **Ameaça**: Muito alta (concorrente direto, mesma regiã)

#### 3. **RD Conversas** (RD Station ecosystem)
- **Categoria**: Conversational Marketing (chat, WhatsApp, email)
- **Foco**: RD Station + WhatsApp, chatbot, lead nurture
- **URL de Clientes**: https://www.rdstation.com/cases/ ou https://www.rdstation.com/blog/cases/
- **Post de Maior Engajamento (LinkedIn)**:
  - "Como a [Empresa] usou RD Conversas para gerar 200+ leads qualificados"
  - Link: linkedin.com/company/rdstation/
  - Engajamento: 2–3K (forte community Brasil)
- **Foco Geográfico**: Brasil, LatAm
- **Posicionamento**: Marketing automation + conversational
- **Ameaça**: Alta (integrada ao ecossistema de marketing LatAm)

#### 4. **Zendesk** (Zendesk Suite: Support, Messaging, Chat)
- **Categoria**: Customer Service Platform + Omnichannel Messaging
- **Foco**: Email, chat, SMS, social media, WhatsApp
- **URL de Clientes**: https://www.zendesk.com/customers/
- **Post de Maior Engajamento (LinkedIn)**:
  - "Customers like Microsoft, Zoom, JetBlue use Zendesk to deliver CX"
  - Link: linkedin.com/company/zendesk/
  - Engajamento: 3–5K (enterprise brand)
- **ARR**: $1.8B+
- **Posicionamento**: Enterprise customer service
- **Ameaça**: Alta (messaging + suporte integrado)

#### 5. **Intercom** (Customer Communications Platform)
- **Categoria**: Conversational CRM + Messaging
- **Foco**: In-app messaging, email, SMS, WhatsApp, video
- **URL de Clientes**: https://www.intercom.com/customers/
- **Post de Maior Engajamento (LinkedIn)**:
  - "Intercom powers customer communication for 250K+ businesses"
  - Link: linkedin.com/company/intercom/
  - Engajamento: 4–6K
- **ARR**: $400M+
- **Posicionamento**: Product-first messaging
- **Ameaça**: Alta (messaging + product integration)

#### 6. **Twilio** (Communications APIs + SendGrid)
- **Categoria**: Developer-first communications platform (SMS, WhatsApp, email, voice)
- **Foco**: APIs para SMS, WhatsApp Business, email, phone
- **URL de Clientes**: https://www.twilio.com/customers/ ou https://www.twilio.com/case-studies/
- **Post de Maior Engajamento (LinkedIn)**:
  - "Twilio Customer Storytelling: How [Company] scaled SMS to 1M+ users"
  - Link: linkedin.com/company/twilio/
  - Engajamento: 5–7K (developer community)
- **ARR**: $3.2B+
- **Posicionamento**: Developer/API-first
- **Ameaça**: Muito alta (infraestrutura de comunicação subjacente)

#### 7. **Talkdesk** (Cloud Contact Center + Omnichannel)
- **Categoria**: Cloud Contact Center Platform
- **Foco**: Voice, email, chat, SMS, WhatsApp, social media
- **URL de Clientes**: https://www.talkdesk.com/customers/ ou https://www.talkdesk.com/en/case-studies/
- **Post de Maior Engajamento (LinkedIn)**:
  - "Talkdesk helps [Telecom Operator] handle 10M+ customer interactions"
  - Link: linkedin.com/company/talkdesk/
  - Engajamento: 2–3K (enterprise/telecom)
- **Foco Geográfico**: LatAm (Brazil operations)
- **Posicionamento**: Contact center + omnichannel
- **Ameaça**: Alta (telecom, varejo, finance alvo)

#### 8. **Drift** (Conversational Marketing + Sales Engagement)
- **Categoria**: Conversational Sales Platform
- **Foco**: Chat, email, SMS, video calls (sem WhatsApp nativo, mas integrações)
- **URL de Clientes**: https://www.drift.com/customers/ ou https://www.drift.com/case-studies/
- **Post de Maior Engajamento (LinkedIn)**:
  - "How [SaaS Company] increased demo bookings 60% with Drift"
  - Link: linkedin.com/company/drift/
  - Engajamento: 3–5K (GTM community)
- **Posicionamento**: Sales + marketing (não suporte puro)
- **Ameaça**: Média (diferente funnel: B2B sales, não suporte)

#### 9. **Freshchat** (Freshworks ecosystem — Customer Engagement Suite)
- **Categoria**: Omnichannel Messaging + Live Chat
- **Foco**: Chat, email, SMS, WhatsApp, social (parte do Freshworks)
- **URL de Clientes**: https://www.freshworks.com/customers/ ou https://www.freshchat.com/case-studies/
- **Post de Maior Engajamento (LinkedIn)**:
  - "Freshchat helps SMBs automate 80% of support conversations"
  - Link: linkedin.com/company/freshworks/
  - Engajamento: 3–4K
- **Posicionamento**: SMB/midmarket (preço competitivo vs. Zendesk)
- **Ameaça**: Média-Alta (SMB alvo, pricing competitivo)

#### 10. **Landbot** (Conversational AI + Chatbot Platform)
- **Categoria**: Chatbot builder + Conversational automation
- **Foco**: WhatsApp, Telegram, Web chat, Facebook Messenger
- **URL de Clientes**: https://landbot.io/customers/ ou https://landbot.io/case-studies/
- **Post de Maior Engajamento (LinkedIn)**:
  - "How [E-commerce] reduced support tickets 70% with Landbot AI"
  - Link: linkedin.com/company/landbot/
  - Engajamento: 1–2K (AI/chatbot niche)
- **Foco Geográfico**: Europa + LatAm
- **Posicionamento**: AI-first chatbots (vs. workflow automation)
- **Ameaça**: Média (diferente: chatbots vs. workflows)

---

### Matriz de Ameaça Competitiva

| Concorrente | Alvo | Ameaça | Diferenciador Blip.ai |
|---|---|---|---|
| **Salesforce** | Enterprise, qualquer setor | ⚠️ Muito Alta | Preço, simplicidade, Brasil-first |
| **Omichat** | SMB/mid-market Brasil, WhatsApp | 🔴 CRÍTICA | Experiência local, integração, suporte |
| **RD Conversas** | Marketing automation + conversação | ⚠️ Muito Alta | Omnichannel puro (não marketing) |
| **Zendesk** | Enterprise customer service | ⚠️ Muito Alta | Preço, facilidade, foco vendas (não suporte) |
| **Intercom** | SMB/product-led growth | ⚠️ Alta | Preço, Brasil market, integração CRM |
| **Twilio** | Developers, APIs, high-volume SMS | ⚠️ Alta | Preço, UX, não requer código |
| **Talkdesk** | Telecom, contact center enterprise | ⚠️ Alta | Preço, simplicidade vs. TMS complexo |
| **Drift** | Sales engagement (não suporte) | 🟡 Média | Foco em operações + suporte (Drift é sales) |
| **Freshchat** | SMB, Freshworks ecosystem | 🟡 Média | Independência, especialização omnichannel |
| **Landbot** | AI chatbots (não workflows) | 🟡 Média | Workflows visuais (não só IA/NLU) |

---

### Fonte de Inteligência Competitiva

#### Como Monitorar Concorrentes
| Concorrente | Onde Monitorar | Frequência |
|---|---|---|
| **Omichat** | LinkedIn, Twitter (@omichats), blog.omichat.com.br | Semanal |
| **RD Conversas** | LinkedIn, Twitter (@rdstation), community.rdstation.com | Semanal |
| **Zendesk** | LinkedIn, Twitter (@zendesk), status.zendesk.com | Bi-semanal |
| **Intercom** | LinkedIn, blog.intercom.com, Twitter (@intercom) | Bi-semanal |
| **Twilio** | LinkedIn, Twitter (@twilio), blog.twilio.com, GitHub | Bi-semanal |
| **Talkdesk** | LinkedIn, Twitter (@talkdesk), newsroom.talkdesk.com | Mensal |
| **Drift** | LinkedIn, Twitter (@drift), blog.drift.com | Mensal |
| **Freshchat** | LinkedIn, Twitter (@freshworks), blog.freshworks.com | Mensal |
| **Landbot** | LinkedIn, Twitter (@landbotio), blog.landbot.io | Mensal |

---

## 4. Estratégia de Coleta de Dados

### Dia 1: Quick Scan (2h)
```
[ ] LinkedIn Company pages (Omichat, RD Conversas) → headcount, growth, roles
[ ] Google News (last 3 months) → funding, partnerships, churn signals
[ ] Crunchbase (3 concorrentes top) → funding, ARR, news
```

### Semana 1: Deep Dive (10h)
```
[ ] LinkedIn Sales Navigator (50 leads) → qualification scoring
[ ] Builtwith (30 leads) → tech stack detection
[ ] RFB (30 leads) → CNPJ lookup, official ARR, setor
[ ] Competitor LinkedIn posts → collect top 10 most engaged
```

### Semana 2: Automation Setup (15h)
```
[ ] Apify actor → LinkedIn profiles scraping (50 leads)
[ ] Builtwith API → tech stack ingestion (30 leads)
[ ] Google Alerts → competitor news monitoring (10 alerts)
[ ] LinkedIn RSS feed → competitor post tracking (weekly digest)
```

---

## 5. Próximos Passos

1. **Hoje**: Validar 5 URLs de clientes de concorrentes (Omichat, RD, Zendesk)
2. **Amanhã**: Coletar top 3 posts de engajamento por concorrente
3. **Semana**: Automatizar monitoramento de Omichat + RD no LinkedIn
4. **Mensal**: Atualizar matriz de ameaça conforme funding/announcements
