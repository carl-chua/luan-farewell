# Sound

The card looks for **`audio/theme.mp3`** and wires it up automatically:

- If the file is here → a speaker button appears top-right of the phone,
  pulsing cyan until you start it. Sound fades in on the first click.
- If the file is missing → the button stays hidden and the card runs silently.
  Nothing breaks.

So: drop your file in this folder, name it `theme.mp3`, done.

## Getting the track

The Attack on Titan opening is *Guren no Yumiya* ("Feuerroter Pfeil und Bogen")
by Linked Horizon. It's commercial copyrighted music, so use a copy you're
entitled to — e.g. export from a track you've bought, or rip from your own CD.

Worth knowing: a page playing a copyrighted song is fine on your own machine,
but it becomes a public performance once you host it on a URL and send it
around. For a card that's only going to Luan and the team, nobody is going to
care. If it ends up somewhere public, that's the thing to think about.

## Alternatives that dodge the issue entirely

- A royalty-free epic/orchestral track (Pixabay Music, Uppbeat, YouTube Audio
  Library) — the *vibe* of the OP without the licensing question.
- A voice memo from the team instead of music. Honestly might land better.

## Other formats

`.m4a`, `.ogg` and `.wav` all work — just change `AUDIO_SRC` near the bottom
of `index.html` to match your filename. Volume is the `VOLUME` const on the
next line (currently `0.5`).
