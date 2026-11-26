# Cepercon Pré-Moldados — site

Site institucional da **Cepercon Pré-Moldados** (Imbuia/SC): estruturas pré-moldadas de concreto armado.
*É pré-moldado pra vida toda.*

**Site no ar:** https://csrhee24.github.io/cepercon-site/

## O que tem

- **Cena 3D no fundo** (Three.js r128): um galpão pré-moldado, inspirado nas obras da Cepercon em Imbuia, é montado peça por peça por dois caminhões munck conforme a página rola, com a equipe guiando as peças.
- **Visual "liquid glass"** no estilo Apple, animações de scroll e texto que acende palavra por palavra.
- **Obras realizadas** em carrossel (fotos do Instagram da Cepercon, com link para cada post).
- **Produtos** com imagens 3D geradas no navegador (pilares, vigas, placas, braços, sapatas, escadas, terças e lajes).
- **Orçamento pelo WhatsApp**: todos os botões e o formulário abrem uma conversa com a mensagem pronta.

## Estrutura

```
index.html                  página única (HTML, CSS e JS)
assets/
  logo-dark.png             logo para fundo escuro (usado no site)
  logo-light.png            logo para fundo claro
  logo-mark.png             símbolo (ícone da aba)
  logo-original.png         arquivo original enviado
  obras/                    fotos do carrossel de obras
prompt-melhorias-vendas.md  próximos passos (funções de vendas)
.claude/serve.ps1           servidor local para pré-visualizar
```

## Rodar localmente

O site é estático. Para ver com as imagens carregando, sirva a pasta por HTTP:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File .claude/serve.ps1
```

e abra http://localhost:8080.

## Editar conteúdo

- **Obras do carrossel:** lista `OBRAS` no `index.html` (campo `img` aponta para `assets/obras/...`).
- **Produtos:** seção `<!-- PRODUTOS -->`; cada imagem 3D é escolhida pelo atributo `data-model`.
- **WhatsApp:** constante `WA` no `index.html`.

## Publicar

Qualquer hospedagem estática serve (GitHub Pages, Netlify, Vercel, Cloudflare Pages): envie `index.html` e a pasta `assets/`.
