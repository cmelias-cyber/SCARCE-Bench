# Security Architecture (Draft Design)

**Status:** design draft. These are planned controls for the RAG assistant, not validated results. Part of the project is to test whether they hold.

## Goals

The RAG assistant is the system under test and also a public-facing prototype. The design aims to keep it inside its intended boundaries and to make its failures observable.

## Architecture

- The public website does not host the model. It connects to an external RAG endpoint through a custom API connection.
- Retrieval is limited to a documented, curated corpus, and the assistant answers only from retrieved material or abstains.

## Planned controls

- **Retrieval boundaries.** Queries can reach only the approved corpus. Held-out evaluation material is stored separately and is never indexed for the public assistant.
- **Access controls.** The endpoint requires authorization, and credentials are kept out of the repository.
- **Rate limits.** Per-user and global limits reduce abuse and runaway costs.
- **Prompt-injection resistance.** The system prompt and retrieved text are treated as separate trust levels, and the assistant is tested against injected instructions in queries and in retrieved content.
- **Data leakage.** Tests check whether the assistant can be made to reveal system instructions, other users' queries, or non-public corpus material.
- **Logging.** Queries are logged for research after personal data is stripped, and users are told that logging happens.
- **Monitoring and containment.** Failures are flagged for review, and the assistant can be taken offline quickly.

## Threat categories to test

- Direct prompt injection through user queries
- Indirect prompt injection through retrieved documents
- Extraction of system instructions or hidden material
- Retrieval outside the approved corpus
- Abuse through high-volume or automated queries

## Relationship to the research questions

These controls are secondary engineering safeguards. The primary research questions remain source conflation and false certainty.
