<div align="center">
  <img width="100%" height="auto" src="https://raw.githubusercontent.com/MuhammadUmarAbbas2011/MuhammadUmarAbbas2011/main/assets/hero.svg" alt="Muhammad Umar Abbas — Full-stack AI Architect" />
</div>

I build the machine around the AI, not the API call. Retrieval and generation are one stage in a request's life — the rest is authentication, sessions that degrade instead of dying, jobs that retry, migrations that don't break production, and tests that run before anything ships. Below is what that actually looks like, not a stack of badges.

## Parts catalog

<img width="100%" height="auto" src="https://raw.githubusercontent.com/MuhammadUmarAbbas2011/MuhammadUmarAbbas2011/main/assets/skills.svg" alt="Skills grouped by layer: AI/retrieval, backend, data, async, automation, frontend, infrastructure" />

## How a request actually moves through the system

<img width="100%" height="auto" src="https://raw.githubusercontent.com/MuhammadUmarAbbas2011/MuhammadUmarAbbas2011/main/assets/system-diagram.svg" alt="Exploded diagram of the request lifecycle, with the LLM drawn as the smallest component" />

JobHuntly follows the same shape with different labels: auth and sessions are identical, retrieval becomes Playwright scraping, and generation becomes TF-IDF + cosine similarity scoring against a parsed resume.

## What breaks, and what happens next

Anyone can show a working demo. The interesting part is what the system does when something goes wrong.

<img width="100%" height="auto" src="https://raw.githubusercontent.com/MuhammadUmarAbbas2011/MuhammadUmarAbbas2011/main/assets/failure-modes.svg" alt="Failure modes and how each one is handled" />

## Nexorithm — RAG as a platform

FastAPI backend answering competitive-programming questions over Codeforces and LeetCode problems.

- Retrieval: source parsing → normalization → FastEmbed vectors → Qdrant index → semantic search → grounded generation via Groq
- Auth: JWT access + OTP email verification
- Sessions: Redis first, PostgreSQL fallback when Redis is unavailable
- Async: Celery for email and background tasks
- Sandboxed executor for user-submitted solutions
- Data: PostgreSQL + SQLAlchemy + Alembic migrations, gated by a pytest suite
- Bootstrapped with Docker Compose

**Frontend:** [Nexorithm-Frontend](https://github.com/MuhammadUmarAbbas2011/Nexorithm-Frontend) — React + Vite + TypeScript

**Repo:** [Nexorithm](https://github.com/MuhammadUmarAbbas2011/Nexorithm)

## JobHuntly — orchestration around scraping

Django application that collects listings, parses the user's resume, and ranks matches — then keeps the user informed while it works.

- Scraping: Playwright + undetected-chromedriver + BeautifulSoup
- Resume parsing: PyMuPDF text extraction
- Matching: TF-IDF vectorization + cosine similarity
- Async: Celery with retries; Celery Beat schedules scraping runs
- Real-time: Django Channels WebSockets for live progress
- Auth: JWT + OTP email verification
- Deployment: Docker Compose with a Redis broker

**Frontend:** [JobHuntly-Frontend](https://github.com/MuhammadUmarAbbas2011/JobHuntly-Frontend) — React + Tailwind

**Repo:** [JobHuntly](https://github.com/MuhammadUmarAbbas2011/JobHuntly)

## More builds

| Project | What it is | Core stack |
| --- | --- | --- |
| [scjobs](https://github.com/MuhammadUmarAbbas2011/scjobs) | Glassdoor job scraper | Playwright (TypeScript) |
| [PrivHarbor](https://github.com/MuhammadUmarAbbas2011/PrivHarbor) + [frontend](https://github.com/MuhammadUmarAbbas2011/Priv-Harbor-frontend) | Phishing URL detection with malware scanning | Python, VirusTotal API, heuristics |
| [Ayat-According-To-Feeling](https://github.com/MuhammadUmarAbbas2011/Ayat-According-To-Feeling) | Quranic verses suggested by emotional state | Django, Google Gemini (gemini-2.0-flash) |

Exploring next: Go, Rust, Elasticsearch, distributed systems.

## How I work

Learn a new piece of the stack → build something small with it → break it on purpose → find the actual root cause → measure the fix → ship it, then repeat. Every project is practice for the next one.

---

<div align="center">
  <img height="180" src="https://github-readme-stats.vercel.app/api?username=MuhammadUmarAbbas2011&show_icons=true&bg_color=0d2843&title_color=eaf2fa&icon_color=f5a524&text_color=7f9db8&hide_border=true&count_private=true" alt="GitHub stats" />
  <img height="180" src="https://streak-stats.demolab.com/?user=MuhammadUmarAbbas2011&background=0d2843&border=5f83a6&stroke=5f83a6&ring=f5a524&fire=f5a524&currStreakNum=eaf2fa&sideNums=7f9db8&currStreakLabel=eaf2fa&sideLabels=7f9db8&dates=7f9db8" alt="GitHub streak" />
</div>

<div align="center">
  <a href="https://github.com/MuhammadUmarAbbas2011">github</a> ·
  <a href="https://muhammadumar.qzz.io">portfolio</a>
</div>
