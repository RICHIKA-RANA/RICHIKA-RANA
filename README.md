<p align="center">
  <a href="https://www.linkedin.com/in/richikarana/">LinkedIn</a> &nbsp;·&nbsp;
  <a href="mailto:richikarana18@gmail.com">richikarana18@gmail.com</a> &nbsp;·&nbsp;
  Bengaluru, India
</p>

# Richika Rana

*Most of what I build is the part you only notice when it breaks.*

I don't start from a framework. I start from a question nobody could answer yet, and work
backwards until the system can answer it, with its reasons attached.

A 100-page report where the answer sits in one cell of one table. A document that has to come
out redacted and still look like itself. A pipeline that took six hours and had no business
taking more than thirty.

<p align="center"><img src="https://raw.githubusercontent.com/RICHIKA-RANA/RICHIKA-RANA/main/art/hero.png" width="300" alt="an answer resting on the element, page and fragments it came from" /></p>

Backend, three years of it. Retrieval, ingestion, and the jobs that have to survive a restart.

---

### 🌳 [module-ttt](https://github.com/TalkingDB/module-ttt)

Ask a long document a question and most systems embed the whole thing, then hope the nearest
vector happens to be the right one.

<p align="center"><img src="https://raw.githubusercontent.com/RICHIKA-RANA/RICHIKA-RANA/main/art/ttt-tree.png" width="330" alt="a document opening into text, table and figure nodes, converging on an answer" /></p>

This one doesn't. It walks a tree of sections, tables and figures, so every answer has an
address. I own retrieval and ingestion. The published benchmark is **more than 90% fewer LLM
tokens per query** than OpenAI File Search with GPT-4o, across 93 questions.

Most of that came from a single idea: index tables as structured elements, so a question
resolves to a cell instead of a page.

`Python` · `FastAPI` · `symbolic AI`

---

### 🧩 [package-content-elementizer](https://github.com/TalkingDB/package-content-elementizer)

Before you can retrieve anything you have to admit what a document really is: half-merged table
cells, headings that are only bold text, paragraphs with no style attached at all.

<p align="center"><img src="https://raw.githubusercontent.com/RICHIKA-RANA/RICHIKA-RANA/main/art/elementizer.png" width="320" alt="a pile of pages becoming a typed, ordered list of elements" /></p>

This reads one and turns it into structured JSON. Every element classified by type, and
provenance carried all the way through so an answer can point back at where it came from. I
added PDF to a pipeline that had only ever spoken DOCX, which was mostly making peace with
irregular grids.

`Python` · `DOCX` · `PDF`

---

### 🔗 [package-named-entity-linker](https://github.com/TalkingDB/package-named-entity-linker)

In regulatory writing the same word is rarely the same thing twice.

<p align="center"><img src="https://raw.githubusercontent.com/RICHIKA-RANA/RICHIKA-RANA/main/art/entities.png" width="340" alt="ambiguous terms resolving into a graph of canonical entities" /></p>

So a term gets resolved against the rest of the document and a Wikibase knowledge base, rather
than guessed at in isolation. On the medical-writing platform this sat under, placeholder
resolution landed close to 90% accuracy.

`Python` · `Wikibase` · `NER`

---

### 🤖 [flowbot-framework](https://github.com/TalkingDB/flowbot-framework)

An agent is only as good as the tools you hand it, and a confident answer with no source is
worse than no answer.

I built the MCP server that exposes the TTT engine to these agents, and the chat where they
answer from a retrieved document instead of from memory.

`TypeScript` · `MCP` · `tool calling`

---

### 🚢 The unglamorous half

<p align="center"><img src="https://raw.githubusercontent.com/RICHIKA-RANA/RICHIKA-RANA/main/art/restart.png" width="340" alt="a pipeline stepping through a document, with a dashed path back to where it stopped" /></p>

[**sdk-talkingdb**](https://github.com/TalkingDB/sdk-talkingdb) is the surface everything else
talks to, which makes it the one place a bad decision stays expensive.
[**infra-tdb-platform**](https://github.com/TalkingDB/infra-tdb-platform) is local setup, repo
orchestration and deploys: GKE with YAML manifests through GitLab CI, later Bitbucket Pipelines.

Conversion is resumable and retries are race-safe, so a job restarts from the last batch it
finished rather than from the top. Somebody has to own the restart path. I'd rather it was me.

`Python` · `Shell` · `Kubernetes` · `GKE`

---

### 📚 Before this

**Wikimedia Foundation, Platform Engineering.** One of 8 interns picked worldwide from 15,000+
applicants. I deprecated the VirtualRestService abstraction across the
[Collection](https://phabricator.wikimedia.org/T336735) and
[Flow](https://phabricator.wikimedia.org/T337223) extensions: 6 merged Gerrit patches, 1,000+
lines of dead code gone, and a
[maintenance script that warms the Parsoid cache](https://phabricator.wikimedia.org/T338922),
shipped in MW 1.41.0-wmf.16. Deleting code in a codebase Wikipedia runs on teaches you to read
first and type later.

**eRaktKosh at C-DAC.** Java backend for India's national blood-bank platform, then live across
34 States and UTs. Cross-field validation on hospital records, because a wrong plasma count is
not a rounding error.

---

### 🌱 Where I started

[BookCart](https://github.com/RICHIKA-RANA/BookCart) in PHP, and
[VirusGame](https://richika-rana.github.io/VirusGame/) in plain JavaScript, in 2021. Leaving
them up on purpose. Everything above is the same instinct with better tools.

---

### What makes an answer trustworthy?

That's the question I keep ending up at. It's why tables got indexed as structures instead of
flattened into text, why provenance rides along with every element, why model-generated SQL got
replaced with parameterised queries so a clinical narrative comes out the same way twice, and
why a failed job reports a stated cause instead of a stack trace.

A system that is right is good. A system that can show you *why* it's right is the one people
actually use.

---

<p align="center">
  Open to backend and SDE2 roles · Bengaluru, Hyderabad or remote
</p>
