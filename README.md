# Swami Ni Vaato Finder

A small website for reading **સ્વામીની વાતો (Swami Ni Vaato)**, the talks of Aksharbrahman Gunatitanand Swami, from sixteen prakarans. Prakarans 1 to 7 (1,484 vatos) are in Gujarati, English and transliteration, with footnotes; prakarans 8 to 16 (2,314 vatos) are in Gujarati. Old words carry their meanings: tap a dotted word to see it.

## What it does

- **Today.** The home page opens with “જય સ્વામિનારાયણ” and a vat for the day. Tap "Another vat" for a new one.
- **How is your heart today?** Twelve feelings, such as sad, anxious, unwell, missing someone, or grateful. Tap one to swipe through the vatos chosen for it, one card at a time, like stories.
- **Subjects.** Hard words (કઠણ વચન, the hard sayings), hand-picked, then all the topics, including hand-picked lists for Seva and Life as a householder. Any list can be read as swipe cards.
- **Search.** Search in English, Gujarati or transliteration; accents are optional. English and romanised words also find the Gujarati: `seva` finds સેવા. A reference like `5.313` or `૫.૩૧૩` opens that vat directly.
- **Share.** Send any vat to WhatsApp, copy it, copy its link, or turn it into a picture for status.
- **Reading settings (Aa).** Larger text, Gujarati only, English only, or both, and a light or dark theme.
- **Save.** Saved vatos stay in your browser only.

It is one `index.html` with the Gujarati and English text built in, plus `extra-….json` (transliteration and footnotes) and `more-….json` (prakarans 8 to 16), which the page fetches after the first vat is on screen so it opens faster on a slow phone. It needs no server and has no tracking and no cookies. After the first visit it works fully offline, and it can be added to the home screen as an app: on iPhone, Share → Add to Home Screen; on Android, the browser menu → Install app. A small service worker (`sw.js`) keeps a copy of the page, the transliteration file and the fonts; it opens from that copy straight away and fetches any update in the background, so changes show on the next open.

## Text

Prakarans 1 to 7 (Gujarati text, English translation, transliteration and footnotes) are from the 7-prakaran edition of Swami Ni Vaato. Prakarans 8 to 16 and the word meanings are from the 16-prakaran edition.

The feeling lists, subject lists and descriptive text on the site are original to this project.

## Security

- A strict Content-Security-Policy allows only the page's own script and style, by hash, plus Google Fonts.
- The page makes no network requests beyond its own data files and Google Fonts, has no forms that submit anywhere, and runs no third-party scripts. The service worker only fetches this site's own files and the fonts.
- All text is escaped before display, and the embedded data cannot break out of its script block.
- Outbound links use `noopener noreferrer`, and the page sends no referrer.
