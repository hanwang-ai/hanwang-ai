### Hi, I'm Wang Han

Computer Science student (SQA-AD programme, UESTC · Chengdu, China). I build small, complete
tools and then write down what actually happened — real test output, not adjectives.

Most of what is here started as a problem on my own machine: a tunnel that dies and leaves a
webhook provider pointing at a URL that no longer exists, dead console windows piling up on the
taskbar, MySQL and Oracle eating a gigabyte of RAM at every boot. Each repo is the real fix,
generalised enough that a stranger can clone it and run it.

---

#### Worth opening

| Repo | What it does | Built with |
|---|---|---|
| [rag-support-bot](https://github.com/uhygyuf/rag-support-bot) | Support chatbot that answers from a company's own docs (real business content, not dummy data), says "I don't know" instead of inventing, and files a ticket for a human | n8n · Supabase pgvector · DeepSeek |
| [service-tunnel-watchdog](https://github.com/uhygyuf/service-tunnel-watchdog) | Keeps a local service **and** its public tunnel alive on Windows — and re-registers the service when the tunnel comes back with a new hostname | PowerShell |
| [zombie-window-cleaner](https://github.com/uhygyuf/zombie-window-cleaner) | Closes the orphaned console windows that service launchers leave behind, on a schedule, without ever touching the running service | PowerShell |
| [algorithm-class-demos](https://github.com/uhygyuf/algorithm-class-demos) | Interactive, step-by-step visualizations for a university Data Structures course — the lecture's own C++ code, executed frame by frame with the call stack drawn | HTML/CSS/JS |
| [AIMail](https://github.com/uhygyuf/AIMail) | Gmail auto-classification: an LLM reads every message and stars, archives or leaves it alone according to rules written in plain language | Google Apps Script · DeepSeek |
| [SQL-Dictionary](https://github.com/uhygyuf/SQL-Dictionary) | Offline SQL syntax dictionary — browse by category, one-click copy, bilingual notes, no install and no network | C++ · Qt 6 · SQLite |

#### How I build

- **It ran on the real thing before it was published.** Where a tool touches processes, files or
  services, the README quotes output from an actual run against a fabricated version of the failure.
- **Tests reproduce the fault and assert the fix in both directions** — the broken state it must
  repair, and the healthy state it must not break. A process-killing utility that fails the second
  test is worse than no utility.
- **Every README has a limitations section.** If a tool cannot do something, the page says so.
- **Written in English**, committed plainly, MIT licensed.

#### Currently

- Data structures and algorithms in C++ (my own implementations, not just notes)
- LLM application work: retrieval, rule-driven classification, agents that escalate instead of guessing
- Preparing for a UK BSc top-up in computer science

<sub>Ask me about any repo in the list above — I can explain the design decisions behind it.</sub>
