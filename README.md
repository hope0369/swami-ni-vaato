# Swami Ni Vaato Finder

A small website for reading **સ્વામીની વાતો (Swami Ni Vaato)**, the talks of Aksharbrahman Gunatitanand Swami, from all seven prakarans. It holds all 1,484 vatos in Gujarati, English and transliteration, with footnotes.

## What it does

- **How are you feeling?** Pick a feeling, such as sad, anxious, unwell, missing someone, or grateful, and get a hand-picked set of vatos for it.
- **Subjects.** Hand-picked lists for Seva, Life as a householder, and Brutal honesty (the hard sayings), plus 52 topic tags.
- **Search.** Search in English, Gujarati or transliteration; accents are optional. English and romanised words also find the Gujarati: `seva` finds સેવા. A reference like `5.313` or `૫.૩૧૩` opens that vat directly.
- **Prakarans.** Read any prakaran in order, or jump straight to a vat.
- **Show text in.** Choose Both, Gujarati only, or English only.
- **Save and copy.** Saved vatos stay in your browser only.

It is one self-contained `index.html`. It needs no server, has no tracking and no cookies, and works offline once loaded.

## Text

The Gujarati text, English translation, transliteration and footnotes are from the 7-prakaran edition as published on [anirdesh.com](https://www.anirdesh.com/vato/), used with permission. Every vat links to its page there.

The feeling lists, subject lists and descriptive text on the site are original to this project.

## Security

- A strict Content-Security-Policy allows only the page's own script and style, by hash, plus Google Fonts.
- There are no network requests, no forms that submit anywhere, and no third-party scripts.
- All text is escaped before display, and the embedded data cannot break out of its script block.
- Outbound links use `noopener noreferrer`, and the page sends no referrer.
