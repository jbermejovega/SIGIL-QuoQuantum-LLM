# SYNTHGOTHHUB RAG · MCP · PYDANTIKA · QUAZRIS8 Compliance Policy V2

Status: `ACTIVE_MODEL_BOUNDARY_POLICY`  
Supersedes: `SYNTHGOTHHUB_RAG_MCP_N8N_COMPLIANCE_V1`  
Canon: `PIORNALEGO_ES_CANON`

## Role

This repository consumes provenance-bearing RAG sections and bounded MCP tools through PYDANTIKA models and QUAZRIS8 gates. Generated model output is never repository truth or certification evidence by itself.

## Canonical request path

```text
retrieved sections
  -> provenance check
  -> PYDANTIKA request model
  -> QUAZRIS8 Q1..Q8 gates
  -> MCP tool request or typed obstruction
  -> trace
  -> external witness verification
```

## PYDANTIKA model requirements

Every request and result must declare schema version, claim class, repository scope, side-effect class, provenance, trace ID, validation status, and typed error envelope.

## QUAZRIS8 claim gates

```yaml
gates:
  Q1_PROBE: source and request exist
  Q2_DECLARE: user intent and claim class declared
  Q3_TYPE: PYDANTIKA validation passes
  Q4_BOUND: tool, repository and side effects bounded
  Q5_EXECUTE: only approved call runs
  Q6_TRACE: result and errors appended
  Q7_VERIFY: claim compared with external witness
  Q8_CLOSE: human-reviewed certificate candidate only
```

## Legacy n8n boundary

n8n-originated payloads are accepted only after conversion into PYDANTIKA models. Workflow-node names, success flags, and execution order have no authority until QUAZRIS8 validation and external witness verification.

## Claim classes

- `retrieved`: source-bound material;
- `inferred`: explicit model inference;
- `generated`: proposal without runtime witness;
- `validated`: PYDANTIKA schema-valid;
- `verified`: external repository, proof, build, test, benchmark, or replay witness exists.

## Seal

```text
RAG keeps provenance.
MCP bounds tools.
PYDANTIKA validates requests and results.
QUAZRIS8 gates action and authority.
n8n payloads are legacy inputs only.
Verified claims require external witnesses.
```
