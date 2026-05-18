### Hi, I'm Dmytro

**Fullstack Developer (.NET / React) — 4+ years**

- Open Work Permit holder for Canada (valid through April 2029) — open to Canadian fullstack opportunities
- Currently: improving performance and shipping features on an AI-powered enterprise platform via Binary Studio
- Independently: building [ArbiScanner](http://www.arbiscannerwebapp.site/) — a 24/7 containerized crypto-arbitrage platform designed, built, and operated solo: 4 microservices (scanner engine, web API, admin panel, Telegram notifier), scanning 12+ exchanges across 3 strategies (futures, funding rate, spot-futures), real-time SignalR dashboard, protobuf over RabbitMQ, MongoDB + PostgreSQL + Redis, deployed on GCP with Grafana/Loki observability
- Recent measured impact: cut p95 latency 2×, CPU 2×, and memory 10× on a high-concurrency .NET / Elasticsearch service supporting 50–100 concurrent users at <0.2% error rate

#### Stack

**Backend** &mdash; C#, .NET, ASP.NET Core, Entity Framework, SignalR, WebRTC, MediaSoup, RabbitMQ, gRPC, Protocol Buffers  
**Frontend** &mdash; React, Redux Toolkit, MobX, Angular, TypeScript, Tailwind CSS  
**Data & caching** &mdash; SQL Server, PostgreSQL, Oracle, MongoDB, Elasticsearch, Redis  
**Infrastructure** &mdash; Docker, Azure DevOps, Grafana, Loki, OpenTelemetry  
**Testing & quality** &mdash; NUnit, SonarQube, Veracode

#### What's pinned below

All five repos below are the ArbiScanner platform — a solo end-to-end project across backend, frontend, infrastructure, and ops:

- **SpreadScanner** — monorepo root: Docker Compose orchestration, shared `.env`, root solution (`ArbiScanner.slnx`), and Grafana provisioning for the full platform
- **ArbiSpreadScanner.WebApp** — ASP.NET Core 10 Web API + React SPA: JWT auth, SignalR real-time push, RabbitMQ consumer, MongoDB + PostgreSQL + Redis, Clean Architecture
- **ArbiSpreadScanner.AdminPannel** — ASP.NET Core 10 admin API + React SPA: user and subscription management, OxaPay crypto payments, two isolated PostgreSQL databases, role-based access
- **ArbiSpreadScanner.TelegramNotifierApp** — .NET 10 worker: Telegram bot (account linking, notification opt-in/out) + RabbitMQ consumer that forwards spread alerts to subscribed users
- **ArbitrageSpreadScanner** — .NET 9 worker: the core scanning engine — 12+ exchanges via ccxt, parallel symbol processing, three strategies (futures, funding rate, spot-futures), proxy rotation, protobuf publishing to RabbitMQ, MongoDB persistence

#### Connect

- Email: dimasdom72@gmail.com
- LinkedIn: [linkedin.com/in/dmytro-bartash-4133b41a0](https://www.linkedin.com/in/dmytro-bartash-4133b41a0/)
- Live project: [arbiscannerwebapp.site](http://www.arbiscannerwebapp.site/)
