A personal workout app — because the "Personal Digital" interface had every chance to be good and isn't.

Three workouts, one full screen, zero ads, zero login, zero drama. Open, tap, train.

## What's in here

| Workout | When | What |
|---|---|---|
| 🅰️ **Treino A** | 100 reps — lower push / upper pull |
| 🅱️ **Treino B** | 100 reps — lower pull / upper push |
| 🔥 **MAS** | Maximal Aerobic Speed — 30/30 protocol |

Each workout follows the same 3-4 block logic:

1. **Movement prep** — mobility and activation, done once, no forced rest.
2. **Main set** — the real circuit, timed, with adjustable laps.
3. **Accessories/power** — finisher work, traditional strength or plyometrics.

## Why it exists

Because trying to figure out "wait, how many sets again?" mid-workout, sweaty phone in hand, inside an app full of videos that need to load, sucks. This one:

- Shows a **photo of each exercise** right on screen (pulled straight from the trainer's original PDF)
- Has a **built-in timer**, with a 3-2-1 beep and vibration
- Shows the **next exercise** during rest, so you never lose the timing
- **Saves your progress automatically** — if your screen locks or a call interrupts mid-workout, it reopens right where you left off
- Works **100% offline** after the first load
- Zero frameworks, zero build step, zero dependency on the internet to run

## How to use it

Open [`index.html`](./index.html), pick today's workout, go.

On mobile: add it to your home screen (Share → Add to Home Screen) and it opens full-screen, no browser bar, like a real app.

## How it's built

- Plain HTML + CSS + JS, one file per workout, no build process
- Photos embedded as base64 directly in the HTML (that's why the files aren't tiny, but they load instantly and don't depend on an image server)
- Progress saved in `localStorage`
- Design built to be read fast with the blurry vision of someone mid-set

## Structure
