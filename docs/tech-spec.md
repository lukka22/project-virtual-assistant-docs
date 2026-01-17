---
title: Tech Spec
nav_order: 3
---

# Tech Spec

## Overview
An Unreal Engine application with a MetaHuman-based 3D avatar, voice input, TTS output, and an LLM+RAG knowledge base for event Q&A.

## Architecture
- Client app (Unreal Engine)
- Voice input pipeline
- LLM + RAG service
- TTS output pipeline

## Components
### 3D Avatar
- MetaHuman asset with lip-sync support
- Facial expression presets (idle, smile, sad, not pleased)
- Camera framing controls

### Voice Input
- Microphone capture
- STT service integration
- Text display for live transcription

### LLM + RAG
- Event knowledge base indexed for retrieval
- Prompting layer for response formatting
- Language support: English, Bahasa Indonesia

### Voice Output
- TTS voice (male/female)
- Lip-sync alignment
- Playback controls (skip/cancel)

## Data Sources
- Admin-managed event knowledge base

## Performance Targets
- End-to-end response latency within acceptable range
- Real-time lip-sync alignment

## Deployment
- Windows PC (Win64)
- Distribution via Steam (Beta Code)

## Open Issues
- Finalize latency targets
- Confirm STT/TTS provider
- Define admin content update process
