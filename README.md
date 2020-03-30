# Monospaced Fonts for CTL Scripts (Devanagari, Arabic, etc.)

__Monotty__ is shortening for for two words: Monospaced and TTY (Teletype, Terminal).

## Building the font (e.g. generate the `.ttf` file) from source

The font binaries are not directly part of this repository, as it only contains source files; however, the binaries are directly built from the `.sfd` files.

This requires the following program:  
[FontForge Open Source Font Editor](https://fontforge.org/en-US/) ([download page](https://fontforge.org/en-US/downloads/))

## Initial Draft Specification

### Standardization Goals
- grapheme cluster boundary tailoring agreement
- monospaced font with fixed-pitch ligatures
- predefined ligature size chart

### Writing Systems
- [Brahmic scripts](https://en.wikipedia.org/wiki/Brahmic_scripts)
  - Devanagari	(Deva)
  - Gujarati	(Gujr)
  - Tamil	(Taml)
  - ...
- [Arabic](https://en.wikipedia.org/wiki/Arabic_script)
- ...

## Monotty Mono Devanagari Regular

Script description: https://hindilanguage.info/devanagari/  
Basic glyph example: http://devanaguide.huertatipografica.com/  
Font name:  `Monotty Mono Devanagari Regular`  
Base font:  `Noto Mono Regular`, `Noto Sans Devanagari Regular`

### Terminal output example

![image](https://dice.netxs.online/cloud/monotty/github-devanagari.png)

...

## Monotty Mono Arabic Regular

...
