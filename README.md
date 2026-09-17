# Hallucination Resistant Document Extraction Workflow

Independent AI systems case study exploring evidence first contract extraction, provenance preservation, uncertainty states, controlled hallucination testing, and responsibility separation between language models, deterministic validation, and human review.

This repository documents a controlled portfolio experiment rather than a deployed product. The benchmark used synthetic contracts. The executions were conversational model runs rather than independent API tests.

## Portfolio Visuals
![Case Study 2 visual 01](assets/Upwork%20Case%20Study%202%20visual%2001.png)
![Case Study 2 visual 02](assets/Upwork%20Case%20Study%202%20visual%2002.png)
![Case Study 2 visual 03](assets/Upwork%20Case%20Study%202%20visual%2003.png)

## What was tested

Eight contract fields were extracted with five evidence states: SUPPORTED, MISSING, AMBIGUOUS, CONFLICTING, and UNREADABLE.

The workflow tested missing information, contradictory clauses, OCR corruption, prompt injection style text, false monetary cues, explicit versus plausible dates, per party conflicts, and formula based liability caps.

## Results

Development Benchmark V1 contained 12 synthetic contracts. The controlled development run matched 108 of 108 frozen substantive decisions. Eleven of twelve raw outputs were syntactically valid JSON.

The unseen holdout contained 6 new synthetic contracts. The frozen prompt matched 54 of 54 frozen substantive decisions and 49 of 49 manually inspected evidence selections traced to the cited source blocks. Four of six raw outputs were syntactically valid JSON.

The raw JSON failures are preserved as a real result. They support the architectural conclusion that semantic extraction and exact serialization are different responsibilities.

## Architecture

1. Preserve the original document and raw text or OCR with stable source identifiers.
2. Use the language model for semantic extraction and evidence selection.
3. Use deterministic software for JSON parsing, schema enforcement, exact evidence verification, and routing rules.
4. Send ambiguous, conflicting, unreadable, or otherwise unresolved evidence to human review.

## Repository contents

`docs/` contains the problem definition, architecture, experiment design, findings, and limitations.

`prompts/` contains the final frozen extraction prompt.

`data/` contains benchmark summaries and result summaries. Hidden gold answers were kept separate from the model during holdout execution.

## Important limitations

This is not production accuracy evidence, legal reliability evidence, a security proof, or deployment readiness evidence. No real customer contracts were processed. No production cost, latency, privacy, monitoring, or throughput measurements were taken.
