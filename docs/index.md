---
title: Home
nav_order: 1
---

# Interactive Virtual Assistant

## Background
In an event, we want to have a memorable gimmick that can also boost sales. The idea is an interactive customer service agent that people can talk to. It is a 3D NPC that assists with event-related information.

## Goal
Serve as both an informational and recreational feature of an event to gain traction for the event's vibe.

## User Stories
### Event Audience
**General**
- I can see the assistant visually as a human 3D character on a PC monitor/TV.
- I can interact by talking to the virtual assistant using a mic.
- I can interact using a touch screen on the PC monitor/TV.
- I can interact using keyboard and mouse as a fallback option.
- I can ask the virtual assistant about information related to the event.
- I can use English as the language.
- I can use Bahasa Indonesia as the language.

**Functional**
- I can see the text of what the assistant is currently speaking.
- I can skip the current voice.
- I can cancel my question.

**Performance**
- I can interact seamlessly with the AI assistant (the delay is not too long).

### Admin
- I can set up the avatar.
- I can set up the avatar voice (male/female).
- I can set the knowledge base for the LLM (RAG).

## Visual
- The virtual assistant has a 3D avatar.
  - The avatar is one unity top to bottom.
  - It can be either realistic or cartoon-like.
  - It needs lip flaps that are in sync with the voice.
  - The facial expressions need to be set (idle, smile, sad, not pleased) during greetings and responses.
  - It can zoom in or out, with a customizable visible frame (virtual camera).
  - Out of scope: customizable outfit.
- The background can be set depending on the mood.
  - It can be a basic single-color background.
  - It can be set like a Google Meet background with a custom image.

## Sound
- The voice of the avatar needs to be as good as ChatGPT.
  - It can be set as female or male.
  - The voice needs to be in sync with lip flaps.
  - Out of scope: more than one variation per voice type (male/female).

## Database
- The LLM needs a source input as a knowledge base.
  - The event knowledge can be set by the admin/developer.
  - Out of scope: the LLM can access the internet and has knowledge outside the related event.

## UI/UX
- Voice input
  - The main input for the assistant.
  - The mechanism will be similar to ChatGPT.
  - There will be a list of recommended/sample commands.
- Touch input
  - First fallback.
  - A list of recommended/sample commands appears as an options menu to select.
- Mouse and keyboard
  - Second fallback.
  - Uses a textbox.

## User Flow
TODO

## Notes
- Audio streaming lag.
- Network latency.

## Platform
Windows PC (Win64)

## Deployment
Steam (Beta Code)

## Tech Stack
- Unreal Engine
- MetaHuman
- LLM (ChatGPT) for voice
- RAG-style LLM

## Hardware
### As User
**PC**
- Ryzen 5
- RTX 3050
- RAM 16GB

**I/O**
- Wireless Mic
- Touch screen
- Mouse and keyboard

### As Developer
**PC**
- Ryzen 7
- RTX 3060
- RAM 32GB

## References
- Unreal Engine plugin https://youtu.be/G2sn7kWGscw?si=rRlqCSssouD2ZdbN
  - Runtime MetaHuman Lip Sync (AI for NPCs) (+ CC4, Genesis, ARKit, and more) https://www.fab.com/listings/b514294e-e78b-4b8b-ad21-78ce51dc7e8c
  - Runtime Text To Speech (Real-Time, Offline, Streaming TTS, AI) https://www.fab.com/listings/0dab646f-73b4-46d9-bb7e-8e6c12bdd808
  - Runtime Audio Importer https://www.fab.com/listings/66e0d72e-982f-4d9e-aaaf-13a1d22efad1
- Digital assistant of Unreal Engine HMI at CES 2026 AMD booth https://www.facebook.com/share/r/1ARqiC1wAR/
- UI chat bot reference https://www.fab.com/ja/listings/a4394add-18a9-44d8-907a-7e1c98bcf02e
