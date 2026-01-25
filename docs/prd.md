---
title: PRD
nav_order: 2
---

# Product Requirements Document (PRD)

## Product Name
**Interactive Event AI Assistant**

---

## 1. Background / Problem Statement
In events, organizers often want a memorable gimmick that stands out and leaves a lasting impression on the audience, while also potentially boosting engagement and sales. Human staff and static displays do not always scale well or provide a consistently engaging experience.

This product introduces an **interactive 3D AI-powered virtual assistant** (a 3D NPC) that audiences can converse with in real time. The assistant provides event-related information while also acting as a recreational and atmospheric element that enhances the overall event vibe.

---

## 2. Goals & Objectives
### Primary Goals
- Create a memorable and engaging event gimmick
- Serve as both an informational and recreational feature
- Increase audience interaction and booth dwell time
- Support multilingual audiences (EN / ID)
- Enable reusable, white-label deployment across multiple events

### Success Metrics
- % of event visitors interacting with the assistant
- Average interaction duration per user
- Booth dwell time increase compared to baseline

### Non-Goals / Out of Scope
- Fully autonomous customer support replacement
- Deep internet-wide knowledge access
- Complex outfit or avatar customization in early phases

---

## 3. Product Positioning & Ownership
- **Product Type:** Innovation project, reusable white-label event product
- **Ownership:** Personal project
- **Intended Usage:** On-site event booths, expos, conferences, brand activations

---

## 4. Target Users
### Event Audience
General event visitors interacting with the assistant on-site via shared displays or kiosks.

### Admin / Editor
Event organizers or operators configuring the assistant via config files or simple in-engine UI.

---

## 5. User Stories

### Event Audience – General
- I can see the assistant visually as a human 3D character on a PC monitor or TV
- I can interact with the assistant by speaking through a microphone
- I can interact using a touch screen on the PC monitor or TV
- I can interact using keyboard and mouse as a fallback option
- I can ask questions using a list of predefined/default questions
- I can use English as the language
- I can use Bahasa Indonesia as the language
- I can see text subtitles of what the assistant is currently saying
- I can skip the current voice response
- I can cancel my question
- I can see QR code related to the event information (if any)

### Event Audience – Performance
- I can interact with the assistant with acceptable latency for live events

### Admin / Editor
- I can define default questions as conversation starters
- I can update content live during the event
- I can switch avatar and voice configuration mid-event
- I can switch avatar's cloth customization (simple one in early phases)
- I can configure upsell or promotional messaging
- I can enable QR-based lead capture
- I can view basic usage analytics (counts, interaction duration)

---

## 5. Core Features & Elements

### Visual
- 3D virtual assistant avatar
  - Full-body unity-style avatar
  - Realistic style
  - Lip-sync (lip flaps) synchronized with voice output
  - Facial expressions (idle, smile, sad, displeased) during greetings and responses
  - Configurable virtual camera (zoom in/out, framing)
- Customizable background
  - Solid color background
  - Custom image background (similar to virtual meeting backgrounds)

### Sound
- High-quality AI-generated voice comparable to modern AI assistants
- Male or female voice options
- Voice output synchronized with lip movement

### Knowledge / Database
- LLM uses an event-specific knowledge base provided by admin/developer
- Knowledge limited strictly to event-related content

### Input Methods
- **Voice input (primary)**
  - Real-time voice interaction
  - Sample/recommended commands provided
- **Touch input (first fallback)**
  - Selectable options menu with predefined questions
- **Mouse & keyboard (second fallback)**
  - Text input via textbox

---

## 6. User Flow (High-Level)
1. User approaches booth / display
2. Assistant greets user (idle animation)
3. User selects or asks a question (voice / touch / text)
4. Assistant processes input (online or offline mode)
5. Assistant responds with voice, subtitles, and animation
6. Optional: QR code displayed for further action
7. User ends or cancels interaction

---

## 7. Performance, Risks & Constraints

### Performance
- Voice interaction latency must feel natural for live events
- Clear visual feedback while processing requests

### Risks & Constraints
- **Data Privacy:** Voice interaction terms must be covered via event T&C and legal notes
- **Cost Control:** LLM usage must respect a configurable per-event cost ceiling
- **Network Dependency:** Online mode preferred but there is fallback option (offline mode).

### Offline / Degraded Mode
- Configurable local-only mode (restart may be required)
- Limited to admin-defined question list
- Scripted Q&A responses
- Local text-to-speech

---

## 8. Platform & Deployment
### Supported Platforms
- Windows PC (Win64)

### Deployment
- Steam (Beta Code distribution)

---

## 9. Hardware Requirements

