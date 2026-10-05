# mulle-sde.github.io

Landing page for [mulle-sde](https://github.com/mulle-sde/mulle-sde) — the
Unix IDE, written in bash.

- **Live site:** https://mulle-sde.github.io/
- **Stack:** plain HTML + CSS. No JavaScript, no build step, no dependencies.
- **Style:** retro terminal / CRT (amber phosphor, scanlines). Deliberately
  different from the dark gradient theme used by
  [mulle-core.github.io](https://mulle-core.github.io/).

## Files

| File         | Purpose                                              |
|--------------|------------------------------------------------------|
| `index.html` | Single-page landing (semantic HTML + JSON-LD)        |
| `style.css`  | All styling, CRT overlays and animations             |
| `logo.png`   | Mulle kybernetiK seal — hero crest, favicon, og:image|
| `README.md`  | This file                                            |

`rec1/` and `rec2/` are older asciinema recording scratch directories and are
not referenced by the page.

## Preview locally

Just open `index.html` in a browser. It is plain HTML + CSS with no build step,
and the relative links (`style.css`, `logo.png`) resolve from the file system.

## Deploy

For an organization GitHub Pages site, this repository must be named
`mulle-sde.github.io` under the `mulle-sde` org, and Pages is served from the
`master` branch root by default — no workflow needed.

```sh
git add index.html style.css logo.png README.md .nojekyll
git commit -m "Replace Jekyll page with static landing page"
git push
```

## Keeping content fresh

- The page describes **functionality**, not the individual commands or the
  underlying tool repositories. If the workflow (Edit-Reflect-Craft), the
  supported platforms or the install instructions change in the
  [mulle-sde README](https://github.com/mulle-sde/mulle-sde), update
  `index.html` to match.
- The install one-liner and the developer-environment link come from the main
  README. Keep them in sync.
- The GitHub org profile renders
  [`mulle-sde/.github`](https://github.com/mulle-sde/.github)
  `profile/README.md`. Content that applies to both should stay consistent.
