### Hi, I'm Dmytro

**Fullstack Developer (.NET / React) — 4+ years**

- Open Work Permit holder for Canada (valid through April 2029) — open to Canadian fullstack opportunities
- Currently: improving performance and shipping features on an AI-powered enterprise platform via Binary Studio
- Independently: building [ArbiScanner](http://www.arbiscannerwebapp.site/) — a 24/7 containerized crypto-arbitrage platform designed, built, and operated solo: 4 microservices (scanner engine, web API, admin panel, Telegram notifier), scanning 12+ exchanges across 3 strategies (futures, funding rate, spot-futures), real-time SignalR dashboard, protobuf over RabbitMQ, MongoDB + PostgreSQL + Redis, deployed on GCP with Grafana/Loki observability, and a full GitHub Actions CI/CD pipeline per service (SonarCloud quality gates, CodeQL scanning, Testcontainers-backed integration tests, GHCR image publishing, automated SSH deploy to the VPS)
- Recent measured impact: cut p95 latency 2×, CPU 2×, and memory 10× on a high-concurrency .NET / Elasticsearch service supporting 50–100 concurrent users at <0.2% error rate

#### Stack

**Backend** &mdash; C#, .NET, ASP.NET Core, Entity Framework, SignalR, WebRTC, MediaSoup, RabbitMQ, gRPC, Protocol Buffers  
**Frontend** &mdash; React, Redux Toolkit, MobX, Angular, TypeScript, Tailwind CSS  
**Data & caching** &mdash; SQL Server, PostgreSQL, Oracle, MongoDB, Elasticsearch, Redis  
**Infrastructure & CI/CD** &mdash; Docker, GitHub Actions (reusable workflows), GitHub Container Registry, Azure DevOps, Grafana, Loki, OpenTelemetry  
**Testing & quality** &mdash; xUnit, NUnit, FluentAssertions, Moq, Testcontainers, Vitest, SonarQube/SonarCloud, CodeQL, Veracode

#### What's pinned below

All five repos below are the ArbiScanner platform — a solo end-to-end project across backend, frontend, infrastructure, and ops:

- **SpreadScanner** — monorepo root: Docker Compose orchestration, shared `.env`, root solution (`ArbiScanner.slnx`), Grafana provisioning, and the reusable `deploy-service.yml` GitHub Actions workflow (test → build/push to GHCR → SSH deploy) shared by every service below
- **ArbiSpreadScanner.WebApp** — ASP.NET Core 10 Web API + React SPA: JWT auth, SignalR real-time push, RabbitMQ consumer, MongoDB + PostgreSQL + Redis, Clean Architecture
- **ArbiSpreadScanner.AdminPannel** — ASP.NET Core 10 admin API + React SPA: user and subscription management, OxaPay crypto payments, two isolated PostgreSQL databases, role-based access
- **ArbiSpreadScanner.TelegramNotifierApp** — .NET 10 worker: Telegram bot (account linking, notification opt-in/out) + RabbitMQ consumer that forwards spread alerts to subscribed users
- **ArbitrageSpreadScanner** — .NET 10 worker: the core scanning engine — 12+ exchanges via ccxt, parallel symbol processing, three strategies (futures, funding rate, spot-futures), proxy rotation, protobuf publishing to RabbitMQ, MongoDB persistence

Every service repo ships its own `ci.yml` (build, unit/integration tests, SonarCloud quality gate, CodeQL) and `deploy.yml` (calls the shared reusable workflow to publish a versioned image to GHCR and roll it out); the two user-facing APIs also run a scheduled/on-demand `load-test.yml`.

#### Connect

- Email: dimasdom72@gmail.com
- LinkedIn: [linkedin.com/in/dmytro-bartash-4133b41a0](https://www.linkedin.com/in/dmytro-bartash-4133b41a0/)
- Live project: [arbiscannerwebapp.site](http://www.arbiscannerwebapp.site/)
