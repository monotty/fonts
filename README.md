# [It is not ready for release yet]

# Monospaced Fonts for CTL Scripts (e.g. Devanagari)

![image](https://dice.netxs.online/cloud/monotty/github-devanagari.png)

__Monotty__ is shortening for for two words: `Monospaced` and `TTY` (Teletype, Terminal).

These fonts are mainly intended for displaying CTL scripts in terminal emulators supporting the character slicing. (See [the new SGR attribute](https://gitlab.freedesktop.org/terminal-wg/specifications/-/issues/23)).

It requires so much horizontal space that it is not very suitable for a “user interface font”.

## Building the font (e.g. generate the `.ttf` file) from source

The font binaries are not directly part of this repository, as it only contains source files; however, the binaries are directly built from the `.sfd` files.

This requires the following program:
- [FontForge Open Source Font Editor](https://fontforge.org/en-US/) ([download page](https://fontforge.org/en-US/downloads/))

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

## Monotty Mono Devanagari Regular

Script description: https://hindilanguage.info/devanagari/  
Basic glyph example: http://devanaguide.huertatipografica.com/  
Font name:  `Monotty Mono Devanagari Regular`  
Base font:  `Noto Mono Regular`, `Noto Sans Devanagari Regular`

### Unicode blocks
Block                     | Range    
--------------------------|--------------
Devanagari                | U+0900 – U+097F
Vedic Extensions          | U+1CD0 – U+1CFA
Common Indic Number Forms | U+A830 – U+A839
Devanagari Extended       | U+A8E0 – U+A8FD

### Shaping Behavior
[...link](https://github.com/itfoundry/devanagari-shaping)
[...link](https://docs.microsoft.com/en-us/typography/script-development/devanagari)

### Ligatures and Conjuncts
- ...

...
