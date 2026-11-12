## Rodrigo Figueiredo

Fullstack web developer in Lisbon. My production years are in **JavaScript and PHP**; I also work in **TypeScript, React** and **Python (FastAPI)**.

Most recently Tech Manager & Fullstack Developer at **Rock in Rio Lisboa**, where I developed, redesigned and maintained the festival's official website — a custom JavaScript/PHP platform that served 1.9M users and 18M tracked events through the 2026 edition, with no downtime across the festival.

### What I publish here

**[framebudget](https://github.com/eimaieros/framebudget)** — a runtime frame budget for animated websites. It measures real frame timing in production and turns the animation down before the user feels the stutter. Percentile-based rather than mean-based, because nobody perceives an average. 61 tests, 12.6 KB minified, zero dependencies.

**[glaze](https://github.com/eimaieros/glaze)** — GPU effects over the DOM you already have. WebGPU, scroll-driven, and it never removes your content: the texture is uploaded before the element is hidden, and every failure path leaves the original page untouched. 94 tests, 17.5 KB minified, zero dependencies.

**[cadence](https://github.com/eimaieros/cadence)** — a technical interview simulator. FastAPI, PostgreSQL 16 with pgvector and Next.js, with answers streamed token by token over SSE, an interviewer that calls tools bound to the session on the server, and retrieval over the job description you paste in, measured with recall@k and MRR in CI. 236 tests; the 177 backend ones run against a real PostgreSQL, because the schema uses JSONB and native enums and a SQLite suite would pass while production broke.

**[cadence-mcp](https://github.com/eimaieros/cadence-mcp)** — an MCP server that lets an AI assistant run a cadence interview: start it, ask, answer and score, with a human confirmation before anything costly or irreversible. The interviewer's tool-call audit comes back to the assistant as records, never as instructions. 71 tests, types checked with `tsc --strict`.

**[boxoffice](https://github.com/eimaieros/boxoffice)** — a ticket-sales backend in Django and PostgreSQL. Tickets in a basket go back on sale by themselves through a Celery task that uses `FOR UPDATE SKIP LOCKED`; checkout takes an `Idempotency-Key`, so a retry or a double click makes one order; stock only moves inside a conditional `UPDATE`, with a `CHECK` constraint as the backstop. Orders are paid by signed webhooks from a stand-in payment provider, applied once, and checked with the provider before they expire in case a webhook got lost. 94 tests against a real PostgreSQL, including races run on real threads.

**[portfolio](https://github.com/eimaieros/portfolio)** — the source of [rodrigofigueiredo.dev](https://rodrigofigueiredo.dev). One HTML file, no framework, WebGL background on Three.js. A verification pipeline runs the page in jsdom with and without WebGL, audits accessibility and SEO, and blocks the build on regression.

**Tamagotchi** and **Personal-Finance-Tracking-App** are from February 2025 and stay up on purpose. The August 2026 commits on both are the interesting part: what I would do differently, done rather than described.

### Elsewhere

[rodrigofigueiredo.dev](https://rodrigofigueiredo.dev) · [LinkedIn](https://www.linkedin.com/in/rodrigomvfigueiredo) · eimaieros@gmail.com

Lisbon, Portugal · EU citizen, no visa needed to work anywhere in the EU.
