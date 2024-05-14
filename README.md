# Monotty Fonts

### Monospaced Fonts for Terminals

![image](.resources/github-devanagari.png)

__Monotty__ is shortening for for two words: `Monospaced` and `TTY` (Teletype, Terminal).

These fonts are mainly intended for experiments with displaying CTL scripts in terminal emulators supporting the character slicing. (See [Unicode Variation Selectors as Size Modifiers](https://gitlab.freedesktop.org/terminal-wg/specifications/-/issues/23)). This font has not been finalized to the level of practical use, and so far it contains some inaccuracies that are not critical for the experiments.

### Supported Writing Systems

- [ ] [Brahmic scripts](https://en.wikipedia.org/wiki/Brahmic_scripts)
  - [x] Devanagari `<dev2>`
    - [x] Nepali `<NEP >`
    - [x] Marathi `<MAR >`
  - [ ] Bengali `<bng2>`
  - [ ] Gujarati `<gjr2>`

## Specification

- Font type: outline (automatic generation from strokes, stroke-based representation, expresses each glyph as a set of stems)
- Weight: configurable stroke width
- Em size: 2000
- Сharacter width: monospaced, exactly 1/2em
- Ascent: 1400
- Descent: 600

## Building from Source

Binary `.ttf` files can only be generated from `.sfd` files using [FontForge Monotty Edition](https://github.com/monotty/fontforge).

Steps for `.ttf` generation: [BUILD.md](/BUILD.md)

### Downloads

 - Devanagari `<dev2>`: [`monotty-dev2.ttf`](https://github.com/monotty/fonts/releases/latest/download/monotty-dev2.ttf)
 - Bengali `<bng2>`: N/A
 - Gujarati `<gjr2>`: N/A
