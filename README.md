# <username>.github.io

Personal site. Static HTML, no build step, served by GitHub Pages from `main` / root.

```
.
├── index.html      landing page (about, research, links)
├── cv/
│   └── index.html  CV page — embeds cv.pdf, links to it
├── reading/
│   └── index.html  reading log page — renders reading-log.json
├── reading-log.json  books (currently + finished)  <-- YOU EDIT THIS
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
| reading log | `https://<username>.github.io/reading/` |

## Updating the reading log

Edit `reading-log.json` only — both the landing page ("What I'm reading")
and `/reading/` read it at load time. Put newest finished books first.

Previewing locally needs a server (browsers block `fetch` on `file://`):

```bash
python -m http.server 8000   # then open http://localhost:8000
```

## Updating the CV

```bash
cp /path/to/myresume_v2.pdf cv.pdf
git commit -am "cv: update" && git push
```
