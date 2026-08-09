# gscav.com

Site da GSC Assistente Virtual. Site estático, sem build: os arquivos
publicados são exatamente os que estão aqui.

## Arquivos

| Arquivo | O que é |
|---|---|
| `index.html` | Página principal |
| `sistema.html` | Página "O Sistema", publicada em `/sistema` |
| `vercel.json` | Tira o `.html` das URLs (`cleanUrls`) |
| `og.png` | Imagem da prévia de link no WhatsApp (1200×630) |
| `favicon.png` | Ícone da aba do navegador |
| `apple-touch-icon.png` | Ícone do atalho no iPhone |

As páginas são autossuficientes: CSS, fotos, logos e a biblioteca de
animação estão embutidos no próprio HTML. Só as fontes vêm de fora
(Google Fonts).

## Como publicar uma alteração

O site fica na Vercel, conectada a este repositório. Todo commit enviado
para a branch `main` publica sozinho, em cerca de um minuto.

```bash
git add -A
git commit -m "descreva o que mudou"
git push
```

Para conferir antes de publicar, abra o `index.html` direto no navegador.

## Como voltar uma versão

```bash
git log --oneline          # lista as versões
git revert <código>        # desfaz uma delas e publica a correção
```

O primeiro commit guarda o site exatamente como estava publicado antes
das alterações de agosto de 2026.

## Onde mexer em cada coisa

- **Avaliações**: procure por `AVALIACAO 1` no `index.html`. Cada cartão
  tem, no comentário acima, o link da avaliação original no Google.
  A nota média e a quantidade ficam no bloco `rv-score`.
- **Trilha do "Como funciona"**: procure por `t-step` no `index.html`.
- **Telas do sistema**: procure por `p-consultas`, `p-fin`, `p-contatos`,
  `p-planos` no `sistema.html`. Os dados são fictícios, de propósito.
- **Prévia do WhatsApp**: as meta tags `og:` ficam no topo dos dois
  arquivos. Ao trocar a `og.png`, o WhatsApp guarda a imagem antiga em
  cache por alguns dias.
