# Dermalyze

**Skin pattern screening demo — educational tool, not a medical device.**

Dermalyze is a single-file, client-side web app that runs a live ABCDE-style
dermoscopy heuristic (Asymmetry, Border irregularity, Color variance,
Diameter/coverage) directly on image pixels in the browser. No image is ever
uploaded to a server — everything runs locally via HTML5 Canvas.

## ⚠️ Disclaimer

This is **not** a diagnostic tool and has **not** been clinically validated.
It uses a transparent, rules-based heuristic engine, not a trained medical
model. Always consult a licensed dermatologist or physician for any skin
concern — especially anything new, changing, bleeding, or growing.

## Features

- Drag-and-drop or click-to-upload image intake
- Real-time pixel analysis: asymmetry, border irregularity, color variance,
  lesion coverage
- Pattern-match summary against five broad, common skin categories
- Educational condition library
- Fully local — zero network calls, zero data collection

## Getting started

Just open `index.html` in any modern browser. No build step, no dependencies,
no server required.

```bash
git clone https://github.com/<your-username>/dermalyze.git
cd dermalyze
open index.html   # or double-click the file
```

## Extending this to a real clinical tool

The scoring logic lives in the `scoreImage()` function in `index.html`. To
make this production-grade:

1. Replace the heuristic engine with a call to a model trained on a labeled
   clinical dataset (e.g. [HAM10000](https://doi.org/10.1038/sdata.2018.161) /
   [ISIC Archive](https://www.isic-archive.com/)).
2. Serve that model behind an API (or run it client-side via TensorFlow.js).
3. Have a licensed dermatologist validate outputs before anyone relies on them.

## License

MIT © 2026 SHRINIDHI S K
