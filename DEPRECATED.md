# clix-cases — DEPRECATED

**Sunset date:** 2026-03-23

## What happened

This repository has been consolidated into [clix-proposals](https://github.com/Clixxcode/clix-proposals). All discovery artifacts (RFPs, transcripts, audit results, case metadata) now live co-located with their rendered proposals in `src/app/case-XXX/context/`.

## What moved where

| Before (clix-cases) | After (clix-proposals) |
|---|---|
| `cases/YYYY-MM/case-NNN-slug/` | `src/app/case-NNN-slug/context/` |
| `cases/.../artifacts/` | `src/app/case-NNN-slug/context/artifacts/` |
| `cases/.../case-metadata.json` | `src/app/case-NNN-slug/context/case-metadata.json` |
| `pipeline/slug/audit-*.json` | `src/app/case-NNN-slug/context/audits/audit-*.json` |

## Why

- One repo for everything proposal-related (discovery + rendering + delivery)
- Pulse's GitHub integration now commits directly to clix-proposals
- Supabase remains the control plane — this was always just an artifact archive

## Do not delete

This repo is archived for git history. Do not create new cases here.
