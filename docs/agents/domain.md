# Domain docs

This is a single-context repository.

## Before exploring

Read:

- `GLOSSARY.md` at the repository root.
- Relevant ADRs under `docs/adr/`, when present.

If a referenced document does not exist, proceed without treating its absence as an error.

## Use the glossary vocabulary

When naming a domain concept in an issue title, plan, hypothesis, test, or implementation note, use the term defined in `GLOSSARY.md`. If a needed concept is missing, treat that as a signal to clarify the language or update the glossary through the domain-modeling skill.

## Flag ADR conflicts

If work contradicts an existing ADR, surface the conflict explicitly rather than silently overriding it.

## Layout

```text
/
├── GLOSSARY.md
└── docs/adr/
```
