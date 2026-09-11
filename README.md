<div align="center">
  <img width="100%" height="auto" src="https://raw.githubusercontent.com/MuhammadUmarAbbas2011/MuhammadUmarAbbas2011/main/assets/hero.svg" alt="Muhammad Umar Abbas — Full Stack AI Architect" />
</div>

---

### `// 01` philosophy

> I build the machine around the AI — not the API call.

RAG is only impressive when the system around it survives real use: authentication, sessions that degrade gracefully, background jobs that retry, migrations that don't break, and tests that run before anything ships. I treat every project as a full system, so the AI layer, the queue layer, and the deploy layer are equally important.

### `// 02` the system

<img width="100%" height="auto" src="https://raw.githubusercontent.com/MuhammadUmarAbbas2011/MuhammadUmarAbbas2011/main/assets/pipeline.svg" alt="Full-stack AI system pipeline" />

---

### `// 03` toolkit

No badge walls. Here is the stack I actually use, mapped by layer.

<img width="100%" height="auto" src="https://raw.githubusercontent.com/MuhammadUmarAbbas2011/MuhammadUmarAbbas2011/main/assets/stack.svg" alt="Technology stack by layer" />

---

### `// 04` Nexorithm — RAG as a platform

A FastAPI backend that answers competitive-programming questions using retrieval-augmented generation over Codeforces and LeetCode problems. Retrieval is one stage — the rest is a real platform.

<img width="100%" height="auto" src="https://raw.githubusercontent.com/MuhammadUmarAbbas2011/MuhammadUmarAbbas2011/main/assets/nexorithm-arch.svg" alt="Nexorithm architecture" />

<details>
  <summary><b>Inside the platform</b></summary>

- RAG pipeline: source parsing → normalization → `FastEmbed` vectors → `Qdrant` index → semantic retrieval → grounded generation via Groq LLM
- Authentication: `JWT` access + OTP email verification
- Sessions: `Redis` first, PostgreSQL fallback when Redis is unavailable
- Async: `Celery` for email and background tasks
- Code execution: sandboxed executor for user-submitted solutions
- Data layer: `PostgreSQL` + `SQLAlchemy` + `Alembic` migrations
- Quality: `pytest` suite; service bootstrapped with `Docker Compose`

**Frontend**: [Nexorithm-Frontend](https://github.com/MuhammadUmarAbbas2011/Nexorithm-Frontend) — React + Vite + TypeScript client.
</details>

➜ [Nexorithm](https://github.com/MuhammadUmarAbbas2011/Nexorithm)

### `// 05` JobHuntly — orchestration around scraping

A Django application that collects job listings, extracts the user's resume, and ranks matches using `TF-IDF` + cosine similarity — then keeps the user informed in real time.

<img width="100%" height="auto" src="https://raw.githubusercontent.com/MuhammadUmarAbbas2011/MuhammadUmarAbbas2011/main/assets/jobhuntly-pipeline.svg" alt="JobHuntly pipeline" />

<details>
  <summary><b>Inside the platform</b></summary>

- Scraping: `Playwright` and `undetected-chromedriver` + `BeautifulSoup`
- Resume parsing: `PyMuPDF` text extraction
- Matching: `TF-IDF` vectorization + `cosine similarity` scoring
- Async: `Celery` with retries; `Celery Beat` schedules scraping runs
- Real-time: `Django Channels` WebSockets for live progress
- Auth: `JWT` + OTP email verification
- Deployment: `Docker Compose` with Redis broker

**Frontend**: [JobHuntly-Frontend](https://github.com/MuhammadUmarAbbas2011/JobHuntly-Frontend) — React + Tailwind client.
</details>

➜ [JobHuntly](https://github.com/MuhammadUmarAbbas2011/JobHuntly)

---

### `// 06` more builds

| Project | What it is | Core stack |
| --- | --- | --- |
| [scjobs](https://github.com/MuhammadUmarAbbas2011/scjobs) | Glassdoor job scraper | Playwright (TypeScript) |
| [PrivHarbor](https://github.com/MuhammadUmarAbbas2011/PrivHarbor) + [frontend](https://github.com/MuhammadUmarAbbas2011/Priv-Harbor-frontend) | Phishing URL detection with malware scanning | Python, VirusTotal API, heuristics |
| [Ayat-According-To-Feeling](https://github.com/MuhammadUmarAbbas2011/Ayat-According-To-Feeling) | Quranic verses suggested by emotional state | Django, Google Gemini (`gemini-2.0-flash`) |

### `// 07` engineering philosophy

<img width="100%" height="auto" src="https://raw.githubusercontent.com/MuhammadUmarAbbas2011/MuhammadUmarAbbas2011/main/assets/philosophy.svg" alt="Learn — Build — Break — Debug — Improve — Ship" />

---

<div align="center">
  <img height="190" src="https://github-readme-stats.vercel.app/api?username=MuhammadUmarAbbas2011&show_icons=true&bg_color=0d1117&title_color=58a6ff&icon_color=8b5cf6&text_color=c9d1d9&hide_border=true&count_private=true" alt="GitHub stats" />
  <img height="190" src="https://streak-stats.demolab.com/?user=MuhammadUmarAbbas2011&background=0d1117&border=30363d&stroke=21262d&ring=58a6ff&fire=8b5cf6&currStreakNum=c9d1d9&sideNums=8b949e&currStreakLabel=c9d1d9&sideLabels=8b949e&dates=8b949e" alt="GitHub streak" />
</div>

---

<div align="center">
  <a href="https://github.com/MuhammadUmarAbbas2011">github</a> ·
  <a href="https://muhammadumar.qzz.io">portfolio</a>
</div>
