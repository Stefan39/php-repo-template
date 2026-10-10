# Demo GIF workflow

Goal: 10-20 seconds that show the **benefit**, not the installation. Target size under 5 MB.

## Terminal demos: vhs

[vhs](https://github.com/charmbracelet/vhs) records a scripted terminal session, so the GIF is reproducible.

```bash
brew install vhs
vhs demo.tape        # writes assets/demo.gif
```

Keep `demo.tape` in the repo (`docs/demo.tape`). Use a fixed terminal size, a short typing speed and no real secrets or customer data.

## UI demos: screen recording and gifski

```bash
brew install gifski ffmpeg
ffmpeg -i recording.mov -vf "fps=15,scale=960:-1" frames/%04d.png
gifski --fps 15 --width 960 --quality 80 -o assets/demo.gif frames/*.png
```

## Checks before commit

- File size under 5 MB (lower `--width`, `--fps` or `--quality` if needed).
- No real customer data, tokens or personal data visible. Use a demo account or redacted data.
- Alt text in the README is meaningful, the first frame already shows the point.
