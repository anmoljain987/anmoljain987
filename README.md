<h1 align="center">Anmol Jain</h1>

<p align="center"><b>SDE-II · Team Lead</b> at Idea Clan · platform and distributed systems</p>

<p align="center">
I build the data and automation platform behind two advertising SaaS products.<br>
Fifteen third-party data sources in, one analytics schema out.
</p>

<p align="center">
<img src="https://img.shields.io/badge/owns-~40_of_95_services-1C3557?style=flat-square" />
<img src="https://img.shields.io/badge/ClickHouse-600B%2B_rows%2Fmonth-F5A623?style=flat-square" />
<img src="https://img.shields.io/badge/p95-113--216ms-2E7D32?style=flat-square" />
<img src="https://img.shields.io/badge/platform_integrations-12-6A1B9A?style=flat-square" />
<img src="https://img.shields.io/badge/at_Idea_Clan-4_years-0B6E99?style=flat-square" />
</p>

<p align="center"><i>
Every number on this page is measured, not estimated. See <a href="#how-these-numbers-were-measured">how</a>.
</i></p>

---

### What I work on

- **~40 of the ~95 microservices** behind FabFunnel (marketing automation) and Lookfinity (multi-tenant ad platform)
- **The whole integration surface.** Twelve ad platforms (Meta, Google, TikTok, Snapchat, NewsBreak, OpenAI Ads, BIGO and others) plus the Voluum, Redtrack and Clickflare tracker sources. Every one has different auth, rate limits, pagination and metric definitions. I own the layer that reconciles all of them into a single model, so one query compares spend and revenue across every source.
- **Kafka → Vector → ClickHouse.** Four production clusters, ~2.3B rows stored, ~600B scanned per month, held at 113-216 ms p95
- **The automation engine.** Rule evaluations on a strict 15-minute cycle, ~1,700 runs/day scanning ~5.8B rows, executing budget and status changes against live advertiser accounts
- **A team of three engineers,** while staying hands-on across architecture, infrastructure and debugging

### Selected work

- **Originated the integration architecture.** First in Lookfinity, then rebuilt with better logic for FabFunnel. I started most of the platform services myself, including the one every later service is cloned from, and built the field-catalog and query engine that makes platform and tracker data comparable. The playbook I wrote for it halved from-scratch build time.
- **Security and reliability audit across 44 services.** 770 evidence-backed findings, then re-verified closure rather than assuming it. Remediated platform-wide defects in multi-tenant auth, SQL parameterisation and dependency resolution.
- **Automated testing where there was none.** A GraphQL contract and resolver harness that runs each service's real composed schema with only the I/O boundary mocked.
- **The engineering standards layer.** 122 task-level implementation guides across 42 repositories, plus a cross-service decision ledger.

### On AI

I use it heavily: investigation, code review, cross-repository analysis, large-scale audits. I also built the tooling the team uses for it, including an MCP server over our own platform data. The value isn't typing faster. It's taking on problems that would otherwise be too wide to attempt, and spending the time saved on judgement instead.

### How these numbers were measured

Not rounded up from memory. Each figure came out of a system I can query again:

| Claim | Source |
|---|---|
| 600B rows/month, 113-216 ms p95 | `system.query_log` across four production ClickHouse clusters, 30-day window |
| ~1,700 automation runs/day, 15-minute cycle | same, filtered to the rule engine's DB user. 100.0% of its queries land on :00/:15/:30/:45 |
| 15 integration sources reconciled | 12 platform service repos plus the tracker query builders in the reporting layer |
| 770 audit findings, 122 guides, 42 repos | counted in the documentation repo |
| ~40 of ~95 services | the company's service ownership register |

I had AI do the sweep across 50+ repositories and the production query logs, because the counting is wide and tedious and a person doing it by hand gets it wrong. The method is in the table. If a number here looks surprising, ask me how it was counted.

### Stack

**Frontend** React · Next.js · TypeScript · Redux Toolkit · Apollo Client
**Backend** Node.js · TypeScript · GraphQL (Apollo Federation) · Express · TypeORM
**Data** ClickHouse · PostgreSQL · MySQL · MongoDB · Redis · Kafka · RabbitMQ · Vector
**Infrastructure** Kubernetes · Helm · ArgoCD / GitOps · Docker · AWS · Jenkins · Grafana / Loki

### Before software

National-level table tennis player and coach. Coached 50+ students over five years, producing 15 state and 7 national players.

---

<p align="center">
<a href="https://www.linkedin.com/in/anmoljain987/"><img src="https://skillicons.dev/icons?i=linkedin" height="35"/></a>
<a href="https://twitter.com/IamAnmolJain"><img src="https://skillicons.dev/icons?i=twitter" height="35"/></a>
<a href="mailto:anmoljain987@gmail.com"><img src="https://skillicons.dev/icons?i=gmail" height="35"/></a>
</p>

<p align="center">
<img src="https://github-readme-stats.vercel.app/api?username=anmoljain987&show_icons=true&theme=radical" height="150"/>
<img src="https://github-readme-streak-stats.herokuapp.com/?user=anmoljain987&theme=radical" height="150"/>
</p>
