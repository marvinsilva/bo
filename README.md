# Triagem de ocorrências (PCRS)

Página única (`index.html`), sem servidor. Lê boletins em PDF no navegador, classifica por tipo,
liga casos com dados em comum e ordena por prioridade.

## Publicar no GitHub Pages
1. Crie um repositório e envie o `index.html` (e este README, se quiser).
2. Settings > Pages > Source: "Deploy from a branch" > `main` / `(root)`.
3. O endereço aparece na mesma tela.

**Não envie BOs reais para o repositório.** O site é público e os BOs ficam só na memória do navegador de quem os soltar na página.

## Uso sem internet (rede interna)
A página carrega pdf.js e JSZip do cdnjs e as fontes do Google. Sem internet, baixe estes arquivos para uma pasta `vendor/` ao lado do `index.html`:
- `pdf.min.js` e `pdf.worker.min.js` (pdf.js 3.11.174)
- `jszip.min.js` (JSZip 3.10.1)

## Ajustes
- Pesos de prioridade e limite de semelhança: botão "Parâmetros".
- Palavras-chave dos subtipos de golpe: `SUBTIPOS_FRAUDE` no script (início do bloco do parser).
- Categorias: `FAMILIAS`.
