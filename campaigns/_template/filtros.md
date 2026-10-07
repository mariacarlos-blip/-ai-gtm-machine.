# Filtros: Blip.ai ICP Search & Qualify

## Mapa de Critérios → Campo → Fonte Pública

Esta tabela mapeia cada **critério ICP** para um **campo busca-ável** (snake_case) e sua **fonte pública**. 
- **(!)** indica critério **sem fonte pública direta** — requer pesquisa manual ou contato.

---

## FILTROS EMPRESA

### Setor
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| Setor: Finance | `industry_naics_code` | Crunchbase, RFB (CNAE 6xxx) | Bancos, seguradoras, fintechs |
| Setor: Telecom | `industry_naics_code` | Crunchbase, ANATEL, RFB (CNAE 61xx) | Operadoras, ISPs |
| Setor: Health | `industry_naics_code` | Crunchbase, RFB (CNAE 86xx) | Saúde, hospitais, seguradoras saúde |
| Setor: Varejo | `industry_naics_code` | Crunchbase, RFB (CNAE 45-47) | Distribuição, e-commerce, franquias |

### Tamanho
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| ARR R$50M–R$500M | `annual_revenue_usd` | Crunchbase, RFB, PitchBook | Faturamento bruto; converter BRL→USD |
| Quadro 200–5.000 | `employee_count` | LinkedIn Company, Crunchbase, RFB | Último censo LinkedIn; RFB ≥1 ano atrás |
| Múltiplos departamentos | `organizational_depth` (!) | LinkedIn Company (página mostra "Employees"), Clearbit | Proxy: >100 em Sales, >50 em Ops, >50 em Marketing |
| Crescimento >20% a.a. | `revenue_growth_yoy` (!) | Crunchbase (funding rounds como sinal), Pitchbook, PythonicMQ | Sem fonte direta; use IPO/série recente como proxy |

### Geografia
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| Presença Brasil | `hq_country` + `offices_country` | LinkedIn Company, Crunchbase, RFB | HQ ou office registrada no Brasil |
| Operação em LATAM | `hq_country` + `offices_in_latam` | LinkedIn Company, Crunchbase | Presença confirmada em >1 país LatAm |
| Estados (SP, MG, RJ foco) | `offices_state` (!) | LinkedIn Company (seção Localizações), Google Maps "empresa" | Requer visita manual ao perfil |

### Modelo de Receita
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| Direto B2C ou B2B2C | `revenue_model` (!) | Site/pitch deck, Crunchbase "Business Model" | Raramente estruturado; ler homepage/deck |
| Recorrente (SaaS, subscription) | `revenue_model` (!) | Crunchbase, Pitchbook, site | Ler modelo de negócio explícito |
| Transacional (e-commerce, vendas) | `revenue_model` (!) | Site, earnings call transcripts, pitch | Ler público-alvo + produto |

### Trigger (Intent Signals)
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| Transformação digital em roadmap | `digital_transformation_mentions` (!) | LinkedIn (posts/news), website (press release), Clearbit (news feed) | Ler posts recentes de exec team |
| Churn cliente alto | `customer_churn_signals` (!) | Earnings calls (transcritos), LinkedIn posts | Palavras-chave: "retention", "churn", "engagement" |
| Crescimento de volume (contratações) | `hiring_velocity` | LinkedIn (vagas abertas, contratos), Lever/Workable public jobs | Scrape posições abertas em Sales/Ops/Marketing |
| Mudança de liderança recente | `executive_change_date` (!) | LinkedIn (histórico executivos), Crunchbase (key people), LinkedIn news | Filtrar <6 meses; novo exec = budget reset |
| Competitor adotou omnichannel (!) | `competitor_activity` (!) | LinkedIn (posts sobre automação, WhatsApp), Google News | Monitorar menção de Zendesk, Intercom, etc. |

### Tecnologia (Stack)
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| CRM em uso (Salesforce, HubSpot, etc.) | `crm_platform` | Builtwith, BuiltWith.com API, LinkedIn (job postings), Hunter (tech stack) | Scrape site; job titles com "Salesforce", "HubSpot" |
| Cloud-first (AWS, Azure, GCP) | `cloud_provider` | Builtwith, LinkedIn jobs, Crunchbase | Ler job postings; "AWS", "Azure", "GCP" em descrição |
| WhatsApp Business Account | `whatsapp_business_status` (!) | WhatsApp Business Directory (requer acesso), site empresa | Raramente público; call para confirmar |
| Integração ERP/SAP | `erp_platform` (!) | LinkedIn jobs ("SAP", "Oracle", "NetSuite"), Builtwith (rastreamento de ERP) | Raras no Builtwith; ler jobs |
| Legacy monolítico (RED FLAG) | `tech_modernization_level` (!) | LinkedIn (job postings), site (tech blog) | Red flag: zero cloud, zero API mention, "mainframe" mention |

