# christadelphian-search-index

Static search index and theme data for [christadelphianclasses.com](https://www.christadelphianclasses.com),
generated from transcripts of the Christadelphian Bible classes hosted at christadelphianbibletalks.com.
Rebuilt automatically when new classes are transcribed and tagged. No manual edits here.

- `pagefind/` — [Pagefind](https://pagefind.app) index. One page per class; every ~60 s of speech is a
  section whose anchor `#t<seconds>` gives the time the phrase was spoken.
- `data/tags.json` — theme tag counts and the classes under each tag (`"<study_id>/<class_id>"`).
- `data/studies/<study_id>.json` — per class: tags, two-sentence summary, key passages, duration.
- `data/vocabulary.json` — the controlled tag vocabulary.
- `data/meta.json` — build time and counts.
- `index.html` — a bare demo of the index (GitHub Pages).

Transcripts were produced with whisper.cpp (large-v3-turbo); tags with Qwen2.5-14B-Instruct. Both
are machine output and contain errors.
