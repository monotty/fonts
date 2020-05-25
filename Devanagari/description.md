# Devanagari script

Font name:  `Monotty`  
File name:  `monotty-dev2.ttf`

### Unicode blocks

Block                     | Range
--------------------------|----------------
Devanagari                | U+0900 – U+097F
Vedic Extensions          | U+1CD0 – U+1CFA
Common Indic Number Forms | U+A830 – U+A839
Devanagari Extended       | U+A8E0 – U+A8FD

### OpenType features

Glyph substitution table \[GSUB]

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

Glyph positioning table \[GPOS]

- Advance width adjustment `<dist>`
- Above base marks `<abvm>`
- Below base marks `<blwm>`

### Related documentation
- [Devanari script description](https://hindilanguage.info/devanagari/)
- [Shaping behavior of Devanagari](https://github.com/itfoundry/devanagari-shaping)
- [Developing OpenType Fonts for Devanagari Script](https://docs.microsoft.com/en-us/typography/script-development/devanagari)
- [Indic script shaping in OpenType](https://github.com/n8willis/opentype-shaping-documents/blob/master/opentype-shaping-indic-general.md)
  - [Devanagari shaping in OpenType](https://github.com/n8willis/opentype-shaping-documents/blob/master/opentype-shaping-indic-general.md)
