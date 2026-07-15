# For You: Luan 👋

A farewell card shaped like a TikTok FYP feed. 18 wishes, one per "post",
vertical scroll-snap, working like button, double-tap to like.

## Open it

Double-click `index.html`. That's it — no build, no dependencies.

## Add the real wishes

Everything editable lives in one array near the bottom of `index.html`,
under the comment `EDIT HERE`. One entry per person:

```js
{ name:"carl_chua", theme:0, tags:["fyp","luan"], sound:"original sound — carl",
  wish:"Your actual message goes here." },
```

- `name` — shows as the `@handle`, and seeds the avatar initials.
- `wish` — the caption. Aim for 1–2 sentences; much longer starts to crowd.
- `tags` — hashtags under the caption. Drop the `#`.
- `sound` — the scrolling music ticker. Any string works.
- `theme` — `0`–`5`. Already arranged so no two neighbours share a colour.
  Only touch it if you reorder people; just avoid repeating one back-to-back.
- `mark` — optional watermark: `"wings"` (Mikasa), `"thorn"` (Yor), or omit
  for the music note. Themes 3 and 4 are the crimson/gold anime posts and
  already carry the matching art.

Adding or removing people is fine — the counter and the cover both read the
array length. If you change the count, update the two hardcoded `18`s in the
cover copy and the outro stats.

## Photos

The same collage sits behind every wish — three photos stacked as bands. The
only thing that changes down the feed is the colour it's duotoned into, which
comes from each wish's `theme`.

Used: `luan1.jpg` (also the cover and the record label), `luan2.jpg` (also the
outro), `luan4.jpg`. `luan3.jpg` is still in `images/` but unused — swap it
into `PHOTOS` any time.

To change the collage, edit the `PHOTOS` array near the bottom of `index.html`:

```js
{ src:"images/luan1.jpg", crop:"50% 40%" },
```

`crop` is the focal point of that band — nudge the second number to slide the
band up or down over people's faces. Add or remove an entry and the grid
re-splits by itself.

To give one wish a single full-bleed photo instead of the collage, add
`photo:"images/whatever.jpg"` to that entry — it takes over for that post.

`images/original/` holds your untouched uploads. Only `luan2.jpg` was resized
for the web (4032px / 1.4MB, far more than a phone-width band can use); the
rest are exactly as you sent them.

## Sound

`audio/theme.mp3` is wired up: a speaker button appears top-right, pulsing
until you start it, then fades in. Browsers block autoplay, so it waits for
the first click. If the file is ever missing the button just hides itself.

Change `AUDIO_SRC` / `VOLUME` near the bottom of `index.html` to swap the
track or adjust the level. See `audio/README.md` for the copyright note.

## Notes

Fonts (Anton, Chakra Petch, Zen Kaku Gothic New) load from Google Fonts, so
it looks best online. Offline it falls back to system faces and still works.