---

## FILTROS PESSOA

### Cargo Primário (Economic Buyer)
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| Dir/VP Operações | `title_keywords` | LinkedIn (title search), Hunter, Clearbit | Keywords: "Director", "VP", "Chief", "Operations" |
| Dir/VP Vendas | `title_keywords` | LinkedIn, Hunter | Keywords: "Director", "VP", "Chief", "Sales", "Revenue" |
| Dir/VP Marketing | `title_keywords` | LinkedIn, Hunter | Keywords: "Director", "VP", "Chief", "Marketing" |
| CIO / CTO | `title_keywords` | LinkedIn, Hunter | Keywords: "Chief Information Officer", "CIO", "CTO", "Chief Technology" |
| Controla orçamento tech | `seniority_level` + `function` (!) | LinkedIn (nível sênior), Hunter (title) | Proxy: Dir+ ou VP+ |
| Autoridade integração CRM/ERP | `function_technology` (!) | LinkedIn (role details), Hunter profile | Ler descrição; "integração", "API", "stack" |

### Cargo Secundário (Champion)
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| Gerente de CRM / Automação | `title_keywords` | LinkedIn, Hunter | Keywords: "Manager", "CRM", "Automation", "Operations" |
| Analista de Operações | `title_keywords` | LinkedIn, Hunter | Keywords: "Analyst", "Operations", "Operations Excellence" |
| Especialista em Automação | `title_keywords` | LinkedIn, Hunter | Keywords: "Specialist", "Automation", "Marketing Automation" |
| Coordenador de Dados / BI | `title_keywords` | LinkedIn, Hunter | Keywords: "Coordinator", "Data", "Analytics", "BI" |

### Senioridade
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| 5–10 anos na função | `experience_years` | LinkedIn (durança em role atual + histórico) | LinkedIn field "Starts Year" – "Now" |
| 10+ anos (Senior) | `experience_years` | LinkedIn | Somar todos os roles similares |
| 2–5 anos na empresa | `tenure_current_company` | LinkedIn (data início na empresa) | Campo "Started" na seção "Experience" |
| Muito junior (<1 ano) | `experience_years` | LinkedIn | RED FLAG — baixa autoridade |

### Área Funcional
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| Operações / Transformação Digital | `function` | LinkedIn (title, company industry match) | Títulos com "Operations", "Transformation", "Process" |
| Vendas / Revenue Ops | `function` | LinkedIn, Hunter | Títulos com "Sales", "Revenue", "Go-to-Market" |
| Marketing / Demand Gen | `function` | LinkedIn, Hunter | Títulos com "Marketing", "Demand", "Demand Gen" |
| Customer Success / Suporte | `function` | LinkedIn, Hunter | Títulos com "Customer Success", "Support", "Onboarding" |

### Papel na Compra
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| Economic Buyer (aprova/assina) | `seniority_level` | LinkedIn (Dir+, VP+) | Proxy: nível sênior + função ops/sales |
| Champion (mobiliza internamente) | `engagement_signals` (!) | LinkedIn (atividade, posts sobre tema), website comportamento (!) | Ler posts recentes sobre automação/CRM |
| Influencer/Recommender | `engagement_signals` (!) | LinkedIn (engajamento em posts sobre categoria), Hunter | Ler atividade em posts de RD Station, Zendesk, etc. |
| Blocker (CISO, purista) | `role_risk` (!) | LinkedIn (título com Security, Privacy, Risk), job postings | RED FLAG: "Chief Security", "Chief Privacy" como stakeholder |

### Atividade & Intento
| Critério ICP | Campo (snake_case) | Fonte Pública | Notas |
|---|---|---|---|
| Publica sobre automação / ops / digital | `linkedin_activity` | LinkedIn (histórico posts últimos 6 meses) | Scrape profile; keywords: "automation", "digital", "omnichannel" |
| Engaja em posts sobre CRM / marketing automation | `linkedin_engagement` | LinkedIn (likes, comments, shares últimos 6 meses) | Scrape posts de RD Station, HubSpot, Zendesk |
| Pesquisa Google sobre WhatsApp Business / omnichannel | `search_intent` (!) | Google Ads (keyword search volume), Google Trends, Clearbit (news feed) | Indireta; monitor de campanhas paid awareness |
| Segue players da categoria (Zendesk, RD Station, etc.) | `follower_category_players` | LinkedIn (followers/following list) | Scrape seguindo-list; keywords "RD Station", "Zendesk", "Twilio" |
| Visitou site Blip.ai nos últimos 30 dias | `website_visitor` (!) | Leadfeeder, Clearbit, Demandbase | Requer pixel/MCP instalado; dados privados |
| Conectou com Blip em eventos / webinars | `event_attendance` (!) | Blip CRM (interno), LinkedIn "Events Attended" (!) | Interno; requer verificação manual |
| Zero atividade online (RED FLAG) | `online_presence_score` (!) | LinkedIn (perfil desatualizado), Google (sem menção) | Não existe no Blip; descartado |

