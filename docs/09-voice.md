# Lesson 09: Local voice: Assist, Wyoming, Linux Voice Assistant

_Keep Whisper/Piper. Move satellites off archived wyoming-satellite._

Fully local voice is real in 2026. Understand the pipeline, validate one layer at a time, and use the modern satellite path.

## The voice pipeline

Microphone → wake word → speech-to-text → conversation/intent/LLM → text-to-speech → speaker.

**What's this mean?** Hear → notice your name → turn speech into text → decide what you meant → talk back out the speaker. Five stations on an assembly line.

**More detail:** Official Home Assistant Assist + fully local voice assistant guide.

## Wyoming services still matter

Wyoming Protocol is still the bridge for Whisper, Piper, Speech-to-Phrase, openWakeWord — including running heavy STT/TTS on another LAN machine/GPU.

**What's this mean?** Wyoming is the radio cable between Home Assistant and the big listening/talking computers. That cable is not dead.

**More detail:** Great layout: satellites on the edge; Whisper/Piper on a powerful box; HA in the middle.

## wyoming-satellite is legacy — use Linux Voice Assistant

rhasspy/wyoming-satellite was archived 2026-01-27. Replacement: OHF Linux Voice Assistant using the ESPHome protocol (timers, media player, stop wake listening, continued conversation). Install via HA OS App, Pi image, Docker, or systemd. It appears in HA through ESPHome. STT/TTS can still be Wyoming.

**What's this mean?** Old Pi satellite software retired. New satellite software talks the ESPHome way Home Assistant prefers now — while Whisper and Piper can stay on Wyoming.

**More detail:** <div class="cr-flow">OLD: Pi → wyoming-satellite → HA<br><span class="hi">NEW: Pi → Linux Voice Assistant → ESPHome protocol → HA</span><br>Whisper / Piper may still be Wyoming services</div>Study: OHF Linux Voice Assistant on GitHub.

## Wake words: validate layers apart

Start with a known wake word like “ok nabu.” Do not debug custom wake word + mic + Whisper + intent + Piper + speaker all at once.

**What's this mean?** Fix one station on the assembly line before you rebuild all five. Otherwise you never know which station jammed.

**More detail:** HA enable wake word + customize wake word guides. Everything Smart Home’s Voice Preview Edition videos are a latency/behavior reference. Piper+Whisper walkthrough videos help once HA Assist already works with push-to-talk.

## Sources

- [HA Assist](https://www.home-assistant.io/voice_control/)
- [Wyoming Protocol](https://www.home-assistant.io/integrations/wyoming/)
- [Linux Voice Assistant](https://github.com/OHF-Voice/linux-voice-assistant)
