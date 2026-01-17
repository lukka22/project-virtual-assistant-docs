---
title: PRD
nav_order: 2
---

# PRD

## Problem Statement
Create a memorable event gimmick that drives engagement and supports sales by providing a conversational, in-venue virtual assistant.

## Goals
- Provide accurate event information.
- Improve attendee engagement and recall.
- Offer a pleasant, low-latency conversational experience.

## Non-Goals
- Internet browsing or knowledge outside the event domain.
- Highly customized outfits or multiple voice variants per gender.

## Personas
- Event audience (primary user)
- Admin/operator (setup and content owner)

## User Stories
- See and interact with a 3D assistant on a display.
- Speak with the assistant using a microphone.
- Use touch input or keyboard/mouse as fallback.
- Ask about event information in English or Bahasa Indonesia.

## Functional Requirements
- Live speech recognition with text display.
- Voice playback with skip/cancel controls.
- Knowledge base configured by admin (RAG).

## Non-Functional Requirements
- Low latency interactions.
- Stable audio streaming.
- Reliable local performance on target hardware.

## Success Metrics
- Conversation latency within acceptable range.
- Session engagement rate.
- Positive attendee feedback.

## Risks
- Audio streaming lag.
- Network latency.

## Open Questions
- Target max response time (ms).
- Content update workflow for the knowledge base.
- Event-specific branding and visuals.
