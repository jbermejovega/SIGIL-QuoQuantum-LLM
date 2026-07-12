# SYNTHGOTHHUB RAG · MCP · n8n Compliance Policy V1

Status: `ACTIVE_MODEL_BOUNDARY_POLICY`  
Canon: `PIORNALEGO_ES_CANON`

## Role

This repository is a typed model boundary and consumer of SYNTHGOTHHUB retrieval and MCP tools. It is not the source of repository truth and may not treat generated text as a verification witness.

## Retrieval contract

Every retrieved context must preserve:

```yaml
required:
  - repository
  - ref
  - path
  - commit_or_blob_sha
  - semantic_type
  - provenance
  - license_or_usage_descriptor
  - validation_status
  - trace_id
```

Conflicting sources remain plural and explicitly marked. The model must not synthesize false consensus.

## MCP tool contract

```yaml
tool_call_required:
  - tool_name_declared
  - input_schema_valid
  - caller_intent_visible
  - side_effect_classified
  - repository_scope_declared
  - trace_event_emitted

mutation_requires:
  - explicit_user_instruction
  - permission_check
  - dedicated_branch
  - visible_diff
  - test_or_validation_witness
  - PR_first
```

## n8n boundary

n8n may orchestrate a model request, retrieval, validation, and tool call, but it may not convert model output into authority without a witness produced by the relevant repository/runtime.

## Claim classes

- `retrieved`: sourced material returned with provenance;
- `inferred`: model inference, explicitly labelled;
- `generated`: proposed content without execution witness;
- `verified`: supported by repository test, build, benchmark, proof, or replay witness.

## Seal

```text
Model output is not repository truth.
Retrieval keeps provenance.
MCP calls remain bounded and visible.
n8n orchestration does not manufacture authority.
Verified claims require external witnesses.
```
