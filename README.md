# Jota WA Mock

Protótipo ultra-realista do WhatsApp pra simular as conversas do Jota.

## Estrutura

- `index.html` — canvas principal (phone + chat + cenas)
- `chart-test.html` — teste isolado do donut chart pra Tela 4
- `wa-refs/` — screenshots reais de WhatsApp iOS usados como referência de fidelidade
- Assets: `header.png`, `input.png`, `input-margin.png`, `Slice 1.png` (teclado), `bgDoodle.png`, `REC-ui.png`, `REC-ui-target.png`, `audio-sending-blank.png`, `audio-sending.png`, `audio-sent.png`, `typing.png`, `nota-fiscal.png`

## Controles

- `k` — toggle teclado
- `h` — esconde painel dev (pra screenshot limpo)
- Botões dev: Teclado, Tela 2, Reset chat, Esconder
- Segura mic do input (com teclado aberto) → grava → solta → dispara Tela 1

## Autoplay (pra render headless / vídeo)

`?autoplay=tela1` ou `?autoplay=tela2` ou `?autoplay=both`
+ `&hidedev=1` esconde os botões dev
