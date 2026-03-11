# CLAUDE.md — clix-cases

## Purpose
Case artifacts, enrichment outputs, and discovery records for The Clix Group.
This is the **input/discovery layer** — structured context that feeds proposal generation.

Proposals do NOT live here. They go to `clix-proposals`.

## Folder Convention
```
cases/
└── YYYY-MM/
    └── case-NNN-{slug}/
        ├── case-metadata.json       # Case details snapshot (from Supabase)
        ├── brief.md                 # Goals, pain points, talking points
        ├── brand-extract.md         # Tone, visual direction, messaging
        ├── artifacts/               # BD-uploaded files (RFPs, transcripts, etc.)
        ├── audits/
        │   ├── seo-audit.md
        │   ├── technical-audit.md
        │   └── competitor-audit.md
        └── enrichment/
            └── domain-crawl.md      # Tech stack, site issues, quick wins
```

## Naming
- Folder: `case-{number}-{account-slug}` (e.g., `case-001-multisorb`)
- Month grouping: `YYYY-MM` (e.g., `2026-03`)
- All lowercase, hyphens only

## What Goes Here
- Case metadata snapshots (`case-metadata.json`)
- Discovery artifacts uploaded by BDs (PDFs, transcripts, docs)
- AI-generated audit outputs (SEO, technical, competitor)
- Brand extraction and domain enrichment results
- Brief summaries generated from context interpretation

## What Does NOT Go Here
- Proposals (→ `clix-proposals`)
- Binary assets like logos/screenshots (→ Supabase Storage)
- Operational state or status (→ Supabase `ops` schema)
- Proposal rendering code or components (→ `clix-proposals`)

## Constraints
- Do not modify files outside the active case folder
- Do not create case folders manually — Pulse scaffolds via GitHub API
- Do not write binary files — use Supabase Storage URLs
- Do not change case status here — Supabase `ops.sales_cases` is the control plane
