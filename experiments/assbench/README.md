# AssBench prompt, run through HAI on one 7900 XTX

The prompt is LTT Labs' AssBench prompt from their "Jarvis at home" article, word for word (public at assbench.com),
given to my assistant with no hint about which model to use. It picked Qwen3.8 Flash-Next, a 125B mixture-of-experts
model, at Q2 on the single Radeon RX 7900 XTX in my gaming PC, with the rest of the model held in system RAM.

- Started 2026-11-04 09:29, stopped by its 4-hour budget at 13:32. 141 tool calls.
- The coding sandbox had no browser, so it installed Playwright and Chromium itself, then ran three full loops of
  render → screenshot from twelve angles → measure → fix.

## Files

| file | what it is |
|---|---|
| `buttocks-1214.html` | the version from 12:14, the one its 12:23 screenshots were taken of. **The best version.** Unmodified. |
| `render-1214.png` | that file opened in a headless browser, default camera (my render, not the model's) |
| `buttocks-final-1330.html` | the final file as delivered at 13:30. Its last edit changed the swimwear into a thin shell it could not re-check (its screenshot tool timed out), and the shorts regressed; it says so in its summary |
| `hai-selfcheck-back-1327.png` | its own last self-check screenshot (of the 13:1x build, before the final edit) |
| `hai-selfcheck-report-1327.txt` | its own measurement report for that build: triangle counts, fps, width/depth at eleven heights, leg gap |
| `hai-answer.md` | its final summary, including where it ran out of time |

Open either HTML file from disk in a browser; it loads three.js 0.168 from jsdelivr and nothing else. Drag to orbit.

## Caveats

- This is the 125B, not the 27B used in the article. The 27B run on the same card is next and will be added here.
- One run, one seed. Treat it as a demonstration, not a benchmark score.
- The model's own date in a docstring is wrong in one place; the geometry it cites is real.
