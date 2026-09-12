# GeMAIHc 2027 &mdash; Short Course Slides

Slides for a two-session short course on generative and multimodal AI for healthcare, presented by David Buckeridge (McGill University & Mila &ndash; Quebec AI Institute) at [GeMAIHc 2027](https://gemaihc.irdta.eu/2027/speakers/).

**Live site:** https://david-buckeridge.github.io/gemaihc-2027-slides/

## Sessions

- **Session 1 &mdash; Generative AI for Public and Population Health** (`session-1/`): LLM foundations, prompt engineering, RAG, and a BEACON outbreak-surveillance case study.
- **Session 2 &mdash; Multimodal AI for Public and Population Health**: in progress, not yet published here.

Each session is a self-contained HTML/CSS/JS deck. See the README inside `session-1/` for viewing instructions, structure, and open items.

## Viewing locally

The deck fetches its own section files at runtime, so it needs to be served over HTTP, not opened directly as a `file://` path.

```
cd session-1
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

## License and attribution

Session 1's visual design and some section content are adapted, with permission, from the [AI4PH workshop deck](https://echore.github.io/workshop-slides/) created by Melissa Ouellet and Yachen Li (July 2026), used under its MIT license.

See the `LICENSE` file in `session-1/`.
