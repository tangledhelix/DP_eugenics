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

### Illustrations ###

- [ ] f001: small pair of decorations next to title (?)
- [ ] f006: entire page
- [ ] p072: entire page

### Things to revisit ###

The illustrations on f006 and p072 are too complex to render to text. For that
version, use the main caption. For HTML/Epub, use the image and the main
caption.

There are fairly complex tables on a few pages.

- [ ] f006: HTML/Epub: use illo. Txt? Asked in forum for PM advice.
- [ ] p005
- [ ] p009
- [ ] p014
- [ ] p019
- [ ] p072: HTML/Epub: use illo. Txt? This seems too complex to attempt?

PM messaged privately and suggested illos for f006, p072 are sufficient, including text caption of the main caption for the table.

Some tables use upward-opening braces, will need to determine how to render.  (p005, p014)

- [ ] p093: output from rounds: `<i>se- cura</i>,`
  - Posted in "No dumb questions" forum
  - Consensus is to leave the space
  - Use a nbsp to keep wrapping sane

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


[1]: https://archive.org/details/b21727922
[2]: https://en.wikipedia.org/wiki/Francis_Galton
[3]: https://www.pgdp.net/phpBB3/viewtopic.php?p=1334069#p1334069
[4]: https://en.wikipedia.org/wiki/Interpunct
[5]: https://www.pgdp.net/phpBB3/viewtopic.php?p=1334108#p1334108
[6]: https://www.compart.com/en/unicode/U+00B7
