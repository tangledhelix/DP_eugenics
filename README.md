## Essays in eugenics. - 63a325387c26a ##

This is a [Distributed Proofreaders](http://www.pgdp.net/) post-processing project.

"Essays in eugenics." by Galton, Francis

- [DP project page](http://www.pgdp.net/c/project.php?id=projectID63a325387c26a)
- [Forum thread](https://www.pgdp.net/phpBB3/viewtopic.php?t=78411)
- [Trello board](https://trello.com/b/8qxEv4eh/dp-essays-in-eugenics)
- [Good words](good_words.txt)
- [Bad words](bad_words.txt)

Page references (e.g. `001`) refer to the scan numbers, not the original book's page numbers.

### Project manager notes ###

A few tables. Please keep column alignment characters (`=`). They will be
replaced in formatting. Alignment dots `. . . .` should be removed. Use
`[**brace]` for the horizontal curly bracket.

Images from [TIA][1].

Francis Galton at [wikipedia][2].

### Forum notes ###

Nothing of note (last checked 19 Feb 2024).

### General notes ###

PPgen complaints that can be ignored:

```
**warning: both <b> and "=" found in text. markup conflict?
```

This is normal because the text contains `=` in 3 or so lines:

```
    Position of the filial centre of (1) = 1·44, of (2) = 2·89. When
                     both parents are T it = 1·58.
“Halizah” (= taking off, untying) in the _Jewish Cyclopædia_. Jewish
```

A bunch of long line warnings in the text build, due to the wide tables.

```
**warning: 2 images apparently not used:
**warning:   h1_decorator_left.png
**warning:   h1_decorator_right.png
```

These are used on the title page, just not in a way that ppgen recognizes.

### Illustrations ###

- [x] cover -- `i_cover.jpg`
- [x] f001: small pair of decorations next to title
- [x] f006: entire page
- [x] p072: entire page

### Things to revisit ###

#### Complex illos ####

The illustrations on f006 and p072 are too complex to render to text. For that
version, use the main caption. For HTML/Epub, use the image and the main
caption.

#### Complex tables ####

There are fairly complex tables on a few pages.

- [x] f006: HTML/Epub: use illo. Txt? Asked in forum for PM advice.
- [x] p005
- [x] p009
- [x] p014
- [x] p019
- [x] p072: HTML/Epub: use illo. Txt? This seems too complex to attempt?

PM messaged privately and suggested illos for f006, p072 are sufficient, including text caption of the main caption for the table.

#### Horizontal brackets in tables ####

Some tables use upward-opening braces, will need to determine how to render.  (p005, p014)

Possible solution: Unicode. There are some characters to look into.
  - TOP CURLY BRACKET U+23DE: ⏞
  - BOTTOM CURLY BRACKET U+23DF: ⏟
  - PRESENTATION FORM FOR VERTICAL LEFT CURLY BRACKET U+FE37: ︷
  - PRESENTATION FORM FOR VERTICAL RIGHT CURLY BRACKET U+FE38: ︸

The first two are from the Misc. Technical block, but the second two are from the CJK Compatibility Forms block. So the first two are more generic and probably preferable.

Posted in the forums on this question.

#### Hyphenated word with embedded space ####

- [x] p093: output from rounds: `<i>se- cura</i>,`
  - Posted in "No dumb questions" forum
  - Consensus is to leave the space
  - Use a nbsp to keep wrapping from breaking at that space, to preserve its intentionality.

#### Equals sign? ####

On p048, halfway down on the right margin, is what looks like an unexpectedly wide equals sign. No promising matches on unicodeplus.com or shapecatcher.com. Posted on forum in case anyone knows different; if not, then maybe it's simply an equals sign.

[U+FF1D][7] (＝) was pointed out in the forums, but in rendering tests it doesn't seem to look much different, at least in the font ppgen uses. I went with a regular = sign.

### Proofer's notes ###

Some numbers appear separated by a character similar to a mid-dot. There are proofer notes on p092 about this. I [posted in the forum][3] about it and one response suggested to use normal period (`.`) unless the entire book used this mid-dot as a decimal point. Looking further I located more, on p019. Nowhere in the text does a "normal" period appear in a number, so far as I see.

**As printed** the dots on the page are not even mid-dots, they are positioned at the top edge of the numbers. Will need to review all the dots in Unicode to see if this character exists; I'm not familiar with it.

These are the only "higher dot" characters I was able to find.

- U+02D9 Dot Above (˙)
- U+0307 Combining Dot Above (e.g. to compose ȧ)
- U+18DF Canadian Syllabics Final Raised Dot (ᣟ)

First two are diacritical marks. The third seems to relate to aboriginal languages in Canada. Just use decimal points.

**Resolution:** use [middle-dot][6] (U+00B7, `&centerdot;`) character, per this [reference][4] supplied in the [forums][5]:

> In British typography, the space dot was once used as the formal decimal point. Its use was advocated by laws and can still be found in some UK-based academic journals such as The Lancet.

### Joined hyphenated words ###

- `semi-*criminals`: appears hyphenated elsewhere in book
- `inter-*marriage`: appears unhyphenated elsewhere in book
- `black-*board`: appears unhyphenated elsewhere in book

### Spellcheck ###

### Transcriber's notes ###

### Smooth Reading ###

### Ebook review notes ###

Summary:
- ADE: Rendered txt/png ok. Suffered at narrow widths.
- iBooks: Rendered txt/svg ok, but had trouble with PNGs!
- Kindle: Rendered txt/png ok. Much trouble with SVG.
- Calibre: sucks at tables.
- Kobo: sucks at tables.
- GPB: sucks at tables.

Verdict: PNG I guess? I'm surprised iBooks had so much trouble with PNGs.
The wiki FAQs also seem to suggest SVG is a special case that should only
be resorted to if using LaTeX. PNG it is.

Rendering of the "drawn with unicode" brackets:
- ADE: renders decently, but not great due to narrow screen width.
- iBooks:
    - Mac: renders acceptably.
    - iPhone: renders acceptably but text brackets not the best.
- Kindle:
    - Previewer: Actually rendered quite well (with zoom-in).
    - iPhone: renders fine but you need to zoom in
    - Android: renders fine on zoom.
    - Paperwhite: renders ok. need to zoom.
- Calibre:
    - Mac: rendering is not great. It flows wrongly, if the table is wider than
      the display it bleeds over the text of the following page, it's just not
      good at all. It renders the brackets acceptably. If you widen the
      viewport then it lays it out okay but might be across a page break which
      is not good. No way to control that as far as I can tell. No zoom like
      iBooks.
- Kobo:
    - iPhone: chars render ok; table bleeds to next page badly.
- Google Play Books:
    - Chars render OK but table layout terrible

Rendering of the PNG brackets:
- ADE: actually rendered quite well. But needed either small font, or wider
  screen, or really both.
- iBooks:
    - Mac: inconsistent - in one table, some brackets appear, not others. In
      another table, no brackets appear!
    - iPhone: doesn't render the L/R brackets. or the top/bottom.
- Kindle:
    - Previewer: Somewhat decent. The scaling isn't that great.
    - iPhone: renders well, need to zoom in
    - Paperwhite: renders fine, even in dark mode (if zoomed)
    - Android: renders with white bg even in dark mode, but they work
- Calibre:
    - Mac: see above regarding layout. Renders the PNGs ok.
- Kobo:
    - iPhone: chars render ok; table layout really bad.
- Google Play Books:
    - PNGs render ok but table layout SUCKS

Rendering of the SVG brackets:
- ADE: not great. They rendered at unexpected sizes. And worse, at inconsistent
  sizes! The same SVG repeated in different columns behaved differently! Same
  CSS. At least, when at narrow width; at wider width it actually lays out
  perfectly. So something about the layout engine is messing up the sizing of
  various cells I guess. Affects only the left-right braces. The top/bottom
  braces don't seem to be affected. At narrow widths, the braces shrink
  unexpectedly. Doesn't happen with PNGs.
- iBooks:
    - Mac: seems to display properly, at least when zooming into the table.
    - iPhone: renders in page at wrong sizes. But on zoom in it renders fine!
- Kindle:
    - Previewer: Ignores some of the SVGs; displays others. But the ones it
      displays are scaled incorrectly. I don't see any consistency to when it
      decides it will or won't render an SVG...
    - iPhone: very inconsistent rendering; some missing; some sized wrong.
      cell layouts are really wack as well.
    - Android: inconsistent.
    - Paperwhite: Renders fine. Odd considering all the other Kindles suck at SVG.
- Calibre:
    - Mac: see above about layout. Renders the SVGs ok.
- Kobo:
    - iPhone: chars render sort of ok; not scaled like I'd want, but really
      bad at the table rendering, and it bleeds to next page
- Google Play Books:
    - chars render ok (wrong scale) but table layout TERRIBLY BAD


[1]: https://archive.org/details/b21727922
[2]: https://en.wikipedia.org/wiki/Francis_Galton
[3]: https://www.pgdp.net/phpBB3/viewtopic.php?p=1334069#p1334069
[4]: https://en.wikipedia.org/wiki/Interpunct
[5]: https://www.pgdp.net/phpBB3/viewtopic.php?p=1334108#p1334108
[6]: https://www.compart.com/en/unicode/U+00B7
[7]: https://www.fileformat.info/info/unicode/char/ff1d/index.htm
