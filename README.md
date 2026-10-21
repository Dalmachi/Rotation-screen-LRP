# La Roche-Posay device preview

A design mock of a La Roche-Posay product page (Mela B3 Dark Spot Serum) shown on a laptop, an iPad (horizontal) and an iPhone. The three devices turn on a ring and take turns coming to the front. Use the left and right arrows, the keyboard arrow keys, or swipe to move them yourself. Click a smaller device to bring it forward.

## Run it

It is plain HTML, CSS and JavaScript with no build step. Browsers block some features when a page opens from a file, so serve the folder:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Publish with GitHub Pages

1. Push this folder to a GitHub repository.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then save.
4. The site appears at `https://<your-username>.github.io/<repository-name>/`.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The device viewer: the laptop, iPad and iPhone frames, the rotating ring, and the arrows. |
| `site.html` | The product page itself. Open it directly to see it as a normal responsive page with its own width bar. The viewer loads it in each device with `?embed=1`. |
| `product.mp4` | The product video with the two molecule bubbles. |
| `poster.jpg` | The video's first frame, shown while the video loads. |
| `logo.png` | The La Roche-Posay logo used in the header. |

## Change things

- **Device sizes and spacing:** the `D` table and the `render()` function at the bottom of `index.html`. Every device shares one scale, and the iPhone is scaled by `m: .79` so it stays smaller than the iPad and laptop, as in real life.
- **Rotation speed:** `dur` in `animate()` is the turn time in milliseconds. The `4200` in `schedule()` is how long each device stays in front.
- **Page content:** edit `site.html`. The layout rules for each device are the `html.tablet` and `html.phone` blocks in its stylesheet.

## Brand note

La Roche-Posay, its logo and its product images belong to their owners. This project is a layout demo. Check that you have the right to publish the logo, the product video and the product name before you make the repository public.
