# AI_OPERATING_INSTRUCTIONS

**Applies To:** ChatGPT / Claude / Cursor / AI Agents  
**Package:** `Studio OS Core Package v1.0`

## Source of Truth

1. Use `STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md` as the current Studio OS source-of-truth map.
2. Use `REVIEWER_RUNTIME_SPECIFICATION_v1.0.md` as the Reviewer execution baseline.
3. Use current `CANONICAL_ACTIVE` documents.
4. Load `CANONICAL_CONDITIONAL` Genre Baselines only when Runtime routing requires them.
5. `REFERENCE` documents are evidence lookup sources, not direct Reviewer rules.
6. `RUNTIME_TEST` documents are Runtime regression evidence, not Game Design Core evidence.
7. `HISTORICAL` and `DEPRECATED` documents must not override current Canonical files.
8. Project facts come from the current approved Project GDD / locked current decision.
9. Conversation memory must not override GitHub Canonical sources.
10. `UNKNOWN` must remain `UNKNOWN` unless the source supports an inference.

## Studio OS Rule Precedence

```text
Current Canonical Manifest
↓
Current Canonical Document
↓
Historical Trace
↓
Conversation Memory
```

## Project Fact Precedence

```text
Current Approved Project GDD
↓
Locked Current Decision
↓
Older Project Source
↓
Reviewer Inference
```

Do not mix the two precedence chains.

## Runtime Loading

```text
Always:
Manifest
Reviewer Runtime

Lookup:
Universal
Genre Master
Scale

Conditional:
Only routed Genre Baselines

Lookup Only:
Reference Library
Runtime Tests

Never:
Historical / Deprecated
```

## Review Guardrails

- Mechanism first; do not route by genre label alone.
- Product Promise before violation.
- `UNKNOWN ≠ FAIL`.
- `Core 하나 = Finding 하나`로 처리하지 않는다.
- Merge Raw Findings into Root Issues.
- One Root Issue should produce one RF unless fixes/root causes materially differ.
- Keep `Knowledge Confidence`, `Project Evidence Strength`, and `Issue Severity` separate.
- Candidate status does not automatically lower Severity.
- Production Handoff is not a Game Design Core.
- Historical GSC is not an active rule.
- Do not invent Project features.
- Do not invent test results.
- Do not infer human fun/readability from machine structure.
- Do not create detailed Validation Plans unless a separate approved module explicitly requests it.

Reviewer may output:

```text
VALIDATION_REQUIRED
Claim:
...
Suggested Evidence Type:
...
```

and stop there.

## Repository Guardrail

If Manifest and actual Repository files disagree:

1. verify the actual latest approved file;
2. verify its Logical ID;
3. update Manifest path/version metadata;
4. do not silently reinterpret rule content.

Current Runtime:

`REVIEWER_RUNTIME_SPECIFICATION_v1.0.md`
