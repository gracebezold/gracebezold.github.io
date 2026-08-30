# <username>.github.io

Personal site. Static HTML, no build step, served by GitHub Pages from `main` / root.

```
.
├── index.html      landing page (about, research, links)
├── cv/
│   └── index.html  CV page — embeds cv.pdf, links to it
├── cv.pdf          the actual CV  <-- YOU ADD THIS
├── .nojekyll       tells Pages to serve files as-is (skip Jekyll)
└── README.md
```


## URLs

| what | url |
|---|---|
| landing page | `https://<username>.github.io/` |
| CV page | `https://<username>.github.io/cv/` |
| raw PDF (put this in application forms) | `https://<username>.github.io/cv.pdf` |

## Updating the CV

```bash
cp /path/to/myresume_v2.pdf cv.pdf
git commit -am "cv: update" && git push
```
