# 🐯 Treinos

App de treino pessoal — porque a interface do "Personal Digital" tinha tudo pra ser boa e não é.

Três treinos, uma tela cheia, zero anúncio, zero login, zero drama. Abre, toca, treina.

## O que tem aqui

| Treino | Quando | O quê |
|---|---|---|
| 🅰️ **Treino A** | Segunda | 100 repetições — empurrar inferior / puxar superior |
| 🅱️ **Treino B** | Quinta | 100 repetições — puxar inferior / empurrar superior |
| 🔥 **MAS** | Terça e sexta | Maximal Aerobic Speed — protocolo 30/30 |

Cada treino segue a mesma lógica de 3-4 blocos:

1. **Preparação de movimento** — mobilidade e ativação, feito uma vez só, sem descanso forçado.
2. **Parte principal** — o circuito de verdade, cronometrado, com voltas ajustáveis.
3. **Acessórios / potência** — fechamento, força tradicional ou pliometria.

## Por que existe

Porque ficar catando "quantas séries mesmo?" no meio do treino, com a mão suada no celular, dentro de um app cheio de vídeo pra carregar, é osso. Isso aqui:

- Tem **foto de cada exercício** direto na tela (puxadas do PDF original do personal)
- **Cronômetro embutido**, com beep nos 3-2-1 e vibração
- Mostra o **próximo exercício** já durante o descanso, pra você não perder o timing
- **Salva seu progresso sozinho** — se a tela travar ou o zap chamar no meio do treino, reabre e continua de onde parou
- Funciona **100% offline** depois do primeiro carregamento
- Zero framework, zero build step, zero dependência de internet pra rodar

## Como usar

Abre o [`index.html`](./index.html), escolhe o treino do dia, bora.

No celular: adiciona à tela inicial (Compartilhar → Adicionar à Tela de Início) e ele abre em tela cheia, sem barra de navegador, como se fosse um app de verdade.

## Como é feito

- HTML + CSS + JS puro, um arquivo por treino, nada de build
- Fotos embutidas como base64 direto no HTML (por isso os arquivos não são pequenos, mas carregam instantâneo e não dependem de servidor de imagem)
- Progresso salvo em `localStorage`
- Design pensado pra ser lido rápido com a visão embaçada de quem tá no meio de uma série

## Estrutura

```
.
├── index.html        # tela inicial, escolhe o treino
├── treino-a.html      
├── treino-b.html      
└── treino-mas.html   
```

---

*Baseado no plano do personal trainer. Feito porque nenhum app comercial resolve o problema de "eu só quero ver o próximo exercício rápido".*
