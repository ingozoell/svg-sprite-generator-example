# SVG Sprite Generator — working example

Five editable SVG icons, one SVG sprite and a ready-to-use HTML demo. No JavaScript, dependencies or build step.

**[Create your own SVG sprite](https://css-img-sprite-generator.ingozoell.de/en/)** — up to 5 images free, no signup required.

## Run the demo

Download this repository as a ZIP, extract it and open `index.html`. Keep all supplied files in the same folder. If your browser restricts local files, serve the folder with any static web server, for example `python3 -m http.server 8000`, and open `http://localhost:8000/`.

## Use an icon

```html
<img src="icons-sprite.svg#home" width="64" height="64" alt="Home">
```

Replace `home` with `heart`, `star`, `leaf` or `moon`. Each image references the same SVG resource with a different fragment identifier. The sprite contains CSS that makes the selected icon visible. This is an image-fragment sprite, not a `<symbol>`/`<use>` sprite sheet.

The explicit width and height reserve space before loading. For decorative icons alongside an equivalent text label, use `alt=""`.

## Included files

- `index.html` — working demonstration with all five icons.
- `icons-sprite.svg` — ready-to-use combined sprite.
- `home.svg`, `heart.svg`, `star.svg`, `leaf.svg`, `moon.svg` — five original, editable source icons.
- `demo.css` — optional demo layout styles; icon selection happens inside the sprite.
- `LICENSE` — MIT license for this example's code and icons.

## Generate your own version

1. Open the [online SVG Sprite Generator](https://css-img-sprite-generator.ingozoell.de/en/).
2. Upload `home.svg`, `heart.svg`, `star.svg`, `leaf.svg` and `moon.svg`, or your own artwork.
3. Choose your embedding settings and download the export.
4. Copy its image and CSS folders into your project and use the supplied HTML.

This small example demonstrates the generator's `sprite.svg#name` embedding method. Your downloaded export may contain additional CSS and files depending on the settings you select.

## Size, color and Retina displays

The supplied icons use vector paths and share a 64 × 64 viewBox. You can display them at 24, 32 or 64 pixels without creating raster 2× or 3× versions. For example, change both HTML dimensions to `32`.

Their stroke color is defined inside the SVG. A page's CSS `color` does not recolor SVGs loaded through `<img>`; edit the source SVGs before generating your sprite, or edit the stroke values in the example sprite.

## Animation limits

This example uses static SVGs. The generator also supports eligible automatically running SVG animations. Animated GIF and AVIF files are exported separately because animation embedded inside an SVG sprite is not reliably supported across browsers. AVIF playback additionally depends on the browser's AVIF image-sequence support.

## Publish a demo with GitHub Pages

After uploading the project to a public repository, open **Settings → Pages**, choose **Deploy from a branch**, and select your default branch and **/(root)**. GitHub will show the published demo address when deployment completes. Add that address to the repository's About section.

## License

MIT — see [LICENSE](LICENSE). Applies to this example's code and icons, not to the generator's application code or to third-party uploads.
