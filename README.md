# OwO-Dusk Config Editor

A single-file, browser-based gui editor for [owo-dusk's](https://github.com/owo-dusk/owo-dusk) `settings.json` and `global_settings.json` — no build step, no backend, nothing leaves your browser.

## Usage

1. Open `index.html` (locally, or via GitHub Pages).
2. Pick **Settings** or **Global Settings**, then either:
   - **Upload** your own file, or
   - **Use template**, if `settings.json` / `global_settings.json` are sitting in the same folder as `index.html`.
3. Edit through the form, or switch to **Raw JSON** for direct text editing.
4. **Copy JSON** or **Download JSON** when you're done.

Use the search bar to jump straight to a setting (e.g. `cooldown`, `channel`, `gamble`).

## Repo layout

```
index.html            the editor itself
settings.json          (optional) template for the Settings card
global_settings.json   (optional) template for the Global Settings card
```

The template files are optional — without them you can still just upload your files manually.

## Notes

- Made using claude, expect bugs and errors. PR's are welcomed.
- Everything runs client-side. Nothing is uploaded anywhere — files never leave your browser.
- `pray` and `curse` can't both be enabled at once (they share the same cooldown window); enabling one turns the other off automatically.
- The `channelSwitcher` section is flagged as advanced — only touch it if you know what you're doing, and it also needs to be enabled in `danger.toml`.
