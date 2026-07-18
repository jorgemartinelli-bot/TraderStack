# TraderStack — Kit de Marca v1

Conceito escolhido: **Stacked Candles** — três barras ascendentes de gráfico construídas por blocos empilhados. Cada bloco é uma ferramenta do stack; o bloco verde no topo é a camada nova / o ganho.

## Paleta

| Uso | Cor | Hex |
|---|---|---|
| Ink (principal) | azul-petróleo quase preto | `#0D1520` |
| Signal Green (acento, fundo claro) | verde candle de alta | `#00A86B` |
| Signal Green (acento, fundo escuro) | verde claro | `#1FCE8F` |
| Marca sobre fundo escuro | off-white | `#F2F5F4` |
| Slate (texto secundário) | | `#3D4B59` |
| Paper (fundo claro) | | `#F7F9F8` |

Regra: vermelho nunca entra na marca — fica reservado para semântica de perda dentro do produto.

## Arquivos

### `svg/` (vetores master — editar aqui)
- `icon-light.svg` / `icon-dark.svg` — símbolo para fundo claro/escuro
- `favicon.svg` — silhueta simplificada (3 barras) para tamanhos ≤ 32 px
- `app-tile.svg` — símbolo sobre tile ink arredondado
- `lockup-horizontal-light/dark.svg` — símbolo + wordmark (texto editável; converter para curvas na arte final)

### `png/` (prontos para uso)
- `icon-*-{32..1024}.png` — símbolo transparente
- `favicon.ico` + `favicon-{16,32,64}.png` — para o site
- `app-tile-{180,192,512,1024}.png` — 180 = apple-touch-icon, 192 = Android
- `avatar-circle-{400,1024}.png` — redes sociais (X, Instagram, Discord)
- `lockup-horizontal-*-h{72,144,576}.png` — cabeçalho de site, e-mail, docs
- `og-image-1200x630.png` — preview de link (Open Graph / redes sociais)

## Wordmark

`Trader` em peso regular + `Stack` em peso máximo (o nome "empilha" peso da esquerda para a direita). Prévia renderizada em Segoe UI; para a arte final, licenciar uma grotesca geométrica com dígitos tabulares (Hanken Grotesk, Archivo ou Geist) e usar a mesma como fonte do produto.

## Regenerar

Script gerador (Python + Pillow): a geometria canônica dos blocos está no script e nos SVGs (viewBox 64). Blocos: coluna 1 = 1 bloco, coluna 2 = 2, coluna 3 = 3 (topo verde), unidade 10×12 rx3, baseline y=54.
