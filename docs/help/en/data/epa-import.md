# Importing findings from German EHR (ePA)

> **About ePA:** This page describes Germany's electronic patient record system (elektronische Patientenakte, abbreviated ePA). The feature is relevant if you live in Germany or use German healthcare services. Users outside Germany can skip this page; Phylax works without ePA integration.

!!! info "Placeholder (Iteration 1)"
    This page is part of the Stage 1 scaffolding. Full content will follow in a later iteration.

Findings from the German electronic patient record (ePA, _elektronische Patientenakte_) can be imported into the Phylax profile with AI assistance. Phylax does not interpret the findings; the AI only structures them for the living profile.

## Planned content for this page

- What the ePA is and which document types Phylax handles (PDF findings, physician letters, lab reports)
- Storing your own API key for OpenAI or Anthropic (zero-knowledge, no Phylax cloud)
- Uploading a document and selecting its source
- Preview of the AI suggestion before it is written to the database
- Source of imported entries: `ai` with a back-reference to the source document
- Privacy notes: data goes directly from the browser to the chosen AI provider, no Phylax backend involved

Status: Iteration 1 (placeholder)
