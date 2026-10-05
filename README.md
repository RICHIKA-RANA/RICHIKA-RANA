<p align="center"><a href="https://www.linkedin.com/in/richikarana/">LinkedIn</a> &nbsp;·&nbsp; <a href="mailto:richikarana18@gmail.com">richikarana18@gmail.com</a> &nbsp;·&nbsp; Bengaluru, India</p>

# Richika Rana

*Most of what I build is the part you only notice when it breaks.*

I don't start from a framework. I start from a question nobody could answer yet, and work backwards until the
system can answer it, with its reasons attached. A 100-page report where the answer sits in one cell of one
table. A document that has to come out redacted and still look like itself. A pipeline that took six hours and
had no business taking more than thirty.

<p align="center"><img src="https://raw.githubusercontent.com/RICHIKA-RANA/RICHIKA-RANA/main/art/hero.png" width="420" alt="scattered material resolving through a structured element into one answer" /></p>

---

### 🌳 [module-ttt](https://github.com/TalkingDB/module-ttt) · 🧩 [package-content-elementizer](https://github.com/TalkingDB/package-content-elementizer)

<table>
<tr><td width="55%" align="center"><img src="https://raw.githubusercontent.com/RICHIKA-RANA/RICHIKA-RANA/main/art/ttt-tree.png" width="420" alt="a path descending through document, section, table and row to one cell" /></td><td width="45%" align="center"><img src="https://raw.githubusercontent.com/RICHIKA-RANA/RICHIKA-RANA/main/art/elementizer.png" width="290" alt="a pile of pages becoming a typed, ordered list of elements" /></td></tr>
<tr><td align="center"><em>Where exactly is the answer?</em></td><td align="center"><em>What is this document made of?</em></td></tr>
</table>

Ask a long document a question and most systems embed the whole thing, then hope the nearest vector happens to
be the right one. TTT walks a tree of sections, tables and figures instead, so **every answer has an address**.
I own retrieval and ingestion, and the published benchmark is more than 90% fewer LLM tokens per query than
OpenAI File Search with GPT-4o, across 93 questions.

Before you can retrieve anything you have to admit what a document really is: half-merged cells, headings that
are only bold text, paragraphs carrying no style at all. The elementizer turns one into typed JSON elements with
provenance riding along, and learned PDF after a lifetime of speaking only DOCX.

`Python` · `FastAPI` · `symbolic AI` · `DOCX` · `PDF`

---

### 🔗 [package-named-entity-linker](https://github.com/TalkingDB/package-named-entity-linker)

In regulatory writing the same word is rarely the same thing twice.

<p align="center"><img src="https://raw.githubusercontent.com/RICHIKA-RANA/RICHIKA-RANA/main/art/entities.png" width="380" alt="the same term resolving to different entities depending on surrounding context" /></p>

So a term resolves against the rest of the document and a Wikibase knowledge base rather than in isolation.
Close to 90% resolution accuracy on the medical-writing platform it sat under.

`Python` · `Wikibase` · `NER`

---

### 🤖 [flowbot-framework](https://github.com/TalkingDB/flowbot-framework)

An agent is only as good as the tools you hand it, and a confident answer with no source is worse than no
answer. I built the MCP server that exposes the TTT engine to these agents, and the chat where they answer from
a retrieved document instead of from memory.

`TypeScript` · `MCP` · `tool calling`

---

### 🚢 The unglamorous half

<p align="center"><img src="https://raw.githubusercontent.com/RICHIKA-RANA/RICHIKA-RANA/main/art/restart.png" width="380" alt="work interrupted, state saved, and the run resuming from where it stopped" /></p>

[**sdk-talkingdb**](https://github.com/TalkingDB/sdk-talkingdb) is the surface everything else talks to, which
makes it the one place a bad decision stays expensive.
[**infra-tdb-platform**](https://github.com/TalkingDB/infra-tdb-platform) is local setup, repo orchestration and
deploys, on GKE through GitLab CI and later Bitbucket Pipelines. Somebody has to own the restart path. I'd
rather it was me.

`Python` · `Shell` · `Kubernetes` · `GKE`

---

### 📚 Before this

**Wikimedia Foundation, Platform Engineering** — one of 8 interns picked worldwide from 15,000+ applicants. Six
merged Gerrit patches deprecating VirtualRestService across
[Collection](https://phabricator.wikimedia.org/T336735) and [Flow](https://phabricator.wikimedia.org/T337223),
1,000+ lines of dead code gone, and a [script warming the Parsoid
cache](https://phabricator.wikimedia.org/T338922) shipped in MW 1.41.0-wmf.16. Deleting code in a codebase
Wikipedia runs on teaches you to read first and type later.

**eRaktKosh at C-DAC** — Java backend for India's national blood-bank platform, live across 34 States and UTs.

**[BookCart](https://github.com/RICHIKA-RANA/BookCart)** in PHP and
**[VirusGame](https://richika-rana.github.io/VirusGame/)** in plain JavaScript, 2021. Leaving
them up on purpose.

---

### What makes an answer trustworthy?

Tables indexed as structures rather than flattened into text. Provenance riding along with every element.
Parameterised queries where a model used to write the SQL. A failed job that reports a stated cause.

A system that is right is good. A system that can show you *why* it's right is the one people actually use.

---

<p align="center">Open to backend and SDE2 roles · Bengaluru, Hyderabad or remote</p>
