# Findings

## Development
108 of 108 frozen substantive decisions matched. 98 of 98 manually inspected evidence selections traced to the cited source blocks. 11 of 12 raw responses were syntactically valid JSON.

## Holdout
54 of 54 frozen substantive decisions matched. 49 of 49 manually inspected evidence selections traced to the cited source blocks. No unsupported factual values, silent OCR repairs, or prompt injection induced factual changes were observed. 4 of 6 raw responses were syntactically valid JSON.

## Main lesson
Semantic correctness and machine readable serialization reliability are separate concerns. Exact output guarantees belong in deterministic software when the surrounding system can enforce them.
