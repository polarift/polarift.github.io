# polarift.github.io

Hosted slide decks and files for the Polarift forum. Served by GitHub Pages at
`https://polarift.github.io/`, and embedded in forum posts with an iframe.

## Layout

One top-level folder per forum category, using the category slug:

    se-practice/
    mbse-modeling/
    verification-validation-test/
    standards-process/
    careers-certification/
    resources/              general files (PDFs, templates, downloads)

Each deck is its own folder: `<category>/<kind>-<nn>-<short-title>/`

    se-practice/lecture-01-intro-to-systems-architecture/
      index.html     the viewer (from pdf-to-html)
      slides.pdf     download copy
      meta.json      title, author, category, forum_topic

## Naming rules

- lowercase, hyphens only, no spaces, no version suffixes (git keeps history)
- `lecture-NN-`, `workshop-NN-` or `guide-` prefix, then a short title
- the folder name becomes the URL, so never rename after it is linked in a post

## Adding a deck

1. Convert the PDF with pdf-to-html and copy `index.html` into a new folder.
2. Add `slides.pdf` and `meta.json`.
3. Add an entry to `library.json` (the index page is built from it).
4. Commit and push.

## Embedding in the forum

Add `https://polarift.github.io/` to the Discourse `allowed_iframes` setting, then:

    <iframe src="https://polarift.github.io/se-practice/<deck>/" width="100%" height="560" allowfullscreen loading="lazy"></iframe>

    [Open full screen](https://polarift.github.io/se-practice/<deck>/) | [Download PDF](https://polarift.github.io/se-practice/<deck>/slides.pdf)

## Copyright

Only add material you have the right to redistribute. Keep the original author
and licence in `meta.json`.
