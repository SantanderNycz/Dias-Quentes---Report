# Dias Quentes — Agosto 2026

Relatório de campanha da Laskasas Portugal, publicado como página estática.

## O que é

Uma única página (`index.html`) autossuficiente. Não precisa de _build_ nem de
instalar nada: React, Recharts e Babel são carregados por CDN e o componente do
relatório é transpilado no próprio browser.

Os dados e o texto vêm do componente original `report_dias_quentes_ago2026.jsx`,
mantido no repositório como fonte de referência.

## Ver localmente

Basta abrir o `index.html` no browser. Como recorre a CDNs, é preciso ligação à
internet. Para servir localmente (recomendado, evita restrições de `file://`):

```bash
# Python 3
python3 -m http.server 8000
# depois abrir http://localhost:8000
```

## Deploy

Qualquer serviço de alojamento estático serve. O `index.html` está na raiz.

- **GitHub Pages** — em _Settings → Pages_, escolher a branch e a pasta raiz (`/`).
- **Netlify** — arrastar a pasta para o painel, ou ligar o repositório (sem _build
  command_; _publish directory_ = raiz).
- **Vercel** — importar o repositório; _framework preset_ = "Other", sem _build_.
- **Cloudflare Pages** — igual: sem _build command_, _output directory_ = raiz.

## Estrutura

```
index.html                        página do relatório (deploy)
report_dias_quentes_ago2026.jsx   componente React original (referência)
README.md
```
