# Crazy Bob v4.1 🤪 — Omni-Agent (Crash-Fixed)

Private local AI on your phone. WebLLM + WebGPU.

## Crash fixes in this build
- **No auto-load on startup** — you tap **Load** when ready (prevents Safari memory kill)
- **Embedder starts only after** the chat model is loaded and settled
- **Previous engine unloaded** before loading a new model
- **Safe default model**: SmolLM2 360M
- **q4f32 option** for devices that lack float16 shaders
- Clearer error messages (OOM / WebGPU / network / f16)
- Idle embedding only runs in tiny batches when the LLM is already running

## Recommended load order on iPhone
1. Open the app
2. Leave **SmolLM2 360M** selected (or Qwen 0.5B)
3. Tap **Load** and wait until status says Ready
4. Chat normally
5. Only try Llama 3.2 1B after that works
6. Avoid 3B on most phones

## If it still fails
- Close other Safari tabs / apps
- Use **Llama 3.2 1B q4f32** if you see an f16 error
- Reload the page and try SmolLM2 again
- First download needs network; later loads use cache

## Features (unchanged)
Chain-of-Thought, Team mode, Self-Healing tools, Long-term User Profile,
Document/PDF offline RAG, Semantic vectors (when embedder loads), Token budgeter,
Web Worker background tasks, Voice, Export/Import memory.

## Files
- `index.html`
- `bob-worker.js` (keep next to index.html)
- icons + `manifest.json`

Host the folder over HTTPS (or localhost), open in Safari, Add to Home Screen.
