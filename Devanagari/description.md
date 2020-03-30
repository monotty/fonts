# Devanagari Script

An abugida, or alphasyllabary, is a segmental writing system in which consonant–vowel sequences are written as a unit; each unit is based on a consonant letter, and vowel notation is secondary.

Indian languages syllable boundaries should be based on tailored grapheme cluster boundaries to conform Indic orthographic syllable definition.

For expample, a Devanagari consonant cluster is a grapheme in the Devanagari writing system, it can consist of up to five consonants and any dependent combining characters; however, for almost all fonts, the final glyphs are never wider than four (2em) and higher than two cells.  
See [Ligature Examples](http://www.sanskritweb.net/cakram/saMyoga-pattra.pdf).  
See [Devanagari conjuncts](https://en.wikipedia.org/wiki/Devanagari_conjuncts).

Assume that terminals consider such conjuncts as tailored grapheme clusters using the following [rules](https://www.unicode.org/L2/L2016/16161-indic-text-seg.pdf),

```
V[m] | {CH}C[v][m] | CH 

Rule 1 : V[m]
Rule 2 : {CH}C[v][m]
Rule 3 : CH (This rule is applicable only at the end of the word)

V is independent vowel
m is modifier(Anusvara/Visarga/Chandrabindu)
C is a consonant which may or may not include a single nukta
v is any dependent vowel or vowel sign (mātrā)
H is Halant (Virama)
| is a rule separator
[ ] - The enclosed items is optional under this bracket
{} - The enclosed item/items occurs zero or repeated multiple times
```

and output them as whole characters, and never splits them. [See the Devanagari script and its use for the Hindi language](https://r12a.github.io/scripts/devanagari/#boundaries).

In this case, by using the sliced characters mode ([new SGR attribute](https://gitlab.freedesktop.org/terminal-wg/specifications/issues/23)), applications (and terminals itself) can correctly output the Devanagari script (and other CTL scripts).  
Applications can take the width for each cluster in a predefined ligature size chart.

Note: To avoid problems with ligatures that cross a linebreak, conjuncts and any dependent combining characters should never be split (font should contain the glyphs to create a conjunct).

There are several problems:
- it is needed a monospaced (? grid-based, grid fit) font with fixed-pitch ligatures of width up to 4 cells (despite it's proportional by nature), or do stretching each glyph horizontally to the nearest cell border
- grapheme cluster boundary tailoring agreement
- clusters width agreement (also the terminal itself can set the width of the clusters if the sliced characters mode is not enabled, and the application does not need to take care of this)
 
__text sample (Hindi)__:  
अनुच्छेद १.  
 सभी मनुष्यों को गौरव और अधिकारों के मामले में जन्मजात स्वतन्त्रता और समानता प्राप्त है ।  
 उन्हें बुद्धि और अन्तरात्मा की देन प्राप्त है और परस्पर उन्हें भाईचारे के भाव से बर्ताव करना चाहिए ।  
  
__colors__: proportional font is marked in yellow, fixed-pitch in green, wide clusters are highlighted in tone  

![image](https://dice.netxs.online/cloud/monotty/github-devanagari-gui.png)
