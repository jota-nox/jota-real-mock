# Status — pra retomar

**Última versão:** v3.9 (publicada em https://jota-real-mock.vercel.app)
**Data do snapshot:** 2026-04-28

---

## Onde estamos

Os 5 roteiros estão **funcionais e publicados**. Visualmente fiéis ao WhatsApp iOS — bolhas, tails, charts, áudios, fotos, quotes inline, formatação rich text. Auto-deploy GitHub → Vercel ativo.

## O que tá ROLANDO bem

- **Hub** (`index.html`) lista os 5 roteiros com WIP badges, links pra autoplay individual, autoplay all, e script de apresentação ao vivo
- **5 protótipos** (`roteiroN.html`) — Categorização, Fiado, 3 Perspectivas, Lista Funcional, A Moto
- **Charts** (`chart-categorias.png`, `chart-faturamento.png`, `chart-projecao.png`) seguindo template Figma
- **Bolhas SVG dinâmicas** — path gerado em JS baseado nas dimensões da bolha; tail mantém tamanho fixo (8×13px) sem distorção (v3.9)
- **Tail aparece em** text/audio/photo/image (todas as variantes)

## Decisão pendente — TAILS, parte 2

User testou v3.9 e ficou OK mas decidiu fazer **9-slice** depois pra fidelidade absoluta. Status:
- v3.9 atual usa SVG path gerado dinamicamente em JS (rect arredondado + tail no canto)
- Próxima iteração: **CSS `border-image` com asset 9-slice** desenhado pra preservar cantos+tail nas 4 zonas estáveis enquanto o meio se estica
- Já temos 2 SVG paths originais do user (verde e branco) que podem virar base do 9-slice asset

User: "vamos fazer 9 slice, mas nao agora" → **AGUARDA SINAL DELE PRA RETOMAR**

## Pra retomar numa sessão nova

```bash
# Abrir o protótipo
open /Users/felippo/Documents/jota-real-mock/index.html

# Ou direto online
open https://jota-real-mock.vercel.app

# Status do repo
cd /Users/felippo/Documents/jota-real-mock && git log --oneline | head -10
```

Memória chave em `~/.claude/projects/-Users-felippo-Documents/memory/project_jota_wa_canvas.md` tem:
- Estrutura de pastas e assets
- Truque do input + teclado (kbH - extraSafe)
- Calibração do timer da gravação
- Workflow de fidelidade visual com agentes em paralelo
- Status público do projeto

## Histórico recente (últimos 6 commits)

```
v3.9 — SVG bubble dinâmico (tail tamanho fixo, sem distorção)
v3.8 — SVG vector bubble em TODAS as variantes (audio/photo/image)
v3.7 — bolhas SVG vector com tail integrado
v3.6 — tails token novos (54×36) + fix typing tail
v3.5 — charts redesenhados com fidelidade ao Figma
v3.4 — tails reais cropados do iOS WhatsApp
```

## Próximos blocos possíveis (não-priorizados)

1. **9-slice border-image pros tails** (combinado, aguardando user)
2. Empacotar como **Skill Claude Code** (`jota-wa-roteiros`) pra gerar roteiros novos via prompt
3. Expor DSL YAML pra roteiros (formato compartilhável fora do Claude)
4. Refinos visuais que ficaram pendentes:
   - Posicionamento de bolhas no aparecimento (mencionado mas não atacado)
   - Sombra das bolhas (drop-shadow vs filter)
5. Substituir charts placeholder por imagens finais quando o user gerar
