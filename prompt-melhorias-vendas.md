# Prompt: transformar o site da Cepercon em máquina de vendas

Copie tudo abaixo e cole no assistente/dev que vai trabalhar no site.

---

Você vai evoluir o site institucional da **Cepercon Pré-Moldados** (Imbuia/SC, CNPJ 35.290.677/0001-96, WhatsApp (47) 98485-2333, Instagram @ceperconpremoldados). O site atual é um `index.html` único em `D:\Site`, com cena 3D (Three.js r128) de um galpão pré-moldado que se monta com o scroll, visual "liquid glass" estilo Apple, paleta azul da marca (#2e68ff / #5cc8ff) e logo em `assets/`. Todo CTA hoje leva ao WhatsApp com mensagem pronta.

## Objetivo
Aumentar o número de **pedidos de orçamento qualificados** (cliques no WhatsApp com informação útil: produto, quantidade, cidade). Cada mudança deve servir a esse objetivo. Mantenha o visual premium atual.

## Regras inegociáveis
- **Não invente dados.** Nada de depoimentos, números de obras, clientes, preços, prazos, garantias, certificações (ex.: NBR 9062) ou raio de entrega que a empresa não confirmou. Onde faltar dado, deixe um marcador visível `[[CONFIRMAR: ...]]` e liste no final.
- Fotos e vídeos só reais da Cepercon (fornecidos pelo cliente). Não use banco de imagens fingindo ser obra deles.
- Mobile primeiro: a maioria do tráfego (Instagram, Google, anúncios) vem do celular.
- Não quebre o que já funciona (montagem 3D, formulário → WhatsApp, logo).

## Prioridade 1 — Conversão (fazer primeiro)
1. **Calculadora de orçamento** (o maior gerador de leads):
   - *Muro:* metros lineares + altura → estimativa de placas e pilares.
   - *Cerca rural:* perímetro (m) ou área (ha) + espaçamento → quantidade de mourões/palanques.
   - O resultado vira mensagem pronta no WhatsApp ("Preciso de ~X placas e Y pilares para um muro de Z m em [cidade]"). Medidas das peças = `[[CONFIRMAR]]`.
2. **Barra fixa de CTA no celular** (rodapé): "WhatsApp" + "Ligar" (`tel:`), sempre visível após o hero.
3. **CTAs por público** logo após a montagem: "Sou produtor rural", "Vou construir/murar", "Sou construtora". Cada um rola para os produtos certos e muda a mensagem do WhatsApp.
4. **Qualificar a mensagem do WhatsApp:** perguntar no formulário prazo desejado e se precisa de entrega/instalação.
5. **Modo leve da cena 3D:** se o aparelho for fraco, a conexão for lenta (`navigator.connection.saveData`, poucos núcleos) ou o WebGL falhar, mostrar uma imagem estática (poster) no lugar. O primeiro conteúdo e o botão de orçamento precisam aparecer em menos de 2,5 s no 4G.

## Prioridade 2 — Confiança (o que faz o cliente decidir)
6. **Galeria "Obras realizadas"** com fotos reais (galpões, muros, caminhão munck montando). Cada obra: tipo, cidade e o que foi usado. Lightbox em vidro.
7. **Seção de entrega e montagem:** se a Cepercon tem caminhão munck próprio (aparece no Instagram), destacar "entregamos e montamos" `[[CONFIRMAR]]`.
8. **Depoimentos reais:** espaço pronto, mas só preenchido com depoimentos autorizados (ou incorporar avaliações do Google).
9. **FAQ** (com marcação FAQPage): prazo de fabricação, região atendida, entrega, instalação, formas de pagamento, peças sob medida. Respostas = `[[CONFIRMAR]]`.
10. **Dados da empresa visíveis:** endereço completo, horário, mapa do Google incorporado, CNPJ. Tudo `[[CONFIRMAR]]`, exceto o CNPJ.

## Prioridade 3 — Ser encontrado (Google local)
11. **SEO local:** title/description por intenção ("muro pré-moldado em Imbuia", "mourão de concreto Alto Vale"), schema `LocalBusiness` + `Product`, Open Graph com imagem bonita para compartilhar no WhatsApp, `sitemap.xml`, `robots.txt`.
12. **Páginas por produto** (`/muros`, `/mouroes`, `/pilares-vigas`, `/lajes`, `/caixas-tampas`) com especificações (dimensões, peso, aplicação), fotos e CTA. As especificações = `[[CONFIRMAR]]`.
13. **Páginas por cidade atendida** (Imbuia, Ituporanga, Vidal Ramos, Alfredo Wagner, Rio do Sul… lista = `[[CONFIRMAR]]`), com conteúdo próprio, nada copiado e colado.
14. Checklist do **Perfil da Empresa no Google** (fotos, categoria, link do site, pedir avaliações) entregue como documento para o cliente.

## Prioridade 4 — Medir para vender mais
15. **Rastrear conversões:** GA4 + Meta Pixel (opcional), com eventos `click_whatsapp`, `click_tel`, `calc_uso`, `form_envio` e qual produto/público. Ler e repassar UTMs na mensagem do WhatsApp (ex.: "vim pelo Instagram").
16. **Banner de cookies LGPD** se houver pixel/analytics (recusar por padrão o que não for essencial).
17. Link na bio do Instagram apontando para o site com UTM, no lugar do wa.link solto.

## Extras que elevam o ticket
- Bloco "Por que pré-moldado vs. alvenaria" (tempo, mão de obra, durabilidade), sem números inventados.
- Destaque de **peças sob medida para construtoras** com upload de projeto (PDF) → e-mail/WhatsApp.
- Botão "Salvar contato" (vCard) e QR code para material impresso/caminhões.
- Campanhas sazonais (ex.: safra → mourões) só se o cliente quiser: área de banner editável.

## Critérios de aceite
- Lighthouse mobile ≥ 85 em Performance e ≥ 95 em Acessibilidade e SEO (com o modo leve ativo em aparelho fraco).
- Nenhuma rolagem horizontal em 360 px; todo CTA com alvo ≥ 44 px.
- Todos os `[[CONFIRMAR]]` listados numa tabela final para o cliente responder.
- Testado em Chrome Android, Safari iOS e desktop; sem erros no console.

## Perguntas para o cliente (entregue junto)
Endereço e horário · cidades/raio de entrega · faz entrega e montagem? tem munck? · prazo médio de fabricação · formas de pagamento/parcelamento · lista real de produtos com medidas e pesos · fotos/vídeos de obras (de preferência drone ou time-lapse de montagem) · depoimentos autorizados · e-mail comercial · tem certificação/ensaios de resistência?
