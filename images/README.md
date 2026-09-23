# Images folder

Add your photos here with these exact filenames so the site picks them up automatically:

- `profile.jpeg` — hero portrait (used at the top of index.html)
- `gallery-1.jpeg` through `gallery-10.jpeg` — the gallery photos

How it works:
- The first 4 (`gallery-1.jpeg`–`gallery-4.jpeg`) always show as the fixed
  photos on the homepage.
- The last 2 homepage slots pick 2 different photos at random from
  everything after the first 4 in the list (`gallery-5.jpeg` onward),
  reshuffled on every page load.
- `gallery.html` is a dedicated page that shows ALL of them in one grid,
  with a click-to-enlarge viewer (arrow keys or on-screen arrows to move
  between photos, Esc or the X to close).

To add more photos (beyond 10, or just more into the random rotation):
1. Drop the new image file into this /images folder (e.g. `gallery-11.jpeg`).
2. Open `gallery-data.js` in the root of the site and add its path as a new
   line in the GALLERY_IMAGES list, e.g. `"images/gallery-11.jpeg",`.
That's it — index.html and gallery.html both read from that one file, so you
never have to edit the HTML itself to add, remove, or reorder photos. Just
keep your favorite 4 at the very top of the list if you want them to be the
homepage's fixed photos.

Recommended: keep each photo under ~500KB (resize/compress before uploading)
so the site stays fast on Netlify/GitHub's free tiers.
