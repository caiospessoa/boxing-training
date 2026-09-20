# EN-US #
# 🐯 Training

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
2. **Main set** — the real circuit, timed. Toggle between **Circuit mode** (round-robin, 40s work/40s rest, 10 laps) and **Isolated mode** (5 straight sets of 10 per exercise, 1 min rest) depending on how busy the gym is.
3. **Accessories** — finisher work. Also toggles between **Circuit** (round-robin) and **Isolated** (all sets of one exercise before the next) — same set count and rest either way, just reordered.

MAS additionally has an activation+power block (6 exercises chained in one loop, 2 passes) and a true interval block (5 rounds of 30s-on/30s-off per exercise, 2 full passes).

## Why it exists

Because trying to figure out "wait, how many sets again?" mid-workout, sweaty phone in hand, inside an app full of videos that need to load, sucks. This one:

- Shows a **photo of each exercise** on screen (pulled from the trainer's original PDFs)
- Has **short looping video clips** for the trickier movements — real footage, cropped and compressed to load instantly, with automatic fallback to the photo
- Has a **built-in timer**, with a 3-2-1 beep and a distinct two-tone chime when rest ends
- **Keeps the screen awake** for the whole workout (Screen Wake Lock — needs iOS 16.4+, works in Safari and Chrome on iPhone since both run on WebKit)
- Shows the **next exercise** during rest, so you never lose the timing
- **Saves your progress automatically** — if your screen locks or a call interrupts mid-workout, it reopens right where you left off
- Works **100% offline** after the first load
- Zero frameworks, zero build step, zero dependency on the internet to run

## How to use it

Open [`index.html`](./index.html), pick today's workout, go.

On mobile: add it to your home screen (Share → Add to Home Screen) and it opens full-screen, no browser bar, like a real app. Works this way from Safari; Chrome on iPhone may vary depending on version.

## How it's built

- Plain HTML + CSS + JS, one file per workout, no build process
- Photos embedded as base64 directly in the HTML (instant load, no image server)
- Video clips are separate `.mp4` files referenced from `videos/`, with automatic fallback to the photo if a clip fails to load
- Progress, lap counts, and circuit/isolated mode preferences saved in `localStorage`
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

# PT-BR #
# 🐯 Treinos

Um app de treino pessoal — porque a interface do "Personal Digital" tinha tudo pra ser boa e não é.

Quatro treinos, uma tela cheia, zero anúncio, zero login, zero drama. Abre, toca, treina.

## O que tem aqui

| Treino | Quando | O quê |
|---|---|---|
| 🅰️ **Treino A** | Segunda | 100 repetições — empurrar inferior / puxar superior |
| 🅱️ **Treino B** | Quinta | 100 repetições — puxar inferior / empurrar superior |
| 🔥 **MAS** | Terça e sexta | Maximal Aerobic Speed — protocolo 30/30 |

Cada treino segue uma estrutura de blocos:

1. **Preparação de movimento** — mobilidade e ativação, feito uma vez só, sem descanso forçado.
2. **Parte principal** — o circuito de verdade, cronometrado. Alterna entre **modo Circuito** (revezando, 40s trabalho/40s descanso, 10 voltas) e **modo Isolado** (5 séries seguidas de 10 por exercício, 1 min de descanso), dependendo de como a academia estiver.
3. **Acessórios** — fechamento. Também alterna entre **Circuito** (revezando) e **Isolado** (termina todas as séries de um exercício antes do próximo) — mesma quantidade de séries e descanso nos dois casos, só muda a ordem.

O MAS ainda tem um bloco de ativação+potência (6 exercícios encadeados num loop só, 2 passagens) e um bloco de intervalo de verdade (5 rounds de 30s ligado/30s desligado por exercício, 2 passagens completas).

## Por que existe

Porque ficar catando "quantas séries mesmo?" no meio do treino, com a mão suada no celular, dentro de um app cheio de vídeo pra carregar, é osso. Este aqui:

- Mostra uma **foto de cada exercício** na tela (extraídas dos PDFs originais do personal)
- Tem **clipes de vídeo curtos em loop** pros movimentos mais complicados — gravação de verdade, cortada e comprimida pra carregar na hora, com foto como reserva se o vídeo não carregar
- Tem **cronômetro embutido**, com beep nos 3-2-1 e um "tim-tim" de dois tons quando o descanso termina
- **Mantém a tela acesa** durante o treino inteiro (Screen Wake Lock — precisa de iOS 16.4+, funciona no Safari e no Chrome do iPhone, já que os dois rodam sobre o mesmo motor da Apple)
- Mostra o **próximo exercício** já durante o descanso, pra você não perder o timing
- **Salva seu progresso sozinho** — se a tela travar ou uma ligação interromper no meio do treino, reabre de onde parou
- Funciona **100% offline** depois do primeiro carregamento
- Zero framework, zero processo de build, zero dependência de internet pra rodar

## Como usar

Abre o [`index.html`](./index.html), escolhe o treino do dia, bora.

No celular: adiciona à tela inicial (Compartilhar → Adicionar à Tela de Início) e ele abre em tela cheia, sem barra de navegador, como um app de verdade. Funciona assim pelo Safari; no Chrome do iPhone pode variar dependendo da versão.

## Como é feito

- HTML + CSS + JS puro, um arquivo por treino, nada de build
- Fotos embutidas como base64 direto no HTML (carrega instantâneo, sem servidor de imagem)
- Os vídeos são arquivos `.mp4` separados, referenciados da pasta `videos/`, com foto como reserva automática se algum clipe não carregar
- Progresso, número de voltas e preferência de modo (circuito/isolado) salvos em `localStorage`
- Design pensado pra ser lido rápido com a visão embaçada de quem tá no meio de uma série

## Estrutura

.
├── index.html # tela inicial, escolhe o treino
├── treino-a.html
├── treino-b.html
├── treino-mas.html
└── videos/ # clipes de demonstração (mp4, sem áudio)
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


Arquivos com prefixo `ab-` são compartilhados entre o Treino A e B (exercício idêntico nos dois blocos de preparação). Tudo que ainda não tem vídeo cai de volta na foto — mais clipes vão sendo adicionados aos poucos.