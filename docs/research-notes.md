# tmux for EvoCUA: Session Semantics Adapter

## Purpose

This document records the research framing behind the static GitHub Pages site. The project studies how tmux can be adapted for EvoCUA as a durable terminal substrate for agentic work.

## Research Question

How should a terminal multiplexer expose stable, recoverable state to an evolving CUA agent without hiding the temporal structure of command execution?

## Working Thesis

The adapter treats each tmux pane as a semi-structured experimental instrument: commands, output spans, focus transitions, and recovery checkpoints become first-class observations for EvoCUA.

## Design Claims

- Pane identity is preserved across command retries and window changes.
- Observation packets separate stable shell state from transient rendering artifacts.
- Recovery hooks favor explicit checkpoints over silent command reissue.

## Evaluation Lens

- State continuity under pane switching
- Action grounding after failed commands
- Trace completeness for post-hoc review


## Threats to Validity

- Terminal state can be over-instrumented, causing an adapter to measure artifacts of the harness rather than real agent behavior.
- A final successful artifact may hide poor recovery behavior, repeated command attempts, or fragile focus management.
- Agent-specific adapters can become difficult to compare unless trace schemas remain explicit and documented.

## Hero Image Source

The GitHub Pages hero image uses the shared tmux CUA screenshot, copied into `docs/assets/hero.png` at its original 1484x1060 PNG resolution.
