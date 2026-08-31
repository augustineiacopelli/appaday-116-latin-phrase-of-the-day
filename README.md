# Latin Phrase of the Day

**App 116 of AppADay**

**Live:** https://augustineiacopelli.github.io/appaday-116-latin-phrase-of-the-day/

**Portfolio:** https://augustineiacopelli.github.io/appaday/

A daily Latin phrase, drawn from a hand-curated set of one hundred spanning liturgy, law, philosophy, and mottoes. Each entry carries the Latin, an English translation, a phonetic pronunciation guide, and a short note on where or how the phrase is used. Today's phrase is selected deterministically from the day of the year, so everyone sees the same phrase on the same date, and the Archive shares that same logic to page backward and forward through any day.

## Features

The Today view shows the day's full phrase with its category, translation, pronunciation, and usage note, and a favorite toggle that persists locally. The Archive view lets you filter by category and page day by day, with each entry collapsed to its Latin headline until tapped open for full detail. A segmented control switches between the two views, and the last view and archive position are remembered between visits.

## How it works

A `getPhraseForOffset` function computes the current day of year, adds an offset, and indexes into the phrase array modulo its length, wrapping cleanly at the start and end of the year. This one function backs both the Today view at offset zero and the Archive's paging at any offset. Favorited phrase ids and the last-viewed state are stored in two separate localStorage keys, both wrapped in try/catch so the app still works if storage is unavailable.

## Build

Single self-contained `index.html`. No frameworks, no build step, no external dependencies beyond Google Fonts. Built to be usable from a 375px phone up through desktop.
