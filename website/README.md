# Spooky Quiz website

Mobile-first static website for GitHub Pages. The embedded Tally form handles questions, private answers, image uploads and validation. No API key, guest answers or uploaded guest photos belong in this repository.

## The one submission form

- Form ID: `KpzeqK`
- Guest link: https://tally.so/r/KpzeqK
- Editor: https://tally.so/forms/KpzeqK/edit
- Workspace: `My workspace`

Guest flow: one question per submission, with guest name, question text, an optional single upload (10 MB maximum) and a complete answer. After submitting, offer a link to contribute another question. Ask guests to contribute at least two and no more than five overall. These are instructions rather than enforced per-person limits. No emails or accounts are required from guests.

The live form uses the same one-question flow.

## Preview

Run `python3 -m http.server 8765 --directory website` from the parent workspace, then open http://localhost:8765.

## GitHub Pages

Publish only this directory's contents as the site artifact. Do not publish the parent workspace, which includes presentation drafts and local project metadata. The workflow at `.github/workflows/pages.yml` in the parent workspace uploads `website/` only.

## Close submissions

Close the form in Tally, or update form `KpzeqK` with `isClosed: true`. Closing the actual form prevents new submissions through both the website and the direct link. A cosmetic closed message on the website alone would not do that.

## Prepare the presentation

After closing, retrieve the completed submissions and their uploaded images through Tally. Preserve submission/question IDs and contributor names. Review duplicates, accuracy, order and visual spoilers before editing the existing Canva deck recorded in the parent workspace's `canva-quiz.json`. Never create another presentation for the same quiz.

## Notes

The website uses one compressed copy of the host-provided background. The original images are preserved. Tally's own form text is intentionally on a white background for legibility on phones. A direct form link remains available if the embed is blocked or JavaScript fails.