### Event Audience (User)
- PC with Ryzen 5 equivalent CPU
- RTX 3050 or equivalent GPU
- 16 GB RAM
- Wireless microphone
- Touch screen display
- Mouse & keyboard

### Developer
- PC with Ryzen 7 equivalent CPU
- RTX 3060 or equivalent GPU
- 32 GB RAM

---

## 10. Technical Specification (High-Level)

### Tech Stack
- Unreal Engine
- MetaHuman
- LLM (ChatGPT) for conversational logic and voice output
- Marvelous Designer

### Modes of Operation
- **Online Mode:** Full AI interaction with event-specific knowledge
- **Offline Mode:** Scripted Q&A with local TTS

---

## 11. Roadmap

```roadmap
Phase 1 (MVP)
- Core 3D avatar interaction
- Voice + subtitle response
- Event-scoped knowledge
- Basic offline fallback (scripted Q&A)
- Basic analytics counters

Phase 2
- Live admin content update
- Avatar & voice switching at runtime
- QR-based lead capture
- Cost monitoring per event

Phase 3
- Advanced analytics & dashboards
- Runtime offline/online switching
- Expanded avatar library
- Web-based admin dashboard
```

---

## 12. Naming

### Codename
- **Blue**

### Generic Product Name Options
- Interactive Event AI Assistant
- Event Virtual Concierge
- Event AI Guide
- Virtual Event Companion

### Marketing Name Options
- Blue Concierge
- Blue Guide
- Blue Presence
- Aura by Blue
- Echo by Blue

---

## 13. Avatar Custom Clothing System (Marvelous Designer Integration)

### Objective
Enable **event owners (customers)** to customize the virtual assistant’s clothing so it visually matches the event theme, brand identity, or sponsor requirements, while maintaining high visual quality and animation compatibility with MetaHuman.

---

### Scope
This feature introduces a **custom cloth pipeline** using **Marvelous Designer** to author realistic garments that can be integrated into **MetaHuman avatars** and simulated (or baked) inside Unreal Engine.

---

### Design Workflow (High-Level)

1. **Clothing Design (Event Owner / Designer)**
   - Event owner provides clothing requirements (theme, colors, branding)
   - Clothing is designed in **Marvelous Designer** using real-world garment patterns
   - Output formats:
     - Garment mesh (OBJ / FBX)
     - UVs and material maps (Base Color, Normal, Roughness)

2. **MetaHuman Compatibility Preparation (Developer)**
   - Garment fitted to MetaHuman body proportions
   - Skinning / weight transfer aligned with MetaHuman skeleton
   - Validation against common MetaHuman poses and facial animations

3. **Simulation Strategy**
   - **Phase 1 (MVP):**
     - Cloth simulation baked into animation (no runtime cloth sim)
     - Stable, performance-friendly for event hardware
   - **Phase 2 (Advanced):**
     - Unreal Engine Chaos Cloth simulation enabled
     - Limited dynamic cloth movement (idle, gesture-based)

4. **Integration in Unreal Engine**
   - Garment imported as part of MetaHuman blueprint
   - Clothing selectable via config or simple in-engine UI
   - Outfit tied to specific event configuration

---

### Admin / Event Owner Experience
- Event owners can:
  - Choose from a predefined clothing set
  - Provide their own custom-designed outfit
- Configuration options:
  - Outfit selection per event
  - Color/material overrides (if supported)
- No real-time cloth editing during the event

---

### Constraints & Considerations
- **Performance:**
  - Runtime cloth simulation may impact FPS on booth hardware
- **Stability:**
  - Cloth clipping with extreme animations must be avoided
- **Production Cost:**
  - Custom clothing increases content production time
- **Fallback:**
  - Default outfit always available if custom cloth fails validation

---

### Out of Scope (Initial)
- Real-time outfit authoring during events
- End-user (audience) clothing customization
- Physics-heavy cloth interactions (wind, collision-heavy scenes)

---

### Roadmap Alignment
```roadmap
Phase 1
- Static custom outfits authored via Marvelous Designer
- Baked cloth animation
- Per-event outfit selection

Phase 2
- Limited Chaos Cloth simulation
- Improved material customization

Phase 3
- Outfit presets library
- Faster turnaround pipeline for event owners
```

---

## 14. Future Ideas
- Emotion-aware responses
- Multi-user interaction awareness
- Camera-based audience detection

---

## 14. Kill Criteria
- Low interaction rate across multiple events
- High operational cost with low engagement
- Poor audience reception or trust issues

---

## 15. References & Inspirations
- Unreal Engine runtime MetaHuman & TTS plugins
- Unreal Engine AI NPC tutorials
- CES-style digital assistant demos
- UI chatbot interaction references


