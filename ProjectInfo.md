Interactive Virtual Assistant

Background
In an event, we want to have certain gimmick that can be remembered by the audience, probably boosting sales as well. If we can have an interactive customer service agent where you can have conversation with. It’s a 3D NPC that can assist you with event related information. 

Goal
To serve as both informational but also recreational feature of an event to gain traction of the event‘s vibe.

User stories
Event audience
General
- I can see the assistant visually as human 3D character in a PC Monitor/TV 
- I can interact by talking to the virtual assistant using mic
- I can interact by using touch screen in the PC monitor/TV
- I can interact by using keyboard and mouse as fallback option
- I can ask virtual assistant about the information related to the event
- I can use English as the language
- I can use Bahasa Indonesia as the language
Functional
- I can see the text of what the assistant is currently speaking of
- I can skip the current voice
- I can cancel my question
Performance
- I can interact seamlessly with the ai assistant (the delay not too long)
Admin
- I can set up the avatar
- I can set up the avatar voice (male/female)
- I can set knowledge base for the LLM (RAG)

Visual
- The virtual assistant has a 3D avatar
	- The avatar is one unity top to bottom
	- It can be either realistic or cartoon-like 
	- It needs lip flaps that in sync with the voice
	- The facial expression need to be set (idle, smile, sad, not pleased) during greetings and responding to question.
	- It can be zoom in our out, the visible frame is customizable (it has virtual camera)
	- out of scope: customizeable outfit 
- The background can be set depends on the mood
	- It can be just basic one color background
	- It can be set just like google meet background with custom image 
Sound
- The voice of avatar need to be as good as chat gpt assistant
	- It can be set up as female or male voice
	- The voice need to be in sync with lip flaps
	- Out of scope: more than one variation per voice type (male/female)
Database
- The LLM need to have a source as an input as the knowledge base
	- The event knowledge can be set by the admin/developer
	- Out of scope: the LLM can access internet and has knowledge outside the related event
UI/UX
- Voice input
	- The main input for the assistant
	- The mechanism will be the same as chat gpt would
	- There will be a list of recommended/sample command
- Touch input
	- As a first fallback
	- The list of the recommended/sample command listed as options menu that the user can select and become an input
- Mouse and keyboard
	- As a second fallback
	- Using textbox

User flow
TODO

Notes
- Audio streaming lag
- Network latency

Platform
Windows PC (Win64)
Deployment: Steam (Beta Code)

Tech stack
Unreal Engine
Meta Human
LLM (chatgpt) for the voice
RAG like LLM

Hardware
As User
PC
- Ryzen 5
- RTX 3050
- RAM 16GB
I/O
- Wireless Mic
- Touch screen
- Mouse and keyboard

As Developer
PC
- Ryzen 7
- RTX 3060
- RAM 32GB

References 
- Unreal engine plugin https://youtu.be/G2sn7kWGscw?si=rRlqCSssouD2ZdbN
	- Runtime MetaHuman Lip Sync (AI for NPCs) (+ CC4, Genesis, ARKit, and more) https://www.fab.com/listings/b514294e-e78b-4b8b-ad21-78ce51dc7e8c
	- Runtime Text To Speech (Real-Time, Offline, Streaming TTS, AI) https://www.fab.com/listings/0dab646f-73b4-46d9-bb7e-8e6c12bdd808
	- Runtime Audio Importer https://www.fab.com/listings/66e0d72e-982f-4d9e-aaaf-13a1d22efad1 
- Digital assistant of unreal engine HMI at CES 2026 AMD booth https://www.facebook.com/share/r/1ARqiC1wAR/
- UI chat bot reference https://www.fab.com/ja/listings/a4394add-18a9-44d8-907a-7e1c98bcf02e
