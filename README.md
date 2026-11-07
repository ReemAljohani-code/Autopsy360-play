# Autopsy360 — Play

**[Play The Virtual Autopsy Table](https://reemaljohani-code.github.io/Autopsy360-play/)**

Developed by **Reem Aljohani, MD**.

The existing interactive 3D simulator includes organ-block separation, cardiac dissection, and brain cutting. Use a modern browser with WebGL enabled. Progress is saved in that browser; no account or installation is needed.

## This repository

This public repository contains the compiled website in `website.zip`, its SHA-256 checksum, and the GitHub Pages deployment workflow. The full editable project, Blender scenes, authoring scripts, and complete source export remain in the separate private `Autopsy360` repository.

The ZIP contains `index.html`, JavaScript/CSS, the team page, runtime models and fonts, and the existing asset attribution/license files. Browser-delivered files are public. Existing third-party asset licenses remain applicable; this repository does not relicense them.

## Deployment

GitHub Pages is configured to use **GitHub Actions**. On a push to `main`, `.github/workflows/pages.yml` checks the archive checksum, extracts the static website, and deploys it using GitHub's official Pages actions. It can also be run manually from the Actions tab. No personal token or repository secret is required.

The website is packaged for the `/Autopsy360-play/` path. The simulator geometry, textures/materials, interface, and lesson logic are retained; deployment only rebases local asset and navigation URLs. The original export baseline is `278da87550481f809241ca9583a5cf62b6a8f267`.

To update, build the private application, package it for this same path, and replace **both** `website.zip` and `website.zip.sha256` in one commit. Keep private source and authoring files out of this repository. The local maintainer packaging helper is `github-pages-tools/package-pages.py` beside the exported project.

## Local preview of this published build

Extract `website.zip` into a directory named `Autopsy360-play`. From its parent directory, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/Autopsy360-play/`. The ZIP is a compiled website; use the private source export for development.
