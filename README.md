# Nagrik Sahayak — Government Information Services Bot

A browser-based chatbot that answers common questions about government
services (identity documents, certificates, taxes, licenses, grievances,
and emergency helplines) using a built-in knowledge base — no server or
internet connection required.

## How it works

- `knowledge.js` — the knowledge base: service categories, each with
  entries that list keywords, required documents, process steps, and
  typical processing time.
- `script.js` — matches what the user types against the keywords in the
  knowledge base and renders the best match as a "ticket" response,
  styled like a token you'd get at a real government service counter.
- `index.html` / `style.css` — the page structure and the visual design
  (an "official service window" look: letterhead header, a directory of
  services on the left, and a counter/chat window on the right).

## Running it

No build step or server needed:

1. Open `index.html` directly in any modern web browser, **or**
2. Serve the folder locally, e.g. `python3 -m http.server`, then visit
   `http://localhost:8000`.

## Extending it

To add a new service, open `knowledge.js` and add a new entry object
(with `title`, `keywords`, `documents`, `steps`, `processingTime`) inside
the relevant category, or add a whole new category to
`SERVICE_DIRECTORY`.

## Note

This is a student demonstration project. The information in the
knowledge base is illustrative and general — always verify actual
procedures, fees, and required documents with the relevant official
government office or website.
