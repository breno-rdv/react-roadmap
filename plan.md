# Implementation Plan

## Summary
Planning artifact generated from the current specification.

## Goal
Turn the approved specification into an implementation sequence with bounded scope.

## Files to Modify
- src/server.ts
- src/commands/router.ts
- src/roles/*
- src/github/pr.ts
- src/llm/github-models.ts

## Steps
- Confirm spec completeness.
- Limit edits to planned files.
- Generate code changes for the approved scope.
- Run validation before handoff.

## Risks
- Missing repository context can lead to incomplete plans.
- Artifact synchronization with GitHub is still placeholder-only.

## Spec Input
spec.md not loaded yet in this scaffold.

## Current Trigger
/plan