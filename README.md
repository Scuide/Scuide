# Evan Seilz

Software developer in Berlin. Backend services and the interfaces around them —
currently a lot of LLM-backed document processing, plus keeping a grown Java
application alive and moving.

## What I work on

**Document extraction with language models.** FastAPI and Pydantic services that turn
scanned administrative documents into structured data. I built the evaluation harness
for it: automated comparison of prompt variants against ground truth captured by hand,
scored as hit rate rather than equality. A pipeline you cannot measure is a pipeline
you cannot change.

**Agent platform.** Several single-purpose agents behind one gateway, LangChain and
FAISS for retrieval, used daily by around a hundred people.

**Registry data standards.** XMeld over OSCI, part of the German XÖV family. A new
protocol version lands every six months and I run that migration. There is no
counterpart to ask whether you got it right, so correctness has to come from the
specification.

**Legacy, honestly.** Java 17 with JSF and PrimeFaces. Kept alive and modernised in
place instead of rewritten.

## Things I built myself

**DMX lighting control** for a Berlin club, written in [vvvv](https://vvvv.org), a
visual dataflow language. Software, cabling and fixture layout are mine. Running every
weekend since 2023 without anyone else maintaining it. Hard real time: roughly 20 ms
per frame, and DMX is unidirectional, so you send without acknowledgement and find
faults by halving the chain.

**Home automation platform.** Home Assistant with around 1,100 entities and 120
automations, with a self-built assistant layer on top. The automation layer decides
*when* something is relevant — triggers, thresholds, cooldowns, deduplication. The
assistant decides only *how* it is phrased and through which channel. The language
model is deliberately not in the control path: latency, cost, and faults you cannot
reproduce.

**Final apprenticeship project.** A company-wide quiz platform. OpenAPI specification
first, TypeScript client generated from it rather than hand-written, Spring Boot and
PostgreSQL behind. Built alone and defended before the chamber of commerce
examination board.

## How I work

**Contract first.** I write the interface before the implementation — OpenAPI in one
project, Pydantic schemas in another, a custom event schema in a third. Three
projects, same approach, arrived at independently each time. A broken contract should
fail at compile time, not at the user.

**State over events.** An event is gone once nobody picks it up. A fact stays until it
has been delivered. Most "the notification never arrived" bugs are this one mistake.

**Test what is testable, monitor what is not** — and know which class of fault each
one catches. Monitoring finds that something is not running. Tests find that something
is running wrong.

## Tech

Python · FastAPI · Pydantic · Java 17 · Spring Boot · TypeScript · React · Next.js ·
PostgreSQL · Docker · Kubernetes · GitLab CI · LangChain · MCP · vvvv

## A note on this profile

Most of what I write lives in a private company repository and stays there. What is
public here is older or personal. I am slowly extracting the parts of my own setup
that make sense standing on their own.

## Elsewhere

[LinkedIn](https://www.linkedin.com/in/evan-seilz-012053151/)
