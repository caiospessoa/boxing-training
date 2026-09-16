# 🐯 Treinos

A personal workout app — because the "Personal Digital" interface had every chance to be good and isn't.

Four workouts, one full screen, zero ads, zero login, zero drama. Open, tap, train.

## What's in here

| Workout | When | What |
|---|---|---|
| 🅰️ **Treino A** | Monday | 100 reps — lower push / upper pull |
| 🅱️ **Treino B** | Thursday | 100 reps — lower pull / upper push |
| 🔥 **MAS** | Tuesday & Friday | Maximal Aerobic Speed — 30/30 protocol |

Each workout follows a block structure:

1. **Movement prep** — mobility and activation, done once, no forced rest.
2. **Main set** — the real circuit, timed, with adjustable laps. Toggle between **Circuit mode** (round-robin, 40s work/40s rest) and **Isolated mode** (5 straight sets of 10 per exercise, 1 min rest) depending on how busy the gym is.
3. **Accessories / power** — finisher work, traditional strength or plyometrics.

MAS additionally has an activation+power block (6 exercises chained in one loop) and a true interval block (5 rounds of 30s-on/30s-off per exercise, 2 full passes).

## Why it exists

Because trying to figure out "wait, how many sets again?" mid-workout, sweaty phone in hand, inside an app full of videos that need to load, sucks. This one:

- Shows a **photo of each exercise** on screen (pulled from the trainer's original PDFs)
- Has **short looping video clips** for the trickier movements — real footage, not stock, cropped and compressed to load instantly
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
- Photos embedded as base64 directly in the HTML (instant load, no image server)
- Video clips are separate `.mp4` files referenced from `videos/`, with automatic fallback to the photo if a clip fails to load
- Progress and mode preferences saved in `localStorage`
- Design built to be read fast with the blurry vision of someone mid-set

## Structure
# 🐯 Treinos

A personal workout app — because the "Personal Digital" interface had every chance to be good and isn't.

Four workouts, one full screen, zero ads, zero login, zero drama. Open, tap, train.

## What's in here

| Workout | When | What |
|---|---|---|
| 🅰️ **Treino A** | Monday | 100 reps — lower push / upper pull |
| 🅱️ **Treino B** | Thursday | 100 reps — lower pull / upper push |
| 🔥 **MAS** | Tuesday & Friday | Maximal Aerobic Speed — 30/30 protocol |

Each workout follows a block structure:

1. **Movement prep** — mobility and activation, done once, no forced rest.
2. **Main set** — the real circuit, timed, with adjustable laps. Toggle between **Circuit mode** (round-robin, 40s work/40s rest) and **Isolated mode** (5 straight sets of 10 per exercise, 1 min rest) depending on how busy the gym is.
3. **Accessories / power** — finisher work, traditional strength or plyometrics.

MAS additionally has an activation+power block (6 exercises chained in one loop) and a true interval block (5 rounds of 30s-on/30s-off per exercise, 2 full passes).

## Why it exists

Because trying to figure out "wait, how many sets again?" mid-workout, sweaty phone in hand, inside an app full of videos that need to load, sucks. This one:

- Shows a **photo of each exercise** on screen (pulled from the trainer's original PDFs)
- Has **short looping video clips** for the trickier movements — real footage, not stock, cropped and compressed to load instantly
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
- Photos embedded as base64 directly in the HTML (instant load, no image server)
- Video clips are separate `.mp4` files referenced from `videos/`, with automatic fallback to the photo if a clip fails to load
- Progress and mode preferences saved in `localStorage`
- Design built to be read fast with the blurry vision of someone mid-set

## Structure

├── index.html # home screen, pick your workout
├── treino-a.html
├── treino-b.html
├── treino-mas.html
└── videos/ # exercise demo clips (mp4, no audio)
├── a-agachamento-detalhado.mp4
├── a-push-press-unilateral.mp4
├── a-remada-suspensa.mp4
├── a-tall-plank-chops.mp4
├── ab-agachamento-elevando-bracos.mp4
├── ab-elevacao-lateral-isometrica-rotacao.mp4
├── ab-manguito-rotacao-externa-peso.mp4
├── b-barra-fixa-livre-pegada-aberta.mp4
├── b-bulgaro.mp4
├── b-canoa-isometrica.mp4
├── b-stiff-detalhado.mp4
├── mas-aceleracao-elastico.mp4
├── mas-good-morning.mp4
└── mas-propriocepcao-unipodal.mp4


Files prefixed `ab-` are shared between Treino A and B (identical exercise in both prep blocks). Everything else without a video still falls back to its photo — more clips get added over time.

---

*Based on a personal trainer's plan. Built because no commercial app solves the problem of "I just want to see the next exercise, fast."*