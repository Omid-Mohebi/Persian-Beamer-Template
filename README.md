# Persian Beamer Template (XeLaTeX)

A small, clean Beamer template for Persian (right-to-left) presentations using **XeLaTeX** and `xepersian`.
It provides a modern color palette, Persian title fonts, and example frames (theorem, example, proof, figures).

---

## How does it look like?

<p align="center">
  <img src="https://github.com/user-attachments/assets/697cd0f4-7e94-4944-850b-23bb6fa26935" alt="image 1" width="48%" />
  <img src="https://github.com/user-attachments/assets/700452a2-93a9-4395-b235-52a951cbf458" alt="image 2" width="48%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/17420a8c-48b4-48e6-86df-22afacd1df22" alt="image 3" width="48%" />
  <img src="https://github.com/user-attachments/assets/492ede36-eb5e-4978-bd41-e663fd5106df" alt="image 4" width="48%" />
</p>




---

## Features

* Persian support via `xepersian`.
* Uses custom Persian fonts:

  * `Yas.ttf` (main body)
  * `IranNastaliq.ttf` (calligraphic/large text, used with `\nas`)
  * `BTitr.ttf` (title font `\titr`)
* Clean `Madrid` Beamer theme with a custom color palette (navy, teal, green, orange).
* Example frames that demonstrate theorem/example/proof/corollary environments.
* Image inclusion example (`plot-python.pdf`) — assets folder set to `./assets/`.

---

## Files / Project layout

```
project-root/
├─ assets/
│  └─ plot-python.pdf
├─ Yas.ttf
├─ IranNastaliq.ttf
├─ BTitr.ttf
└─ main.tex         <-- .tex file
```

* Put the font files either in the project root (as above) or install them system-wide.
* Place images and figures inside `assets/` as shown or update `\graphicspath`.

---

## Required software

* A TeX distribution with XeLaTeX support:

  * TeX Live (recommended) — Linux/macOS/Windows
  * MiKTeX (Windows)
* LaTeX packages used (normally included in a current TeX Live / MiKTeX):

  * `beamer`, `xepersian`, `graphicx`, `xcolor`, and standard font handling available to XeLaTeX.
* Fonts mentioned above (`Yas.ttf`, `IranNastaliq.ttf`, `BTitr.ttf`) — either copy them into the project directory or install them to the OS fonts folder.

---

## Compilation instructions

### Overleaf

1. Upload `.tex` file and the font files (`Yas.ttf`, `IranNastaliq.ttf`, `BTitr.ttf`) and `assets/` to the Overleaf project.
2. In Overleaf menu: **Menu → Compiler** → choose **XeLaTeX**.
3. Click Recompile.

### Local 

* Use **XeLaTeX** (not pdfLaTeX) because `xepersian` and `.ttf` fonts require an engine with native font access.
* Run twice (or use `latexmk`) to ensure references, TOC and overlays are correct.


