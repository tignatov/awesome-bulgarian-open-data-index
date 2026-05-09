# A Comprehensive Index of Open Data Sources Published by Bulgarian Government Entities

> **Reference document — last compiled May 2026.** This index catalogues open data, public registers, machine‑readable APIs, and human‑readable transparency portals operated by central, regional, and local public-sector bodies in the Republic of Bulgaria, plus key state‑owned enterprises, regulators, the judiciary, and selected civic-tech aggregators. URLs are given as they are advertised by the source organisations. Coverage focuses on datasets and registers that can be reused programmatically; where access is only via a web register/portal that is noted explicitly. Bulgarian (BG) and English (EN) language versions are flagged. This document deliberately mixes Bulgarian source names with English translations for searchability.

---

## Table of contents

1. [Overview and how to use this index](#1-overview)
2. [Legal framework and policy context](#2-legal-framework)
3. [Open Government Partnership status](#3-ogp)
4. [Tier 0 — National master portals (start here)](#4-tier-0)
5. [Central government — Council of Ministers, Presidency, Parliament](#5-central-government)
6. [Ministries (line ministries)](#6-ministries)
7. [Executive / state agencies](#7-executive-agencies)
8. [Independent regulators and commissions](#8-regulators)
9. [Judicial system, prosecution, official gazette](#9-judicial)
10. [Elections, parties, public consultations](#10-elections)
11. [Bulgarian National Bank and macro-financial data](#11-bnb)
12. [Cadastre, geospatial / INSPIRE node, addresses](#12-geospatial)
13. [Business, tax, customs and economic registers](#13-business-registers)
14. [Health, social security, pensions](#14-health-social)
15. [State-owned enterprises and infrastructure operators](#15-soes)
16. [Local government — oblasti and municipalities](#16-local-gov)
17. [Public universities, BAS and research data](#17-research)
18. [EU and international portals where Bulgarian data is aggregated](#18-eu-international)
19. [Civic tech and NGO aggregators / datasets](#19-civic-tech)
20. [Cross-cutting indices (by domain, by access type, by format)](#20-cross-cutting)
21. [Caveats and known limitations](#21-caveats)

---

<a id="1-overview"></a>
## 1. Overview and how to use this index

Bulgaria has been a member of the **EU Open Data Directive (2019/1024)** regime since accession and operates a CKAN-based national open data portal at **`https://data.egov.bg`** (formerly `opendata.government.bg`), maintained by the **Ministry of e-Government (MEU)** — the successor to the State e-Government Agency (DAEU). According to public statements by the Ministry, the portal aggregates several thousand datasets from more than 500 public-sector organisations. In addition to the central CKAN portal, dozens of ministries, agencies, regulators, courts, and municipalities publish data directly on their own institutional sites, often as static CSV/XLSX/PDF downloads or via specialised registers. A separate **National Spatial Data Portal** at `https://inspire.egov.bg` implements the INSPIRE Directive.

In the **2024 EU Open Data Maturity Assessment** (data.europa.eu), Bulgaria was placed in the *“Beginners”* group along with Greece, Romania, Croatia, Malta, Albania, Iceland and Bosnia & Herzegovina; its overall maturity score dropped about 13 percentage points compared to 2023, partly reflecting methodological tightening. Bulgaria reports a *top-down* governance model and a *custom* (non-standard) portal stack for its national portal, although the underlying engine is CKAN.

Use this index in three ways: (a) follow links by **publishing entity** (sections 5–17); (b) search by **thematic domain** (section 20-A); (c) filter by **access type / format** (section 20-B/C) when you need a specific integration pattern (CKAN API vs. SOAP vs. scraping).

---

<a id="2-legal-framework"></a>
## 2. Legal framework and policy context

| Instrument | Bulgarian name | Scope |
|---|---|---|
| Access to Public Information Act (APIA / ZDOI) | Закон за достъп до обществена информация | Right to request information; mandates the central open data portal in Art. 15d. |
| Public Sector Information Re-use rules (transposition of EU Open Data Directive 2019/1024, ex 2003/98/EC, 2013/37/EU) | Глава четвърта „а“ на ЗДОИ | Re-use of public sector information; obligation to publish in machine-readable formats with metadata. |
| Council of Ministers prioritised dataset list | Списък с набори от данни по приоритетни области | Annual list of datasets each administration must open; revised yearly (e.g., 30‑dataset list approved 2020). |
| EU Implementing Regulation 2023/138 | High-Value Datasets Regulation | Six categories (geospatial; earth obs/environment; meteorological; statistics; companies; mobility) must be free, machine-readable, available via API + bulk download since June 2024. |
| INSPIRE Directive 2007/2/EC | Закон за достъп до пространствени данни (ЗДПД) | Geospatial interoperability; implemented through `inspire.egov.bg`. |
| e-Government Act | Закон за електронното управление | Mandates publication of administrative information and electronic services. |
| Anti-Corruption Act | Закон за противодействие на корупцията | Public registers of declarations for senior officials. |

---

<a id="3-ogp"></a>
## 3. Open Government Partnership (OGP) status

Bulgaria has been an OGP member since 2011. After a hiatus following the third action plan (2016–2018), the country adopted a **fourth action plan (2022–2024)** with 14 commitments covering open data, COVID‑19 spending transparency, civic participation, anti-corruption, and conceptual reform of open governance. Implementation was tracked by the **Administration of the Council of Ministers** and reviewed by the OGP Independent Reporting Mechanism. Six of fourteen commitments were rated full/substantial; commitments 6 (COVID-19 spending) and several open-data commitments produced the strongest early results. As of the 2025 IRM Results Report, work on a fifth action plan had begun but had not been formally adopted.

Key OGP-related public infrastructure:
- **`strategy.bg`** — Public Consultations Portal (Портал за обществени консултации) maintained by the Council of Ministers.
- **`gov.bg`** — Council of Ministers website with cabinet decisions, draft acts, and meeting agendas.

---

<a id="4-tier-0"></a>
## 4. Tier 0 — National master portals (start here)

| # | Name (BG / EN) | URL | Operator | What it contains | Access | Formats | Lang |
|---|---|---|---|---|---|---|---|
| T0.1 | Портал за отворени данни на Република България / **National Open Data Portal** | `https://data.egov.bg` | Ministry of e-Government (МЕУ) | Central CKAN catalogue aggregating datasets from ministries, agencies, municipalities, regulators. Forks of CKAN with Bulgarian theme; includes datastore, datapusher. Source code on GitHub: `governmentbg/data-gov-bg`. | CKAN web UI; CKAN REST API (`/api/3/action/...`); per‑resource downloads; datastore; user registration optional for browsing. | CSV, JSON, XML, XLSX, RDF, GeoJSON, Shapefile (per dataset) | BG/EN |
| T0.2 | Национален портал за пространствени данни (INSPIRE) / **National Spatial Data Portal** | `https://inspire.egov.bg` | Ministry of e-Government | INSPIRE-compliant geoportal indexing WMS/WFS endpoints from cadastre, environment, hydrology, statistics, ports, transport. Lists “data sharing entities” incl. NSI, BPI Co., IO-BAS. | OGC WMS / WFS; CSW catalogue; metadata search | XML/GML, GeoJSON, Shapefile, WMS tiles | BG/EN |
| T0.3 | Единен портал за достъп до електронни административни услуги / **Single Portal for e‑Services** | `https://egov.bg` | Ministry of e-Government | 370+ administrative services; not strictly open data but key for service catalogues. Linked to **`iisda.government.bg`** — Integrated information system for state administration with org-chart and registers. | Web portal | HTML, PDF mainly | BG/EN |
| T0.4 | Портал за обществени консултации / **Public Consultations Portal** | `https://strategy.bg` | Council of Ministers | Drafts of laws, secondary legislation, strategies; OGP action plans were drafted here. | Web portal; structured per draft act | HTML, PDF | BG (mostly) |
| T0.5 | Регистър на административните структури и актовете на органите на изпълнителната власт / **Register of administrative structures and executive-branch acts** | `https://iisda.government.bg` | Council of Ministers Administration | Authoritative directory of ministries, agencies, commissions, local administrations, with addresses, regulations, organisational structures. | Web register | HTML, occasional XLSX exports | BG/EN |
| T0.6 | EUR-Lex / N-Lex Bulgaria gateway | `https://n-lex.europa.eu/n-lex/legis_bg/apis_form` | EU Publications Office | Cross-search of Bulgarian legislation harmonised with EU law. Useful as secondary access to the State Gazette. | Web search | HTML, PDF | BG/EN |
| T0.7 | data.europa.eu Bulgaria catalogue | `https://data.europa.eu/data/catalogues/open-data-bulgaria` | EU Publications Office | Harvests Bulgarian metadata; secondary discovery layer for `data.egov.bg`. | DCAT-AP harvest; SPARQL endpoint at portal level | RDF/DCAT, JSON | EN/BG |

---

<a id="5-central-government"></a>
## 5. Central government — Council of Ministers, Presidency, Parliament

### 5.1 Council of Ministers / Министерски съвет
- **`https://www.gov.bg`** — Council of Ministers homepage. Cabinet decisions, agendas, press releases (HTML/PDF; BG/EN).
- **`https://strategy.bg`** — Public Consultations and Strategic Documents portal.
- **`https://www.government.bg`** — Government information portal, used by the State Administration as parent domain for many ministry sites.

### 5.2 President / Президент на Република България
- **`https://www.president.bg`** — decrees, vetoes, statements, biographies. Mostly human‑readable (HTML/PDF). No structured open data feed; decrees are also republished in the State Gazette.

### 5.3 Народно събрание / National Assembly (Parliament)
- **`https://www.parliament.bg`** — bills, voting roll-calls, plenary stenograms, committee transcripts, MP profiles, declarations.
- **`https://dv.parliament.bg`** — official online edition of the **State Gazette (Държавен вестник)** — the gazette of record (since 1879). Full PDFs of every issue; search interface.
- Voting and bill data are published as HTML/PDF; there is **no formal open API** equivalent to UK/EU parliaments. Civic developers regularly scrape these pages. The third-party site **`parliament.bg/pub/ncpi/...`** hosts polling reports.
- **N-Lex BG** (`n-lex.europa.eu/.../legis_bg/...`) provides a structured EU gateway to Bulgarian acts.

### 5.4 Constitutional Court / Конституционен съд
- **`http://www.constcourt.bg`** — decisions and dissenting opinions in HTML/PDF. Full text of decisions published with the official numbering format `Decision No X of YYYY in Case No Y/YYYY`.

---

<a id="6-ministries"></a>
## 6. Ministries (line ministries)

The full ministerial list (Council of Ministers as of 2026; mergers happen frequently after government changes). Most ministries publish:
- a “Profile of the buyer” (профил на купувача) for procurement;
- annual reports and statistical bulletins as PDF;
- selected datasets pushed to `data.egov.bg` under their organisational page.

| # | Ministry (BG / EN) | Web | Notable open data / registers |
|---|---|---|---|
| M1 | Министерство на финансите / **Ministry of Finance** | `https://www.minfin.bg` | Consolidated Fiscal Programme (CFP) monthly bulletins; State Budget law; Medium-Term Budgetary Forecast; debt statistics. World Bank BOOST dataset is derived from MoF cash-basis budget execution data. PDF/XLSX. |
| M2 | Министерство на вътрешните работи / **Ministry of Interior (MVR)** | `https://www.mvr.bg` | Crime statistics (annual reports); KAT traffic-violation lookups (limited public). |
| M3 | Министерство на правосъдието / **Ministry of Justice** | `https://www.justice.government.bg` | Coordinator for ECLI; legalacts.justice.bg (see §9). |
| M4 | Министерство на здравеопазването / **Ministry of Health** | `https://www.mh.government.bg` | Annual public-health reports; lists of healthcare establishments; tariffs; pharmaceutical pricing decisions; `mh.government.bg/bg/politiki/godishen-doklad-za-zdraveto`. |
| M5 | Министерство на образованието и науката / **Ministry of Education and Science** | `https://www.mon.bg` | Register of accredited universities; national assessment results; school registers; **`rsvu.mon.bg`** — Rating system of Bulgarian higher schools. |
| M6 | Министерство на външните работи / **MFA** | `https://www.mfa.bg` | Treaties; consular networks; press releases. |
| M7 | Министерство на отбраната / **Ministry of Defence** | `https://www.mod.bg` | Public information — limited; some policy documents. |
| M8 | Министерство на икономиката и индустрията / **Ministry of Economy and Industry** | `https://www.mi.government.bg` | Foreign trade indicators; SME programmes; lists of certified investors (replicated in `data.egov.bg`). |
| M9 | Министерство на енергетиката / **Ministry of Energy** | `https://www.me.government.bg` | Energy balances; public registers under Energy Act. |
| M10 | Министерство на околната среда и водите / **MOEW** | `https://www.moew.government.bg` | National environmental data through ExEA (see §7); river basin directorates. |
| M11 | Министерство на земеделието и храните / **Ministry of Agriculture and Food** | `https://www.mzh.government.bg` | CAP Strategic Plan 2023–2027; Land Identification System (LPIS) data via SFA; statistical bulletins; phytosanitary registers. |
| M12 | Министерство на транспорта и съобщенията / **Ministry of Transport and Communications** | `https://www.mtc.government.bg` | Road, rail, maritime, aviation policy data; oversees BDŽ, NRIC, BPI Co. |
| M13 | Министерство на туризма / **Ministry of Tourism** | `https://www.tourism.government.bg` | National Tourist Register (hotels, guides, tour operators); statistics. |
| M14 | Министерство на труда и социалната политика / **MLSP** | `https://www.mlsp.government.bg` | Labour-market and social-services data, partly via NSSI/EA Employment. |
| M15 | Министерство на културата / **Ministry of Culture** | `https://www.mc.government.bg` | National Register of Cultural Monuments; library and museum directories. |
| M16 | Министерство на електронното управление / **Ministry of e-Government (MEU)** | `https://e-gov.bg` | Operates `data.egov.bg`, `inspire.egov.bg`, `egov.bg`, e‑signature, e‑identification. Source-of-truth ministry for open data policy. |
| M17 | Министерство на регионалното развитие и благоустройството / **MRDPW** | `https://www.mrrb.government.bg` | Cadastre/AGCC oversight; **GRAO** (`https://www.grao.bg`) civil registration data — population by settlement, by age, electoral lists. |
| M18 | Министерство на иновациите и растежа / **Ministry of Innovation and Growth** | `https://www.mig.government.bg` | OP “Innovation and Competitiveness” / “Competitiveness and Innovation in Enterprises” beneficiary lists. |
| M19 | Министерство на младежта и спорта / **Ministry of Youth and Sports** | `https://mpes.government.bg` | National Sport Register; licensed sport federations. |
| M20 | Министерство на околните инвестиции (when present) | Varies | Periodic, depending on cabinet structure. |

> Note: cabinet structure changes after each general election; some portfolios are split or merged (e.g., Tourism merged with Economy on occasion). Always cross-check at `iisda.government.bg`.

---

<a id="7-executive-agencies"></a>
## 7. State agencies and executive agencies (Изпълнителни агенции)

| Agency | URL | Data offered |
|---|---|---|
| **Национален статистически институт (NSI)** | `https://www.nsi.bg` and Open Data section `https://www.nsi.bg/opendata/` | Demographics; macroeconomic indicators; social statistics; **Census 2021** dataset; municipality- and district-level breakdowns; **Infostat** interactive system. CSV, XLSX, JSON, PC-Axis (PX), API endpoints (per-table). Bilingual BG/EN. SDDS Plus reporter together with BNB and MoF. |
| **Национална агенция за приходите (NRA / NAP)** | `https://www.nra.bg` | Tax statistics; insolvency lookup; VAT/Bulstat lookup. Limited open API (mostly web forms). VIES via EU. |
| **Агенция Митници / Customs Agency** | `https://customs.bg` | Foreign trade statistics; tariff database (TARIC mirror); excise duty registers (BACIS). |
| **Агенция по геодезия, картография и кадастър (AGCC)** | `https://www.cadastre.bg`, KAIS portal `https://kais.cadastre.bg`, INSPIRE node `https://inspire.cadastre.bg`, geographical names `http://geonames.cadastre.bg` | Cadastral parcels, addresses, buildings, geographic names; ArcGIS REST endpoint at `inspire.cadastre.bg:6080/arcgis/rest/services/inspire/iServices/MapServer`. Open Data section at `kais.cadastre.bg/en/OpenData`. Many high-resolution datasets are paid; INSPIRE metadata is open. |
| **Изпълнителна агенция по околна среда (ExEA / ИАОС)** | `https://eea.government.bg` | National environmental monitoring; live air quality (PM10, PM2.5, NO2, SO2, CO, O3) at `eea.government.bg/kav`; gamma-radiation network; National Ecological Database; annual State of Environment reports. CSV/XML downloads + map viewer. |
| **Българска агенция по безопасност на храните (BFSA / БАБХ)** | `https://bfsa.egov.bg` | Animal-disease registers; food-business operator lists; pesticide MRLs; veterinary medicines plan. |
| **Изпълнителна агенция по лекарствата (BDA / Bulgarian Drug Agency)** | `https://www.bda.bg` | Marketing-authorisation register; pharmacovigilance; inspection reports. |
| **Патентно ведомство / Patent Office** | `https://www.bpo.bg` | Trademark, patent, industrial design search. |
| **Агенция по вписванията / Registry Agency** | `https://www.registryagency.bg`, public portal `https://portal.registryagency.bg` | Trade Register (TRRYuLNTs); BULSTAT; Property Register; NPLE register; daily bulk dump of company changes pushed to `data.egov.bg` (see §13). |
| **Държавна агенция „Държавен резерв и военновременни запаси“** | `https://www.statereserve.bg` | Stock data — limited public access. |
| **Държавна агенция „Архиви“** | `https://www.archives.government.bg` | National archive descriptions and finding aids. |
| **Държавна агенция за бежанците** | `https://www.aref.government.bg` | Asylum statistics. |
| **Изпълнителна агенция „Главна инспекция по труда“** | `https://www.gli.government.bg` | Labour inspections — periodic reports. |
| **Агенция за социално подпомагане** | `https://www.asp.government.bg` | Social-assistance recipients statistics. |
| **Държавен фонд „Земеделие“ (SFA)** | `https://www.dfz.bg` | CAP paying agency; payment registers per scheme; LPIS extracts. |
| **Изпълнителна агенция „Електронни съобщителни мрежи и информационни системи“** | `https://www.esmis.government.bg` | National Open Data System tooling; SEEU. |
| **Държавна агенция „Национална сигурност“ (DANS)** | `https://www.dans.bg` | Limited public outputs. |
| **Главна дирекция „Гражданска регистрация и административно обслужване“ (GRAO)** | `https://www.grao.bg` | Population by settlement, electoral lists, civil-registration aggregates — XLSX/CSV releases. |
| **Изпълнителна агенция „Сертификационен одит на средствата от ЕС“** | `https://www.aeuf.minfin.bg` | EU funds audit reports. |

---

<a id="8-regulators"></a>
## 8. Independent regulators and commissions

| Body | URL | Data |
|---|---|---|
| **Комисия за защита на конкуренцията (CPC)** | `https://www.cpc.bg` | Decisions register; cartel cases; merger filings (HTML + PDF). |
| **Комисия за регулиране на съобщенията (CRC)** | `https://crc.bg` | Spectrum register; postal & e‑comms operators; mobile/broadband statistics. |
| **Комисия за енергийно и водно регулиране (KEVR)** | `https://www.dker.bg` | Tariff decisions; license register; daily natural-gas balances; electricity prices. |
| **Комисия за финансов надзор (FSC)** | `https://www.fsc.bg` | Single-window register of investment intermediaries, insurers, pension funds, listed issuers; **Unified Information System (EIS)**; FSC Mobile app; structured registers per supervisor segment. |
| **Комисия за защита на личните данни (CPDP)** | `https://www.cpdp.bg` | Decisions, fines, register of data controllers/DPOs. |
| **Сметна палата / National Audit Office** | `https://www.bulnao.government.bg` | Audit reports on state and municipal budgets; political-party financial reports; declarations of assets of MPs and senior officials. |
| **Комисия за противодействие на корупцията (CAC)** | `https://caciaf.bg` (since 2023 split: CAC and CIAF) | Public register of declarations of assets and interests; conflict-of-interest decisions; asset-forfeiture statistics. |
| **Комисия за публичен надзор над регистрираните одитори (KPNRO)** | `https://www.cpros.bg` | Auditor register. |
| **Комисия за защита от дискриминация** | `https://kzd-nondiscrimination.com` | Decisions database. |
| **Съвет за електронни медии (CEM)** | `https://www.cem.bg` | Broadcasting licenses; ad-monitoring reports. |
| **Държавна комисия по сигурността на информацията** | `https://www.dksi.bg` | Limited. |
| **Българска народна банка (BNB)** — see §11 |  |  |
| **Агенция за обществени поръчки (PPA)** | `https://www2.aop.bg` and CAIS EOP at `https://app.eop.bg` | Public Procurement Register; List of Contracting Authorities; List of awarded contracts; monthly bulletin; statistics. Mandatory e‑procurement since Nov 2019. |

---

<a id="9-judicial"></a>
## 9. Judicial system, prosecution, official gazette

| Source | URL | Description |
|---|---|---|
| **legalacts.justice.bg** | `https://legalacts.justice.bg` | Central web interface for case-law publication, ECLI-coordinated by the Supreme Judicial Council. Personal data redacted. Maintained via Regulation No 4 of 2017. |
| **Върховен касационен съд (VKS) — Supreme Court of Cassation** | `http://www.vks.bg` | Judgments since 1 Oct 2008 in full text; bulletins; search by court/parties/case number. |
| **Върховен административен съд (SAC)** | `http://www.sac.government.bg` | Administrative case-law; decisions striking down secondary legislation. |
| **Висш съдебен съвет (Supreme Judicial Council, VSS)** | `https://www.vss.justice.bg` | Judicial statistics; appointment decisions; ECLI coordinator. |
| **Прокуратура / Prosecutor's Office** | `https://prb.bg` | Statistics, press releases. |
| **Единен портал за електронно правосъдие (UPEJ)** | `https://ecase.justice.bg` | Per-case status (registered users); since 1 July 2021 mandatory for lawyers under JSA Art. 360c. |
| **Sofia City Court e-portal** | `https://sgs.justice.bg` | Local case lookup. |
| **Държавен вестник / State Gazette** | `https://dv.parliament.bg` | Official journal since 1879; PDF issues; free search across last 7 years. |
| **lex.bg / ciela.net (commercial)** | `https://www.lex.bg`, `https://www.ciela.net/official-gazette` | Commercial consolidated legislation; ciela offers free historical SG access at moment-of-promulgation. |

---

<a id="10-elections"></a>
## 10. Elections, parties, public consultations

| Source | URL | Description |
|---|---|---|
| **Централна избирателна комисия (CIK / CEC)** | `https://www.cik.bg` and per-election results pages e.g., `results.cik.bg` | Per-election results down to section level (~12,000 SECs); candidate registers; SEC protocols; voter-list checks. CSV/XLSX/JSON published per election since 2014. Data also pushed to `data.egov.bg`. |
| **GRAO voter-list checks** | `https://www.grao.bg` | Section assignments; check-by-EGN. |
| **Sofia Election dashboards (third-party, NGO)** | `https://europeelects.eu`, `dashboard.bg` (varies) | Aggregations of CIK data with visualisations. |
| **Анти-Корупционен фонд (ACF) — Анализ на изборите** | `https://acf.bg` | Reports on vote-buying and turnout patterns at risk-flagged sections. |

---

<a id="11-bnb"></a>
## 11. Bulgarian National Bank (BNB)

- **`https://www.bnb.bg`** — central bank statistics, monetary policy, financial stability.
- **`https://www.bnb.bg/Statistics/...`** — Statistics section: monetary aggregates, interest rates, balance of payments, IIP, government finance, foreign reserves, banking-sector aggregates, BNB balance sheet (CSV/XLSX downloads).
- **SDDS Plus national page** — `https://www.bnb.bg/Statistics/SDDSPlus/SDDSPlusNationalPage/index.htm` — co-published with NSI, MoF, BSE.
- **Daily exchange rates** — `https://www.bnb.bg/Statistics/StExternalSector/StExchangeRates/StERForeignCurrencies/index.htm`; XML feed widely consumed by accounting / tax systems and replicated by third-party APIs (e.g., `fluentax.com`).
- **MFI ID** `BGBNBG9661`, **LEI** `5299001WEKCK7E65TI48`, **BIC** `BNBGBGSF`.

---

<a id="12-geospatial"></a>
## 12. Cadastre, geospatial / INSPIRE node, addresses

| Source | URL | Description / Formats |
|---|---|---|
| **AGCC — Geodesy, Cartography and Cadastre Agency** | `https://www.cadastre.bg` (institutional) | Authoritative cadastral, topographic, geodetic data. |
| **KAIS — Cadastral and Administrative Information System** | `https://kais.cadastre.bg` | Public lookup: parcel ID, building ID, owner type. KAIS Open Data section at `/en/OpenData`. Mobile/web apps redistribute. |
| **`gkf.cadastre.bg`** | Geocartfund | Historic and current cartographic materials. |
| **National INSPIRE Geoportal** | `https://inspire.egov.bg/en` | Catalogue of all INSPIRE-aligned datasets across Bulgarian public bodies. |
| **`inspire.cadastre.bg`** | Cadastre INSPIRE node | OGC services WMS/WFS for cadastral parcels, buildings, addresses, geographical names; ArcGIS REST: `inspire.cadastre.bg:6080/arcgis/rest/services/inspire/iServices/MapServer`. |
| **`geonames.cadastre.bg`** | Geographical names register | Toponymic INSPIRE register. |
| **Sofia GIS / iSofMap** | `https://www.gis-sofia.bg`, `https://isofmap.bg` (or via gis-sofia.bg) | Sofia-municipality cadastre, addresses, regulation plans, green areas. As of 2025 Mayor Vasil Terziev announced opening of orthophoto, address, green area and commercial-zone data publicly — part of Sofia’s “digital twin” initiative. |
| **NextGIS / OSM derivatives** (third-party) | `https://data.nextgis.com/en/region/BG/base/` | Reformatted OSM and INSPIRE data — Shapefile/GeoPackage/GeoJSON. |
| **Bulgarian Spatial Data Infrastructure (legacy/research)** | `https://bsdi.asde-bg.org` | Civil-society/academic precursor to INSPIRE node. |

---

<a id="13-business-registers"></a>
## 13. Business, tax, customs and economic registers

| Register | URL | Notes |
|---|---|---|
| **Търговски регистър и регистър на ЮЛНЦ (Trade Register & NPLE Register)** | `https://portal.registryagency.bg` | Public 24/7. Daily bulk database dump (history + redactions) pushed to `data.egov.bg` under CC-BY licence; this is what civic projects like **`companybook.bg`** (TheCompanyBook) and `yurukov/bg-corporate-opendata` consume. Entity look-up by UIC/name. |
| **BULSTAT register** | `https://portal.registryagency.bg/bulstat` | Identification numbers for non-merchants. |
| **Имотен регистър / Property Register** | `https://portal.registryagency.bg/imoten-registar` | Real-estate transactions; partial public access. |
| **NRA — Tax compliance lookups** | `https://nra.bg` | VAT/EORI checks; arrears certificate validation. |
| **Customs Agency BACIS** | `https://customs.bg` | Excise centralised IS; data shared with NRA, NSI. |
| **NSI Business Statistics** | `https://www.nsi.bg/business-statistics` | Annual activity reports filing portal; downstream macro statistics. |
| **AOP — Public Procurement Register / CAIS EOP** | `https://www2.aop.bg`, `https://app.eop.bg` | All tenders ≥ €25,000; awarded-contracts register; integrated with TED. |
| **InvestBulgaria Agency** | `https://www.investbg.government.bg` | Certified investors; FDI data. |
| **BCCI Voluntary Trade Register** | `https://www.bcci.bg/tradereg-system-en.html` | Voluntary; chamber-administered. |
| **ESMA / FSC issuer disclosures** | via `https://www.fsc.bg` | Listed company financial reports. |

---

<a id="14-health-social"></a>
## 14. Health, social security, pensions

| Source | URL | Description |
|---|---|---|
| **Национална здравноосигурителна каса (NHIF / NZOK)** | `https://www.nhif.bg`, EN `https://www.en.nhif.bg` | Annual reports; reimbursement decisions; positive drug list; per-region structures. Datasets like **NHIF Bulgaria: Individually Approved Medicines under Ordinance №2** are released on request and re-published on Zenodo. |
| **Национален осигурителен институт (NSSI / NOI)** | `https://www.noi.bg` | Pensions and social-insurance statistics, monthly bulletins, beneficiary aggregates. |
| **Ministry of Health** | `https://www.mh.government.bg` | Annual public-health reports; healthcare establishment registers. |
| **NSI Health section** | `https://www.nsi.bg/en/content/4663/health` | Health establishments at 31.12 each year; mortality and morbidity. |
| **Eurohealth Observatory / WHO** | `https://eurohealthobservatory.who.int/countries/bulgaria` | Secondary aggregator. |

---

<a id="15-soes"></a>
## 15. State-owned enterprises and infrastructure operators

These typically publish **financial statements** (under the Public Enterprises and Control Agency – APSK, `https://www.priv.government.bg`) and limited operational data; few have full open APIs.

| Entity | URL | Data |
|---|---|---|
| **Holding БДЖ ЕАД (Bulgarian State Railways)** | `https://holding.bdz.bg` | Annual financial reports; rolling-stock data; tickets via `https://www.bdz.bg`. |
| **БДЖ — Пътнически превози ЕООД / Passenger Services** | `https://www.bdz.bg` | Timetables (HTML/PDF); ticket API not public. |
| **БДЖ — Товарни превози / Cargo** | `https://bdz-cargo.bg` | Service catalogue. |
| **Национална компания „Железопътна инфраструктура“ (NRIC)** | `https://www.rail-infra.bg` | Network statement; train-path register; infrastructure charges. |
| **„Български пощи“ ЕАД (Bulgarian Posts)** | `https://www.bgpost.bg` | Rates, tracking; no formal open data. |
| **„Електроенергиен системен оператор“ ЕАД (ESO)** | `https://www.eso.bg` | Real-time grid data: load, generation mix, interconnection flows; ENTSO-E TP relayed; XML/CSV exports. |
| **„Национална електрическа компания“ ЕАД (NEK)** | `https://www.nek.bg` | Wholesale electricity; HPP data; financials. |
| **„Български енергиен холдинг“ (BEH)** | `https://www.bgenh.com` | Group-level reports; subsidiaries. |
| **„Булгаргаз“ ЕАД** | `https://www.bulgargaz.bg` | Tariff filings (KEVR). |
| **„Булгартрансгаз“ ЕАД** | `https://www.bulgartransgaz.bg` | TSO transparency data per ENTSO-G; capacity bookings. |
| **„АЕЦ Козлодуй“ ЕАД (Kozloduy NPP)** | `https://www.kznpp.org` | Plant statistics; environmental monitoring. |
| **Independent Bulgarian Energy Exchange (IBEX)** | `https://www.ibex.bg` | Day-ahead, intraday, balancing market data; historical CSVs. |
| **„ВиК“ holding companies (28 districts) and MRRB** | per-district sites; oversight via MRRB | Water-supply tariffs, leakage rates. |
| **„Държавно предприятие „Пристанищна инфраструктура“ (BPI Co.)** | `https://www.bgports.bg` | Port statistics; INSPIRE node listed in `inspire.egov.bg`. |
| **„Държавно предприятие „Ръководство на въздушното движение“ (BULATSA)** | `https://www.bulatsa.com` | ATM statistics. |
| **Sofia Airport / Varna / Burgas / Plovdiv airports** | each has its own site | Concessioned to private operators (e.g., Sofia: Meridiam–SOF Connect; Varna/Burgas: Fraport-Bulgaria). |
| **Tram and Metro – Sofia Public Transport** | `https://www.sofiatraffic.bg` | Schedules; **GTFS** has been published intermittently. |
| **„Държавна консолидационна компания“ (SCC)** | `https://www.scc.bg` | Investment vehicle; minimal public data. |

---

<a id="16-local-gov"></a>
## 16. Local government — districts (oblasti) and municipalities

Bulgaria has **28 oblast (district) administrations** (each headed by a regional governor appointed by the Council of Ministers) and **265 municipalities** (with elected mayors and councils, per Local Self-Government and Local Administration Act / ZMSMA). Only a small minority of municipalities publish structured open data; most expose just budgets, council decisions, procurement profile, and zoning ordinances on their websites.

### 16.1 Oblast (district) administrations

All have institutional sites of the form `https://www.<oblast>.government.bg` (e.g., `bs.government.bg` for Burgas, `pd.government.bg` for Plovdiv, `vn.government.bg` for Varna). Content: governor’s decisions, regional development strategies, public consultations, beneficiary lists. No central oblast-level open-data portal exists.

### 16.2 Major municipalities — open data status

| Municipality | Site | Open data status |
|---|---|---|
| **Столична община / Sofia** | `https://www.sofia.bg` | Most advanced. Mayor Vasil Terziev (2024–) publicly opened **orthophoto maps, addresses, green areas, commercial zones** in 2025; Sofia’s “Innovative Sofia” / “Digitalisation and Information Systems” department. **GIS Sofia (`gis-sofia.bg`)** runs **iSofMap**. Council decisions, annual budget execution, and procurement profile online. Some datasets pushed to `data.egov.bg`. A standalone `data.sofia.bg` URL has been discussed but at time of writing the canonical entry points remain `sofia.bg`, `gis-sofia.bg/iSofMap`, and `data.egov.bg`. |
| **Пловдив / Plovdiv** | `https://www.plovdiv.bg` | Council decisions; budget; profile of the buyer. Open data: limited but pushes via `data.egov.bg`. |
| **Варна / Varna** | `https://www.varna.bg` | Council decisions; municipal company list; procurement. |
| **Бургас / Burgas** | `https://www.burgas.bg` | One of the more proactive — open data datasets on cycling counts, traffic, parking, GTFS for buses (`burgasbus.eu`). |
| **Русе / Ruse** | `https://www.ruse-bg.eu` | Decisions, plans. |
| **Стара Загора / Stara Zagora** | `https://www.starazagora.bg` |  |
| **Плевен / Pleven** | `https://www.pleven.bg` |  |
| **Сливен / Sliven** | `https://www.sliven.bg` |  |
| **Велико Търново / Veliko Tarnovo** | `https://www.veliko-tarnovo.bg` |  |
| **Габрово / Gabrovo** | `https://www.gabrovo.bg` | Pioneer in smart-city pilots; some open datasets. |
| **Шумен / Shumen** | `https://www.shumen.bg` |  |
| **Видин / Vidin** | `https://www.vidin.bg` |  |
| **Добрич / Dobrich** | `https://www.dobrich.bg` |  |
| **Пазарджик / Pazardzhik** | `https://www.pazardzhik.bg` |  |
| **Перник / Pernik** | `https://www.pernik.bg` |  |
| **Хасково / Haskovo** | `https://www.haskovo.bg` |  |
| **Благоевград / Blagoevgrad** | `https://www.blagoevgrad.bg` |  |
| **Враца / Vratsa** | `https://www.vratsa.bg` |  |
| **Кърджали / Kardzhali** | `https://www.kardjali.bg` |  |
| **Ямбол / Yambol** | `https://www.yambol.bg` |  |

> The remaining municipalities (~245) have minimal websites with PDFs of council decisions and budgets. Many smaller ones publish only legally mandated information (procurement notices in the AOP register).

### 16.3 Cross-cutting municipal data
- **NSI municipality-level statistics** (`https://www.nsi.bg/en/content/...`) — population, education, labour, environment per of 265 municipalities (XLSX).
- **NSI City Statistics** (functional urban areas — Sofia, Plovdiv, Varna, Burgas, Pleven, Ruse, Vidin, Stara Zagora, Sliven, Dobrich, Shumen, Pernik, Yambol, Haskovo, Pazardzhik, Blagoevgrad, Veliko Tarnovo, Vratsa).
- **Regional Profiles 2017–** (`https://www.regionalprofiles.bg`) — IME (think tank) annual analysis; CSV downloads.
- **GRAO** (`https://www.grao.bg`) — population by settlement and municipality (annual XLSX).

---

<a id="17-research"></a>
## 17. Public universities, BAS and research data

| Source | URL | Data |
|---|---|---|
| **Българска академия на науките (BAS)** | `https://www.bas.bg` | Institute-by-institute publications; 40+ institutes. |
| **Institute of Oceanology – BAS (IO-BAS)** | `https://io-bas.bg` | Black Sea oceanographic data; INSPIRE-listed. |
| **NACID — National Centre for Information and Documentation** | `https://nacid.bg` | Diploma recognition register; PhD register; researcher CVs. |
| **NALIS — National Academic Library and Information System** | `http://www.nalis.bg` | Union catalogue ~3.5M records, 40 libraries. |
| **National Library of Sts. Cyril and Methodius** | `https://www.nationallibrary.bg` | Digital collections. |
| **OpenAIRE Bulgaria NOAD** | `https://www.openaire.eu/os-bulgaria` | Open Science contact point. |
| **rsvu.mon.bg — Rating System of Higher Schools** | `https://rsvu.mon.bg` | Programme-level performance. |
| **INSAIT @ Sofia University** | `https://insait.ai` | AI research outputs; some open models. |

---

<a id="18-eu-international"></a>
## 18. EU and international portals where Bulgarian data is aggregated

| Portal | URL | Bulgarian relevance |
|---|---|---|
| **data.europa.eu** | `https://data.europa.eu/data/catalogues/open-data-bulgaria` | Harvests `data.egov.bg`; offers DCAT-AP metadata, SPARQL. |
| **Eurostat** | `https://ec.europa.eu/eurostat/data/database` | NSI data harmonised at NUTS levels; PC-Axis, CSV, JSON-stat. |
| **European Environment Agency (EEA)** | `https://www.eea.europa.eu/en/topics/in-depth/air-pollution/air-pollution-country-fact-sheets-2024/bulgaria-...` | Air pollution, INSPIRE compliance reporting. |
| **ENTSO-E Transparency Platform** | `https://transparency.entsoe.eu` | Bulgarian electricity TSO (ESO) data. |
| **ENTSO-G** | `https://transparency.entsog.eu` | Bulgartransgaz capacity. |
| **TED (Tenders Electronic Daily)** | `https://ted.europa.eu` | Bulgarian above-threshold tenders. |
| **European Data Portal (Maturity)** | `https://data.europa.eu/en/open-data-maturity/2024` | 2024 Bulgaria factsheet — Beginner cluster. |
| **European Court of Human Rights HUDOC** | `https://hudoc.echr.coe.int` | Cases against Bulgaria. |
| **EU CAP Network** | `https://eu-cap-network.ec.europa.eu/countries/bulgaria_en` | Bulgaria CAP Strategic Plan. |
| **OECD Bulgaria** | `https://www.oecd.org/en/countries/bulgaria.html` | Recent reports incl. on anti-corruption authorities (2024). |
| **World Bank BOOST – Bulgaria fiscal database** | World Bank platform | Cash-basis MoF execution data. |
| **IMF Bulgaria** | `https://www.imf.org/en/Countries/BGR` | Article IV reports, datasets. |
| **CEIC, Trading Economics, etc. (commercial)** | various | Re-license BNB/NSI data. |

---

<a id="19-civic-tech"></a>
## 19. Civic tech and NGO aggregators / datasets

| Project | URL | What it does |
|---|---|---|
| **Обществото.bg / Obshtestvo.bg Foundation** | `https://obshtestvo.bg` | Co-launched the original Bulgarian open data portal in 2014; ongoing CKAN-related contributions. |
| **GitHub `governmentbg/data-gov-bg`** | `https://github.com/governmentbg/data-gov-bg` | Source code of `data.egov.bg`; CKAN fork + Bulgarian theme + datapusher. |
| **GitHub `governmentbg/brra-opendata`** | `https://github.com/governmentbg/brra-opendata` | Trade Register opendata export script. |
| **TheCompanyBook** | `https://companybook.bg` | Free re-publication of Trade Register data with REST API; daily refresh. |
| **OSI-Sofia OpenData (Open Society Institute)** | `https://opendata.bg` | Sociological survey microdata: democracy, rule of law, attitudes (since 2005). |
| **Anti-Corruption Fund (ACF)** | `https://acf.bg` | Monitoring reports on high-level corruption cases; vote-buying data. |
| **Институт за пазарна икономика (IME)** | `https://ime.bg`, `https://www.regionalprofiles.bg` | Regional profiles, fiscal analyses; conducts Open Budget Survey for IBP. |
| **Bulgarian Institute for Legal Initiatives** | `https://bili-bg.org` | Judicial transparency rankings; selection-procedure datasets for senior judges. |
| **Access to Information Programme (AIP)** | `https://aip-bg.org` | Active Transparency Rating of Bulgarian Institutions (annual). |
| **Center for the Study of Democracy (CSD)** | `https://csd.bg` | Hidden economy index; corruption monitoring data. |
| **AEJ-Bulgaria** | `https://aej-bulgaria.org` | Press freedom and access-to-information cases. |
| **Bivol.bg** | `https://bivol.bg` | Investigative journalism; structured data behind major stories. |
| **`yurukov/bg-corporate-opendata`** | `https://github.com/yurukov/bg-corporate-opendata` | Visualisations of Trade Register — VAT registrations on map. |
| **Boyan Yurukov’s opendata.yurukov.net** | `http://opendata.yurukov.net` | Various BG opendata mashups (business, health, COVID-19). |
| **`covid.opendatablend.bg`-style trackers** (multiple) | various | COVID-19 charts based on `data.egov.bg`, ECDC, NSI. |
| **kat-bulgaria HACS integration** | GitHub | Home Assistant integration to check unpaid traffic fines via KAT. |
| **OpenStreetMap Bulgaria community** | `https://community.openstreetmap.org/c/europe/bulgaria` | Discussions on use of AGCC data on OSM. |
| **`api.store/bulgaria-api`** | `https://api.store/bulgaria-api` | Wrapped data.egov.bg as a REST API. |
| **`dateno.io`** | `https://dateno.io/registry/catalog/cdi00010348/` | Indexes Bulgarian portal in global dataset search. |

---

<a id="20-cross-cutting"></a>
## 20. Cross-cutting indices

### 20-A. By thematic domain

- **Budget & finance** — MoF (`minfin.bg`), AOP procurement, BNB, Sofia/Plovdiv/etc. budgets, BOOST.
- **Statistics & demographics** — NSI Open Data, GRAO, Eurostat, Census 2021.
- **Health** — Ministry of Health, NHIF, NSSI, NSI health section, BDA.
- **Education** — MoN, NSI, rsvu.mon.bg, NACID.
- **Environment** — MOEW, ExEA (`eea.government.bg`), River Basin Directorates, EEA.
- **Energy** — Ministry of Energy, KEVR, ESO, NEK, BEH, IBEX, ENTSO-E.
- **Transport** — MTC, NRIC, BDŽ, BPI Co., BULATSA, Sofia Public Transport (GTFS), AGCC roads.
- **Justice & legal** — State Gazette `dv.parliament.bg`, `legalacts.justice.bg`, VKS, SAC, Constitutional Court, n-lex.
- **Procurement** — AOP, CAIS EOP, TED.
- **Geospatial** — AGCC/KAIS, INSPIRE node `inspire.egov.bg`, GIS Sofia/iSofMap.
- **Companies & business** — Trade Register, BULSTAT, FSC, BCCI, NRA.
- **Agriculture** — MAF, SFA (paying agency), BFSA, NSI agricultural statistics.
- **Culture** — Ministry of Culture register, NALIS, National Library.
- **Elections** — CIK, GRAO, Audit Office political-party reports.
- **Social protection** — MLSP, NSSI, ASA.

### 20-B. By access type

| Type | Examples |
|---|---|
| **CKAN portal & API** | `data.egov.bg` (central); `data.europa.eu` (harvests). |
| **OGC WMS/WFS / CSW (geospatial)** | `inspire.egov.bg`; `inspire.cadastre.bg`; `gis-sofia.bg` ArcGIS REST. |
| **REST API** | NSI Infostat (table-level); BNB exchange rates; AOP CAIS EOP services; FSC EIS; CompanyBook (third-party). |
| **Bulk download** | Trade Register daily dump; NSI yearbooks; ExEA air-quality CSV; State Gazette PDFs. |
| **SOAP** | Some NRA, AGCC, e-Government legacy services. |
| **Web register only (HTML lookup)** | Most sectoral regulators (CPC, CRC, KEVR), KAIS public lookup, Constitutional Court decisions. |
| **Scraping required** | Parliament voting and stenograms; Court case-law beyond legalacts.justice.bg; many municipal council decisions. |
| **Registration required** | CAIS EOP for tendering; UPEJ for case access; cadastre KAIS write access. |

### 20-C. By format

| Format | Where it appears |
|---|---|
| **CSV** | `data.egov.bg` majority, NSI, ExEA, GRAO, AOP, BNB, ESO. |
| **JSON / JSON-stat** | NSI Infostat; data.egov.bg; data.europa.eu API; some FSC services. |
| **XML / GML** | INSPIRE services; BNB exchange rates; State Gazette feeds; SOAP envelopes. |
| **XLSX** | Default for ministries publishing statistical bulletins (MoF, NSI, NSSI, NHIF). |
| **PDF (human-readable)** | Many ministerial reports; State Gazette; municipal decisions. |
| **RDF / DCAT-AP** | Metadata at `data.egov.bg` and `data.europa.eu`. |
| **GeoJSON** | Selected INSPIRE services; municipal GIS exports; OSM derivatives. |
| **Shapefile / GeoPackage** | AGCC geo-card fund; INSPIRE downloads; NextGIS; ExEA. |
| **PC-Axis (PX)** | NSI long-form statistical tables. |

---

<a id="21-caveats"></a>
## 21. Caveats and known limitations

1. **Maturity is uneven.** The 2024 EU Open Data Maturity Report places Bulgaria in the “Beginners” group with a 13-percentage-point year-over-year drop; the methodological refresh and gaps in HVD reporting contributed. Many published “datasets” on `data.egov.bg` are stale or one-off snapshots rather than live feeds. Civic-society analyses (e.g., the NGOLinks usability study) document UX limitations: large datasets require manual click-through downloads of every resource.
2. **Coverage of municipalities is thin.** Of 265 municipalities, only Sofia (and to a lesser extent Burgas, Gabrovo, Plovdiv, Varna) have made substantive open-data releases. Most smaller municipalities publish only minimum statutory disclosures (procurement profile, council decisions as PDF).
3. **APIs are inconsistent.** Even where a portal advertises an API, rate limits, authentication, and stability vary. The CKAN datastore on `data.egov.bg` exposes per-resource SQL/JSON APIs but they are not uniformly enabled.
4. **Bilingual coverage drops outside top-level pages.** NSI, BNB, MEU, AOP and Eurostat-aligned content is solidly bilingual; sectoral regulators and local government materials are predominantly Bulgarian only.
5. **Fast-moving institutional landscape.** Cabinet reshuffles (six parliamentary elections 2021–2026) mean ministries split, merge, or change names; the Ministry of e-Government itself was reorganised from the State e-Government Agency. Always re-verify entity names against `iisda.government.bg`.
6. **Bulk Trade Register dump licence.** It is published under CC-BY on `data.egov.bg`; downstream reusers like `companybook.bg` and `governmentbg/brra-opendata` rely on it. Personal data for natural persons in the dump is anonymised per Bulgarian law; verify before reuse.
7. **The 2019 NRA data breach** showed how sensitive *non-open* government databases are. This index covers only data intended for public release; do not infer that adjacent administrative data is or should be open.
8. **Some entries reflect aspirational publishing.** Mayor Terziev’s 2025 announcement on Sofia geospatial open data and various OGP commitments include forward-looking promises; check the underlying URLs at time of use, as portals sometimes lag.
9. **High-Value Datasets (Reg. 2023/138).** Bulgaria, like other Member States, was required from June 2024 to publish six categories (geospatial, earth observation/environment, meteorological, statistics, companies, mobility) free, machine-readable, via API + bulk. The first reporting exercise occurred in 2025. Bulgaria’s implementation status is mixed: company data and INSPIRE geospatial layers are largely available; meteorological and mobility data via APIs are still maturing.
10. **Court case-law searches are not full open data.** `legalacts.justice.bg` provides per-decision pages but no documented bulk export or open API; for systematic analysis researchers scrape or use commercial systems (Сиела, Apis, Lex.bg).
11. **Election data publishing has improved markedly since 2014**; CIK now publishes per-section CSV/JSON within hours of vote counts, but historical pre-2013 results are scattered across legacy `cik.bg` archives.
12. **The civic-tech ecosystem is small but active.** The same individuals (e.g., Boyan Yurukov, Dimitar Dimitrov from Obshtestvo.bg) appear repeatedly across projects; institutional continuity is largely informal.
13. **Bulgaria’s INSPIRE node has been described as “experimental” in the past** (BSDI legacy, OKFN 2016 thread). The current `inspire.egov.bg` (under the Ministry of e-Government, since 2021–2022) is the canonical authority and integrates AGCC, NSI, IO-BAS, BPI Co. and others.
14. **Watch for URL drift.** `opendata.government.bg` was the pre-2018 portal; the canonical address is now `data.egov.bg`. Old citations and Government documents (including some EU-level pages) still link to the legacy URL.

---

### Quick-start recipes

- **To enumerate every dataset in Bulgaria machine-readably**: hit `https://data.egov.bg/api/3/action/package_list` (CKAN), then iterate `package_show?id=<name>` for metadata; cross-reference via `data.europa.eu` DCAT-AP harvest.
- **For company/UIC lookups**: use the Trade Register bulk dump on `data.egov.bg` (search “Търговски регистър”) — daily ZIPs; alternatively the unofficial `companybook.bg` REST API.
- **For elections**: download the per-election CSV bundle from `cik.bg`/`results.cik.bg` after each vote; supplement with GRAO section lists.
- **For environmental real-time data**: ExEA at `eea.government.bg/kav` (front-end), with the underlying station-level numbers also surfaced through EU EEA endpoints and AQICN.
- **For geospatial layers**: start at `inspire.egov.bg`, follow capability links to `inspire.cadastre.bg`, and supplement with NextGIS or OSM where `data.egov.bg` lacks coverage.
- **For Sofia city analytics**: combine NSI municipality tables, GIS Sofia (`gis-sofia.bg`/iSofMap), Sofia Traffic GTFS, and Sofia’s own datasets on `data.egov.bg`.

---

*This index is intentionally exhaustive at the level of *publishing entity* and *type of data offered*; it does not enumerate the thousands of individual datasets on `data.egov.bg` (use the CKAN API for that). It should be treated as a living document — the Bulgarian open-data landscape is shifting rapidly under EU HVD pressure and the new (2024) Ministry of e-Government roadmap.*
