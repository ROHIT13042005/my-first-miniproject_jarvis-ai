# JARVIS Performance Optimization

Applied safe optimizations focused on CPU/heat without removing features:

- HUD animation: 60 FPS -> ~30 FPS.
- Dashboard/system metrics UI refresh: 2s -> 4s.
- Live camera preview: ~30 FPS -> ~15 FPS.
- System alert monitor: 10s -> 30s.
- Proactive mode evaluation: 60s -> 180s.
- Camera warm-up frames: 10 -> 5.
- Python `__pycache__` folders are excluded from the optimized ZIP.

The microphone/Gemini audio path and feature behavior are intentionally left intact. Wake-word detection remains local and only runs when wake-word mode is enabled.

If CPU is still high after these changes, the next optimization should be an optional low-power mode that pauses the HUD animation and disables proactive/background monitoring while JARVIS is idle.
