# CV source

`cv.tex` builds the PDF the site serves at `/cv/`.

Moved here from `~/Dropbox/Job Applications/` so the CV lives alongside the
site that publishes it. `res.cls` is the document class it needs; nothing else
in the old folder used it. The other packages (`helvet`, `hyperref`, `lipsum`)
are stock TeX Live.

```sh
make publish      # build and copy to ../pdfs/cv.pdf
```

This folder starts with an underscore, so Jekyll excludes it from the built
site — the `.tex` source is never published, only the PDF that `make publish`
copies into `pdfs/`.
