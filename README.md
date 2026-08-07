# A Letter, In A Page 💌

A single-page, mobile-friendly, handcrafted love letter — built for reconciliation.
Blush pink, cream, and warm gold. Elegant serif type. Soft fade/slide animations.

There's nothing to install and no build step. Open `index.html` in a browser to see it.

---

## ✏️ Easiest way: edit it right on the page (no code)

Open the site on your phone or computer and it starts in **Editing** mode:

- **Tap any text** — her name, the memories, the reasons, your message — and just type. It saves automatically **on that device**.
- **Tap "⤴ change photo"** on any picture to swap in your own. Also saved on the device.
- Tap **Preview** to see it exactly as she will (tap **✎ Edit** to come back).
- When it's perfect, tap **Download final page** — you get a single `for-her.html`
  file with all your words and photos baked in and editing turned off. That file
  *is* her page: send it to her directly, or send it to me and I'll host it.

> Your edits live in that one browser. If you edit on your phone, do the final
> **Download** on your phone. Want me to lock in your version permanently on the
> live site instead? Just send me your `for-her.html` (or tell me the final text)
> and say **"lock it."**

---

## Or edit the source directly

Everything you personalize also lives in **`index.html`**. Open it in any text editor
and search for **`✎ EDIT`** — each spot is labeled. There are five things to change:

| # | What | Search for | How many |
|---|------|-----------|----------|
| 1 | Her name | `✎ EDIT · NAME` | 1 |
| 2 | Opening lines | `✎ EDIT · OPENING` | 2 short lines |
| 3 | Timeline moments | `✎ EDIT · TIMELINE` | 4–6 blocks |
| 4 | Photo gallery (tap → note) | `✎ EDIT · PHOTOS` | as many as you like |
| 5 | "Reasons I love you" cards | `✎ EDIT · REASONS` | 8–10 cards |
| 6 | Final message | `✎ EDIT · MESSAGE` | your words |

### Timeline moments
Each memory is one `<article class="moment ...">` block. Copy a block to add a
memory, delete one to remove it. Change the `date`, the `<h3>` title, and the `<p>`
caption. Keep the alternating `from-left` / `from-right` order so they slide in from
opposite sides on desktop.

### Reasons cards
Each reason is one `<div class="card ...">` block. The **front** shows the number
automatically; put the reason itself inside `card-back`. Tap (or click, or press
Enter) to flip. Add cards 9 and 10 by copying a block and bumping the `no`.

### Photo gallery (a photo that flips to a note)
Each photo is one `<div class="card photo-card ...">` block. Put your image files
next to `index.html` and set each one's name in `src="..."` (e.g. `photo1.jpg`,
`photo2.jpg`, …). The **front** is the photo with a small caption; tap it and it
flips to reveal the **note** on the back — same feel as the reasons cards. Until you
add an image, a soft blush placeholder shows in its place, so nothing looks broken.
Portrait-ish photos crop best. Add or remove blocks freely.

### The final message
This is the heart of the page — write it in your own voice. Add or remove `<p>`
paragraphs. The big italic line is the `closing`; the last line is your `signoff`.

---

## Optional: background music 🎵

Drop an audio file named **`music.mp3`** in the same folder as `index.html`.
A small circular toggle appears in the bottom-right corner; tap it and the track
fades in gently and loops. **If there's no `music.mp3`, the toggle simply stays
hidden** — nothing to configure.

> Browsers block audio from auto-playing, so music only starts when *she* taps the
> toggle. That's intentional and works everywhere. Pick something quiet and yours —
> and make sure you have the right to use the file.

---

## Sharing it with her

It's just static files, so any of these work:

- **Netlify Drop** — drag the folder onto <https://app.netlify.com/drop>, get a link.
- **GitHub Pages** — enable Pages on this repo/branch.
- **Vercel** — import the repo, deploy.
- Or zip the folder and send it; she opens `index.html`.

---

## Notes

- **Fonts:** Cormorant Garamond (headings) + EB Garamond (body), loaded from Google
  Fonts, with system-serif fallbacks if offline.
- **Reduced motion:** if her device is set to "reduce motion," animations quiet
  down automatically.
- **No tracking, no analytics, no dependencies** — just HTML, CSS, and a little JS.
