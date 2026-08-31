# Book pages

Three closed books sit on the desk (the old SketchUp open books are hidden).
Each has a folder here.

Per book:

```
books/bookN/cover.jpg      – shown first, at its own aspect
books/bookN/1.jpg          – ONE spread  (left page + right page in one image)
books/bookN/2.jpg          – next spread
...
```

- `.jpg`, `.jpeg`, `.png`, `.webp`. Plain numbers (`1.jpg`), no zero-padding.
- Count auto-detected — stops at the first missing number.
- Every image is shown full-bleed at its **exact** pixel aspect. The 3D page
  is rebuilt to the image; images are never resized, stretched, or cropped.
- Label reads "cover", then "pages 1–2", "pages 3–4", … (assumes each numbered
  image is a 2-page spread).

`book1` is loaded from `booksfiles/TEST/` — `cover.jpeg` + `1–6.jpeg`
(each 1684×1191, i.e. a two-page spread). `book2` / `book3` are empty until
you add images.

Page images are A5-proportioned (148 × 210, e.g. 842 × 1191 px). The closed
book model is built to that ratio, so a cover fills its top face exactly.

## Desk books / posters

Placed where the four old open books sat (that strip clears when they're
hidden, and the research-paper sheet is hidden too). Each book's short bottom
edge faces the chair.

| folder | opened by            | desk position (world x, z) |
|--------|----------------------|----------------------------|
| book1  | poster 1 (left)      | 0.47, −0.82                |
| book2  | poster 2 (centre)    | 0.47, −1.04                |
| book3  | poster 3 (right)     | 0.47, −1.26                |

Also opens by centring the reticle on the book on the desk and clicking.
Positions, titles, poster→book map, page-flip sound, and framing constants
are all at the top of `../books.js` (`BOOK_SPOTS`, `BOOKS`, `POSTER_MAP`,
`flipSound`, `TOP_FILL` / `READ_FOV` / `CAM_DUR` / `DIM_EXPOSURE`).
