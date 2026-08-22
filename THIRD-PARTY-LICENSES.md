# Third-party licenses

Every page on this site is built with `embed-resources`, so it is one self-contained file: the stylesheets, the scripts and the typefaces are not fetched from anywhere, they are inlined into the page itself. That is deliberate --- a deck opens in a lecture hall with no wifi --- and it means each page *redistributes* the software and fonts below rather than merely linking to them. Several of those licences require their notice to travel with the copy. This file is that notice.

It is generated material's companion, not a claim of ownership: nothing listed here belongs to the course. The course's own licence is in [LICENSE.md](LICENSE.md).

## Fonts

Three families are embedded as base64 faces inside the pages' stylesheets, in the weights the site actually uses. All three are under the [SIL Open Font License, Version 1.1](https://openfontlicense.org/), which permits this and asks that the copyright notice and licence be retained wherever the font is redistributed.

**Source Sans 3** --- the course website: the landing page and the class outline. Fifteen faces, weights 300, 400, 600 and 700 plus italic 400, in the latin, latin-ext and greek subsets.

> Copyright 2010-2020 Adobe (http://www.adobe.com/), with Reserved Font Name 'Source'.
> All Rights Reserved. Source is a trademark of Adobe in the United States and/or other countries.
>
> This Font Software is licensed under the SIL Open Font License, Version 1.1.

**Nunito** --- the slide decks, in both the presentation and the reading page. Ten faces, weights 400, 500, 600 and 700 plus italic 400, in the latin and latin-ext subsets.

> Copyright 2014 The Nunito Project Authors (https://github.com/googlefonts/nunito)
>
> This Font Software is licensed under the SIL Open Font License, Version 1.1.

**Source Sans Pro** --- four faces, carried into each presentation by reveal.js's own default theme rather than chosen by this course. The decks are set in Nunito and do not use it, but it is inlined with the rest of the theme and so is redistributed here all the same.

> Copyright 2010, 2012 Adobe Systems Incorporated (http://www.adobe.com/), with Reserved Font Name 'Source'.
> All Rights Reserved. Source is a trademark of Adobe Systems Incorporated in the United States and/or other countries.
>
> This Font Software is licensed under the SIL Open Font License, Version 1.1.

The full licence text is at <https://openfontlicense.org/open-font-license-official-text/>. Note the one restriction that matters in practice: none of these fonts may be sold on its own, and none may be redistributed under a name containing a Reserved Font Name. Shipping them inside a web page, as here, is expressly permitted.

## Software

**reveal.js 5.1.0** --- the slide decks. MIT License, Copyright (c) 2011-2024 Hakim El Hattab, https://hakim.se, and reveal.js contributors. <https://github.com/hakimel/reveal.js>

**Bootstrap 5.3.1** --- the landing page, the class outline, the projects and the lecture notebooks, through Quarto's themes. MIT License, Copyright (c) 2011-2024 The Bootstrap Authors. <https://github.com/twbs/bootstrap>

**Quarto** --- the site is rendered by Quarto, which inlines several small components of its own into each page, among them AnchorJS (MIT), Tippy.js and Popper (MIT), and clipboard.js (MIT). Quarto itself is MIT-licensed. <https://github.com/quarto-dev/quarto-cli>

Each of these is MIT, which permits redistribution in source and binary form provided the copyright notice and permission notice are included --- which is what this file does. The full text of the MIT License is at <https://opensource.org/license/mit>.

**MathJax is not redistributed here, and that is worth stating rather than leaving out.** Reveal's bundled math plugin would fetch MathJax (Apache License 2.0, <https://github.com/mathjax/MathJax>) from a CDN at view time if a deck carried mathematical notation; none currently does, and no page on this site contains a copy. The projects and the lecture notebooks do not use it at all --- their mathematics is rendered to MathML when the page is built, so it needs no script and no network.

## Material quoted inside the course

The slide decks reproduce figures and citation headers from published papers --- Barnhart et al. in *Current Biology*, Guido et al. in *Nature*, Sousa et al. in *Cancer Research* --- and quote remarks made by other researchers. These belong to their owners and appear as quotation for teaching. They are not covered by the course's licence and are not offered for reuse.
