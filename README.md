# Agenda Astrologia — widget rosa pastel

## O que tem aqui
- `index.html` — o widget do calendário (auto-contido, sem dependências além de fontes do Google).
- `astrologia.ics` — sua exportação da agenda "Astrologia". O widget lê esse arquivo direto, sem precisar de API do Google.

## Como colocar no GitHub Pages
1. Crie um repositório novo no GitHub (pode ser público).
2. Suba os dois arquivos (`index.html` e `astrologia.ics`) para a raiz do repositório.
3. Vá em **Settings → Pages**, em "Branch" escolha `main` (ou `master`) e pasta `/root`, salve.
4. Espere ~1 minuto. O GitHub te dá uma URL tipo `https://SEUUSUARIO.github.io/NOMEDOREPO/`.
5. No Notion, use o bloco **Embed** (digite `/embed`) e cole essa URL.

## Atualizar os eventos no futuro
Quando quiser atualizar a agenda, exporte de novo o `.ics` do Google Calendar (Configurações da agenda → Exportar agenda), substitua o arquivo `astrologia.ics` no repositório mantendo o mesmo nome, e o widget já reflete a mudança automaticamente — não precisa mexer no `index.html`.

## Personalizar as cores
Todas as cores ficam no topo do `index.html`, dentro de `:root { ... }`. Os principais:
- `--rose` / `--rose-strong` — tom principal dos eventos e dia selecionado
- `--blush-1` / `--blush-2` — fundo suave do painel de eventos
- `--lilac` — destaque do dia de hoje
- `--ink` — cor do texto

Troque os valores hexadecimais e salve; não precisa de mais nada.
