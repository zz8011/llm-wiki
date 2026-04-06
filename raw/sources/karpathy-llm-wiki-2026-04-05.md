---
type: source
title: "LLM Wiki"
author: Andrej Karpathy
url: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
date: 2026-04-05
tags: [AI, 知识管理, LLM, 个人知识库]
---

# LLM Wiki

A pattern for building personal knowledge bases using LLMs.

## The Core Idea

Most people's experience with LLMs and documents looks like RAG: you upload a collection of files, the LLM retrieves relevant chunks at query time, and generates an answer. This works, but the LLM is rediscovering knowledge from scratch on every question. There's no accumulation.

The idea here is different. Instead of just retrieving from raw documents at query time, the LLM incrementally builds and maintains a persistent wiki — a structured, interlinked collection of markdown files that sits between you and the raw sources. When you add a new source, the LLM doesn't just index it for later retrieval. It reads it, extracts the key information, and integrates it into the existing wiki — updating entity pages, revising topic summaries, noting where new data contradicts old claims, strengthening or challenging the evolving synthesis. The knowledge is compiled once and then kept current, not re-derived on every query.

## Architecture

Three layers:
1. **Raw sources** — immutable source documents
2. **Wiki** — LLM-generated markdown files
3. **Schema** — configuration file (e.g. CLAUDE.md)

## Operations

- **Ingest**: Process new sources, create/update wiki pages
- **Query**: Ask questions against the wiki
- **Lint**: Health-check the wiki periodically

## Why This Works

The tedious part of maintaining a knowledge base is not the reading or the thinking — it's the bookkeeping. LLMs don't get bored, don't forget to update a cross-reference, and can touch 15 files in one pass.

## Tools

- Obsidian Web Clipper
- Obsidian Git
- qmd (local search)
- Marp (slides)
- Dataview
