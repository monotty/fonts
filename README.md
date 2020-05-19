# [It is not ready for release yet]
# The Monotty Font Project
## OpenType monospace fonts for CTL scripts

![image](https://dice.netxs.online/cloud/monotty/github-devanagari.png)

__Monotty__ is shortening for for two words: `Monospaced` and `TTY` (Teletype, Terminal).

These fonts are mainly intended for displaying CTL scripts in terminal emulators supporting the character slicing. (See [the new SGR attribute](https://gitlab.freedesktop.org/terminal-wg/specifications/-/issues/23)).

It requires so much horizontal space that it is not very suitable for a “user interface font”.

## Building the font (e.g. generate the `.ttf` file) from source

The font binaries are not directly part of this repository, as it only contains source files; however, the binaries are directly built from the `.sfd` files.

This requires the [FontForge Monotty Edition](https://github.com/monotty/fontforge).

You can also download the last generated file
 - [`monotty-dev2.ttf`](https://dice.netxs.online/cloud/monotty/monotty-dev2.ttf)

### Building stages 
- Use the source `.sfd`
>![image](https://dice.netxs.online/cloud/monotty/build/step1-source.png)

- Build all glyphs, or only selected glyphs, specifying the desired brush shape 
>![image](https://dice.netxs.online/cloud/monotty/build/step2-menu-build.png) + ![image](https://dice.netxs.online/cloud/monotty/build/build-brush.png)

- Checking the results
>![image](https://dice.netxs.online/cloud/monotty/build/step2-build.png)

- Generate `.ttf` (File -> Generate Fonts..., Generate)
>![image](https://dice.netxs.online/cloud/monotty/build/step3-generate.png)

## Specification
- Font type: outline (automatic generation from strokes, stroke-based representation, expresses each glyph as a set of stems)
- Weight: configurable stroke width
- Em size: 2000
- Сharacter width: monospaced, exactly 1/2em
- Ascent: 1300
- Descent: 700

### Writing Systems
- [ ] [Brahmic scripts](https://en.wikipedia.org/wiki/Brahmic_scripts)
  - [x] Devanagari	`<dev2>`
    - [x] Nepali `<NEP >`
    - [x] Marathi `<MAR >`
  - [ ] Bengali	`<bng2>`
  - [ ] Gujarati	`<gjr2>`

## Monotty Devanagari

Devanari script description: https://hindilanguage.info/devanagari/  
Font name:  `Monotty`  

### Unicode blocks
Block                     | Range    
--------------------------|--------------
Devanagari                | U+0900 – U+097F
Vedic Extensions          | U+1CD0 – U+1CFA
Common Indic Number Forms | U+A830 – U+A839
Devanagari Extended       | U+A8E0 – U+A8FD

### OpenType Features
#### Glyph Substitution Table \[GSUB]

- Localized forms
  - Language-specific forms `<locl>`
- Basic Shaping forms
  - Nuqta forms of consonants `<nukt>`
  - Akhand ligatures `<akhn>`
  - Above-base form of 'Ra' `<rphf>`
  - Rakaar ligatures `<rkrf>`
  - Below-base forms `<blwf>`
  - Half forms `<half>`
  - Conjunct-vattu forms `<vatu>`
  - Conjunct forms `<cjct>`
- Presentation forms
  - Pre-base consonant conjuncts `<pres>`
  - Above-base marks `<abvs>`
  - Below-base consonant conjuncts and marks `<blws>`
  - Post-base substitutions `<psts>`
  - Halant forms `<haln>`
  
#### Glyph Positioning Table \[GPOS]

- Advance width adjustment `<dist>`
- Above base marks `<abvm>`
- Below base marks `<blwm>`

### Related documentation
- [FontForge Tutorial](https://fontforge.org/docs/tutorial.html)
- [Shaping behavior of Devanagari](https://github.com/itfoundry/devanagari-shaping)
- [Developing OpenType Fonts for Devanagari Script](https://docs.microsoft.com/en-us/typography/script-development/devanagari)
- [Indic script shaping in OpenType](https://github.com/n8willis/opentype-shaping-documents/blob/master/opentype-shaping-indic-general.md)
  - [Devanagari shaping in OpenType](https://github.com/n8willis/opentype-shaping-documents/blob/master/opentype-shaping-indic-general.md)
