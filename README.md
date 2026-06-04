# Script Emotion Workbench

A static prototype for visualizing emotional intent, director assumptions, and shot discussion points in talking-head scripts.

This project is not an emotion scoring tool. It does not try to say a script is "96% happy" or reduce performance to metrics. Instead, it turns a pasted script into a discussion surface:

- What emotional intent seems to be carrying the piece?
- Which parts feel like the main line, side branches, or discussion points?
- Where does the emotional curve rise, sink, or settle?
- How might A-roll, B-roll, self-shot scenes, and locations support the director's intent?
- What is still uncertain and worth discussing before spending time shooting?

The current version is a zero-dependency static frontend. Analysis is rule-based in the browser, so it can run locally without a backend.

## Why This Exists

Short-form creators and small production teams often struggle to decide whether a script is worth shooting. The hard part is not only writing the words. It is making the director's intent discussable:

- why this script is worth the effort
- what the creator is really trying to say
- which emotion should be visible on screen
- where the script is still vague
- what kind of shot plan would make the idea feel acceptable and believable

This workbench tries to reduce the amount of absolute interpretation held by one director. It gives creators a shared visual language for discussing the script before production.

## Current Features

- Paste a Chinese talking-head script and split it into editable segments.
- Generate an emotion curve based on script progression and emotional intent.
- Surface a "director intent hypothesis" instead of a final judgment.
- Show discussion questions and uncertainty points.
- Classify segments as main line, transition, side branch, or discussion point.
- Suggest A-roll, B-roll, self-shot scenes, locations, breathing points, and subtitle focus.
- Export the analysis as Markdown.
- Run as a plain static web page.

## What It Is Not

- It is not a production-ready AI analysis system yet.
- It is not a universal script quality judge.
- It does not claim that every good script needs a hook, turn, or fixed structure.
- It does not replace a director's taste or a creator's personal voice.

## Local Usage

```bash
python3 -m http.server 4173
```

Then open:

```text
http://127.0.0.1:4173
```

If you run the command from this folder, the static app will load directly.

## Project Files

- `index.html` - static app shell
- `styles.css` - responsive UI and visualization styling
- `app.js` - local analysis rules and rendering logic
- `preview.png` - preview image for the current prototype
- `OSS_APPLICATION_NOTE.md` - short note for open-source grant/application contexts

## Roadmap

- Replace local heuristics with an optional model-backed JSON analysis API.
- Add saved projects and version comparison.
- Add PDF export for director review.
- Add timeline markers for editing tools.
- Add multi-person comments for writer/director/editor discussion.
- Add bilingual UI and docs.
- Collect real scripts and compare how different creators interpret the same text.

## License

MIT