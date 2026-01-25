# BIBLIA-CONTENT Editorial Engine

**Version:** 1.0.0 (Stable)  
**Last Updated:** January 2026

## Overview

The **BIBLIA-CONTENT Editorial Engine** is a robust, structured repository of theological and pastoral content. Designed as a headless content source, it serves as the foundational database for publishing platforms, mobile applications, and academic study tools. 

This repository treats content as data, utilizing strict Markdown formatting combined with YAML Frontmatter to ensure portability, parsability, and long-term archival stability.

## Directory Structure

The repository follows a canonical hierarchical structure based on biblical indexing:

```text
/
├── biblia/
│   ├── {book_name}/           # Bible Book (e.g., 'salmos', 'genesis')
│   │   ├── {chapter_number}/  # Chapter (e.g., '97', '01')
│   │   │   ├── devocional-01.md
│   │   │   ├── estudo-tematico.md
│   │   │   ├── exposicao-homiletica.md
│   │   │   ├── mensagem-pastoral.md
│   │   │   ├── oracao.md
│   │   │   ├── temas-controversos.md
│   │   │   └── terminologias.md
```

## Data Schema

Every file is a Markdown document preambled by a YAML Frontmatter block. This metadata is critical for the indexing engine.

### Frontmatter Specification

```yaml
---
slug: string    # Unique identifier (e.g., "salmos-97-estudo-tematico")
titulo: string  # Display title of the content
tipo: enum      # Content type identifier
origem: string  # Source collection (default: "biblia")
livro: string   # Book name (normalized lowercase)
capitulo: int   # Chapter number
data: date      # ISO 8601 date (YYYY-MM-DD)
autor: string   # Content author/editor
tags: array     # List of keywords
---
```

### Content Types

The engine currently supports the following distinct content modules per chapter:

| Type Key | Description |
| :--- | :--- |
| `devocional-01` | Daily devotional reflections focused on practical application. |
| `estudo-tematico` | In-depth theological analysis of specific themes within the text. |
| `exposicao-homiletica` | Structured outlines and exegetical notes for preaching. |
| `mensagem-pastoral` | Pastoral letters or guidance derived from the chapter context. |
| `oracao` | Liturgical or spontaneous prayers based on the scripture. |
| `temas-controversos` | Apologetic discussions on difficult or debated passages. |
| `terminologias` | Lexical studies of key Hebrew/Greek terms found in the text. |

## Integration & Usage

### As a Datasource
This repository is designed to be consumed by static site generators (SSG) or CMS importers. 
- **Parsing**: Use a Markdown parser with YAML support (e.g., `gray-matter` in Node.js, `python-frontmatter`).
- **Indexing**: Files should be indexed by `livro` > `capitulo` for navigation trees.

### Editorial Standards
- **Encoding**: All files are UTF-8.
- **Markdown**: Standard CommonMark syntax.
- **Immutability**: Tags and branches marked `stable` (e.g., `stable-20260125`) represent finalized editorial content and should not be altered retroactively.

## License & Copying

**Copyright © 2026 Nascente Pensologocreio.**  
All Rights Reserved.

This material is proprietary editorial content. Unauthorized reproduction, distribution, or commercial use without express permission is prohibited.
