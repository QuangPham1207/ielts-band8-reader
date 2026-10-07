# IELTS Band 8 Reader

Personal static study site: 25 starter samples (MVP toward 130), modelled on the Spanish course's static-site pattern.

## Structure

- `index.html` — homepage with cards (same pattern as Spanish `index.html`).
- `assets/style.css` — shared stylesheet (phone-first, dark-mode). Spanish inlines CSS per lesson; here one shared file is enough and keeps 130 pages maintainable.
- `samples/<section>/*.html` — one self-contained sample per file (links `../../assets/style.css` relatively — adjust to `../..` depth per folder).
- `template/sample-template.html` — canonical template. Copy it for every new sample.
- `syllabus.md` — coverage map MVP 25 → 130.

## Local preview

Open `index.html` in a browser, or serve statically:

```powershell
npx serve "D:\Projects\IELTS-Reader"
# or
python -m http.server 8000 --directory "D:\Projects\IELTS-Reader"
```

## Publish (GitHub Pages, account QuangPham1207)

Note: local `gh` is logged in as `QuangPham-CX`. For `QuangPham1207` you will need to auth that account or push via the GitHub web UI.

```powershell
Set-Location "D:\Projects\IELTS-Reader"
git init; git add -A; git commit -m "IELTS Band 8 Reader MVP: scaffold + 25 samples"
gh repo create QuangPham1207/ielts-band8-reader --public --source=. --push
# then: repo Settings → Pages → Deploy from branch → main → / (root)
```

Site will be at `https://quangpham1207.github.io/ielts-band8-reader/`.

## Add a sample

1. Copy `template/sample-template.html` to the right folder.
2. Follow `AGENTS.md` (the 7-section page contract).
3. Add a card in `index.html` + a row in `syllabus.md`.
