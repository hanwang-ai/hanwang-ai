### Small tools that actually run

I build things that fix a problem I hit myself, then publish the evidence: the real test output,
the failure the tool repairs, and what it cannot do.

Most of what is here started on my own machine — a tunnel that dies and leaves a webhook provider
pointing at a URL that no longer exists, dead console windows piling up on the taskbar, database
services eating a gigabyte of RAM at every boot. Each repo is the real fix, generalised enough
that a stranger can clone it and run it.

---

#### Worth opening

| Repo | What it does | Built with |
|---|---|---|
| [rag-support-bot](https://github.com/hanwang-ai/rag-support-bot) | Support chatbot that answers from a company's own docs (real business content, not dummy data), says "I don't know" instead of inventing, and files a ticket for a human | n8n · Supabase pgvector · DeepSeek |
| [service-tunnel-watchdog](https://github.com/hanwang-ai/service-tunnel-watchdog) | Keeps a local service **and** its public tunnel alive on Windows — and re-registers the service when the tunnel comes back with a new hostname | PowerShell |
| [zombie-window-cleaner](https://github.com/hanwang-ai/zombie-window-cleaner) | Closes the orphaned console windows that service launchers leave behind, on a schedule, without ever touching the running service | PowerShell |
| [algorithm-class-demos](https://github.com/hanwang-ai/algorithm-class-demos) | Eleven interactive visualizations for a Data Structures course — the lecture's own C++ code executed frame by frame, with the call stack drawn and a recursion tree that grows as you step. **[Live demo ↗](https://hanwang-ai.github.io/algorithm-class-demos/)** | HTML/CSS/JS |
| [AIMail](https://github.com/hanwang-ai/AIMail) | Gmail auto-classification: an LLM reads every message and stars, archives or leaves it alone according to rules written in plain language | Google Apps Script · DeepSeek |
| [SQL-Dictionary](https://github.com/hanwang-ai/SQL-Dictionary) | Offline SQL syntax dictionary — browse by category, one-click copy, bilingual notes, no install and no network | C++ · Qt 6 · SQLite |

#### How I build

- **It ran on the real thing before it was published.** Where a tool touches processes, files or
  services, the README quotes output from an actual run against a fabricated version of the failure.
- **Tests reproduce the fault and assert the fix in both directions** — the broken state it must
  repair, and the healthy state it must not break. A process-killing utility that fails the second
  test is worse than no utility.
- **Every README has a limitations section.** If a tool cannot do something, the page says so.
- **Written in English**, committed plainly, MIT licensed.

#### Currently

- Data structures and algorithms in C++ — my own implementations, not only notes
- LLM application work: retrieval, rule-driven classification, and agents that escalate instead of guessing
- Turning the Windows utilities I run daily into repos a stranger can install

<sub>Ask about any repo above — I can explain the design decisions behind it.</sub>