---

## FILTROS COMBINADOS (Scoring)

### Qualification Score (0–100)
```
Empresa (0–60):
  Setor correto        +15
  Tamanho correto      +15
  Geografia Brasil     +10
  Trigger ativo        +20

Pessoa (0–40):
  Cargo primário       +15
  Senioridade 5+       +10
  Atividade recente    +15

TOTAL:
  ≥70 = QUALIFICADO → Inbound qualify + add to list
  50–69 = MARGINAL → Research + 1 point of contact
  <50 = NÃO-ALVO → Skip
```

### Exemplo: Gr Pereira
```
Empresa:
  Setor (Varejo)           +15
  Tamanho (~R$200M)        +15
  Geografia (MG/SP)        +10
  Trigger (churn alt)      +20
  Subtotal Empresa         = 60

Pessoa (Gerente Ops):
  Cargo secundário         +10
  Senioridade (8 anos)     +10
  Atividade (LinkedIn)     +12
  Subtotal Pessoa          = 32

TOTAL                       = 92 ✅ QUALIFIED
```

---

## Fontes Públicas Recomendadas (por prioridade)

| Fonte | Cobertura | Custo | Latência | Recomendação |
|---|---|---|---|---|
| **LinkedIn** (Sales Navigator) | 90%+ execs Brasil | Pago ($$$) | Real-time | Primária: Ops, Sales, titulo, senioridade |
| **Crunchbase** | 70% midmarket+ | Pago ($) | 1–3 meses | Setor, ARR, funding rounds, news |
| **RFB / Receita Federal** | 100% (todos CNPJ) | Grátis | 1+ ano | Faturamento, funcionários, setor (CNAE) |
| **Builtwith** | 80% (tech stack) | Pago ($) | 1–2 meses | Cloud (AWS/Azure), CRM, ERP, integração |
| **Hunter.io** | 85% (emails + stack) | Pago ($) | Real-time | Emails, títulos, tech stack do site |
| **Clearbit** | 60% (enrichment) | Pago ($$) | Real-time | News, funding, executives, tech |
| **Google (pesquisa)** | 100% | Grátis | 0–5 dias | Intento manual (integrações, case studies) |
| **Google Trends / Ads Keyword Planner** | 100% (volume) | Grátis | Real-time | Sinais de intento de busca |
| **LinkedIn (organic scrape)** | 90% | Grátis (com limite) | Real-time | Atividade, engajamento, followers |
| **Company website** | 100% (quando existe) | Grátis | Real-time | About, team, press releases, blog |
| **Apify** (web scraping) | Custom | Pago ($) | 1–3 dias | LinkedIn profiles, job postings, sites |
| **Leadfeeder / Demandbase** | 50% (visitors) | Pago ($$$) | Real-time | Website visitors (requer pixel) |

---

## Template de Pesquisa Manual (para critérios com **!**)

### Checklist para empresa candidata:
```
[ ] CNPJ → RFB → ARR, setor, quadro, faturamento  
[ ] LinkedIn Company → offices (estados), headcount, recruiting
[ ] Website → about, news, blog (trigger: "automação", "omnichannel", "WhatsApp")
[ ] Google News → últimas 3 meses (exec changes, funding, partnerships)
[ ] Crunchbase → series, ARR, growth signals
[ ] Building → tech stack (CRM, cloud, ERP)
```

### Checklist para pessoa candidata:
```
[ ] LinkedIn (público) → titulo, senioridade, tenure, atividade posts
[ ] Hunter.io → email, título, company
[ ] Google (nome + empresa) → publications, speaking, online presence
[ ] LinkedIn 2nd-degree connections → mutual contacts (warm intro path)
```

---

## Próximos Passos

1. **Hoje**: Priorizar LinkedIn Sales Navigator + Crunchbase para primeiro batch (50 leads)
2. **Semana 1**: Validar 5 qualified leads manualmente (full research)
3. **Semana 2**: Testar outbound em 50 leads; medir response rate
4. **Semana 3**: Iterar ICP / filtros baseado em taxa de conversão
5. **Mensal**: Atualizar lista (removidos que fecharam, adicionados em trigger)
