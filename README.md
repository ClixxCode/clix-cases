# Clix Cases

Case artifacts, enrichment, and proposal records for The Clix Group.

## Structure

cases/
├── 2026-03/
│ ├── case-001-multisorb/
│ │ ├── proposal.mdx # Proposal document
│ │ ├── case-metadata.json # Case metadata
│ │ └── artifacts/ # Artifacts (RFPs, transcripts, etc)


## Workflow

1. **Create case folder:** `cases/YYYY-MM/case-NNN-{slug}/`
2. **Create case-metadata.json** with case details
3. **Upload artifacts** to `artifacts/` subdirectory
4. **Generate proposal.mdx** from enrichment analysis
5. **Push:** Trigger ISR revalidation on proposals.clix.co

## Access

- Private repository
- Linked to Pulse case system via case_id
- Webhook-triggered revalidation on case updates
