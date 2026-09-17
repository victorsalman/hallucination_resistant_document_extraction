# Architecture

## Source layer
Preserve original document, raw extracted text or OCR, stable source identifiers, page and section metadata where available.

## Language model layer
Perform semantic interpretation, evidence selection, ambiguity recognition, conflict recognition, and candidate structured extraction.

## Deterministic validation layer
Parse JSON, enforce schema, validate allowed fields and states, verify source identifiers, verify exact decoded source text against the cited block, reject malformed output, and route unresolved fields.

## Human review layer
Review ambiguous, conflicting, unreadable, or otherwise unresolved evidence with access to original source evidence.
