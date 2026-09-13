# MNEMOSYNE SITE — Guia de Deploy e Descoberta Orgânica
## Gerado: Setembro 2026 | R$ 0,00 | Sem redes sociais

---

## 1. ESTRUTURA DO SITE

```
MNEMOSYNE_SITE/
├── index.html          ← Hub principal (seletor de idioma)
├── en/index.html       ← Página EN completa com SEO
├── pt/index.html       ← Página PT completa com SEO
├── es/index.html       ← Página ES completa com SEO
├── sitemap.xml         ← Sitemap multilíngue com hreflang
├── robots.txt          ← Permite todos os crawlers
└── DEPLOY_E_SEO.md     ← Este arquivo
```

---

## 2. O QUE ESTÁ IMPLEMENTADO EM CADA PÁGINA

### SEO Técnico (todas as páginas)
- `<title>` otimizado por idioma e obra
- `<meta name="description">` específico por idioma
- `<meta name="keywords">` com termos de busca reais
- `<link rel="canonical">` — URL canônica por idioma
- `<link rel="alternate" hreflang>` — 4 atributos por página (PT, EN, ES, x-default)
- Open Graph completo: og:type=book, og:title, og:description, og:image, og:url, og:locale, books:author, books:isbn
- Twitter Card: summary_large_image

### Schema.org / JSON-LD (todas as páginas)
- `@type: Book` com: name, author, isbn, numberOfPages, genre, description, about, offers (preços reais), isPartOf (série), sameAs (Amazon)
- `@type: Person` com @id único por idioma
- `@type: WebPage` com BreadcrumbList
- `@type: WebSite` (no hub index.html)

### Estrutura HTML Semântica
- `<main>`, `<section aria-labelledby>`, `<nav>`, `<footer>`
- Headings hierárquicos: H1 → H2 → H3
- `alt` descritivo em todas as imagens
- `loading="eager"` na imagem hero (LCP)
- Links internos entre PT, EN e ES em TODAS as páginas
- `rel="noopener"` em todos os links externos

### Conteúdo (100% canônico — sem invenção)
- Sinopse extraída da contracapa oficial
- Personagem: Henry Wallace
- Temas: memória, perda, luto, identidade, amor, consciência, humanidade
- Tagline oficial: "Algumas memórias merecem o tempo que pedem."
- Série: O Ciclo de Orfeu / The Orpheus Cycle / El Ciclo de Orpheus
- ASINs reais: B0HG6FXLR4 / B0HFZGMPYF / B0H7P51W4K / B0H7PBW5BQ / B0HHS6VQP8 / B0HGWGQFFC / B0HH1SZGDM
- ISBNs: EN HC 9798194153367 / ES HC 9798170326037
- Preços exatos de cada formato/idioma

---

## 3. DEPLOY — OPÇÕES GRATUITAS

### OPÇÃO A — GitHub Pages (RECOMENDADO, gratuito, domínio personalizado)
```bash
# 1. Crie conta em github.com (se não tiver)
# 2. Crie repositório: adrianogiannesin.github.io
# 3. Faça upload dos arquivos da pasta MNEMOSYNE_SITE
# 4. Em Settings → Pages → Source: main branch / root
# URL automática: https://adrianogiannesin.github.io
# Com domínio próprio: adicione CNAME com "adrianogiannesin.com"
```

### OPÇÃO B — Netlify (arraste a pasta, zero config)
```
1. Acesse netlify.com → Log in with GitHub
2. Arraste a pasta MNEMOSYNE_SITE para o painel
3. URL automática: algo-como.netlify.app
4. Em Domain settings → Add custom domain → adrianogiannesin.com
```

### OPÇÃO C — Cloudflare Pages (CDN global, gratuito)
```
1. dash.cloudflare.com → Pages → Create application
2. Conecte o repositório GitHub
3. Build: sem configuração (site estático puro)
```

---

## 4. DOMÍNIO — adrianogiannesin.com

**SUBSTITUA no site antes do deploy:**
Buscar e substituir `https://adrianogiannesin.com` pelo domínio real se for diferente.

**Onde registrar (baixo custo):**
- Namecheap: ~$10/ano
- Cloudflare Registrar: preço de custo (~$8/ano)
- Google Domains (via Squarespace): ~$12/ano

---

## 5. PÓS-DEPLOY — INDEXAÇÃO

### Google Search Console
1. Acesse search.google.com/search-console
2. Adicione propriedade: https://adrianogiannesin.com
3. Verifique propriedade (HTML tag ou DNS)
4. Vá em Sitemaps → Adicione: https://adrianogiannesin.com/sitemap.xml
5. Solicite indexação manual de cada URL (Inspecionar URL → Solicitar indexação)

### Bing Webmaster Tools
1. Acesse bing.com/webmasters
2. Adicione o site
3. Submeta o sitemap

### Google Rich Results Test
Valide o JSON-LD de cada página:
- https://search.google.com/test/rich-results?url=https://adrianogiannesin.com/en/
- https://search.google.com/test/rich-results?url=https://adrianogiannesin.com/pt/
- https://search.google.com/test/rich-results?url=https://adrianogiannesin.com/es/

---

## 6. DESCOBERTA ORGÂNICA — AÇÕES EXTERNAS (SEM REDES SOCIAIS)

### PRIORIDADE 1 — Amazon Author Central
URL: https://author.amazon.com
- Login com email KDP (admgiannesin@gmail.com)
- "Add a book" → adicionar todos os ASINs
- "Add biography" (use o texto da seção About the author do site)
- "Add photo" (foto profissional)
- Adicionar URL do site no perfil
- IMPACTO: aparece nas páginas de produto da Amazon — tráfego de alta intenção

### PRIORIDADE 2 — Goodreads Author Profile
URL: https://www.goodreads.com/author/show/71115304.Adriano_Giannesin
- Clicar "Is this you?" e reivindicar o perfil
- Adicionar biografia, foto, website
- Adicionar todos os livros das 3 edições
- IMPACTO: Goodreads é a maior rede de leitores do mundo

### PRIORIDADE 3 — BookBub Author Profile (gratuito)
URL: https://www.bookbub.com/partners/authors
- Criar perfil de autor gratuito
- Adicionar livros, bio, foto, website
- IMPACTO: BookBub tem milhões de leitores anglófonos ativos

### PRIORIDADE 4 — StoryGraph (alternativa ao Goodreads)
URL: https://www.thestorygraph.com
- Criar perfil de autor
- Adicionar obra
- IMPACTO: crescendo rapidamente entre leitores EN

### PRIORIDADE 5 — LibraryThing (PT+EN+ES)
URL: https://www.librarything.com
- Adicionar obra nas 3 edições
- IMPACTO: indexado pelo Google, comunidade de leitores séria

### PRIORIDADE 6 — WorldCat / OCLC
- A Amazon automaticamente alimenta muitos catálogos de bibliotecas
- Verificar se o livro aparece em worldcat.org após algumas semanas de publicação

---

## 7. CONTEÚDO ORGÂNICO — ESTRUTURA PRONTA PARA CRIAR

### Artigos evergreen que poderiam ser criadas como subpáginas do site:

| Título (EN) | Intenção de busca | Ligação com o livro |
|---|---|---|
| "What is the Mnemosyne myth?" | informacional | Nome da obra, mitologia grega |
| "Grief and memory in contemporary fiction" | informacional | Tema central |
| "Best literary fiction about loss" | comercial | Categoria do livro |
| "Orpheus myth in modern literature" | informacional | Série |
| "Books about consciousness and identity" | informacional | Projeto Orpheus |
| "Literary fiction about grief 2026" | comercial temporal | Ano de publicação |

### Artigos evergreen em PT:

| Título (PT) | Intenção |
|---|---|
| "Ficção literária sobre luto" | comercial |
| "Melhores romances brasileiros indie 2026" | comercial |
| "O mito de Orfeu na ficção contemporânea" | informacional |
| "Ficção sobre memória e identidade" | informacional |

---

## 8. LINKS INTERNOS — MAPA DE INTERLIGAÇÃO

```
index.html ←→ en/index.html
index.html ←→ pt/index.html
index.html ←→ es/index.html
en/index.html ←→ pt/index.html
en/index.html ←→ es/index.html
pt/index.html ←→ en/index.html
pt/index.html ←→ es/index.html
es/index.html ←→ en/index.html
es/index.html ←→ pt/index.html
```
Todas as interligações estão implementadas. ✓

---

## 9. VALIDAÇÃO — CHECKLIST PÓS-DEPLOY

- [ ] Google Search Console: propriedade verificada
- [ ] Sitemap submetido ao Google
- [ ] Sitemap submetido ao Bing
- [ ] Rich Results Test: Book schema válido em EN, PT, ES
- [ ] hreflang validado (hreflang.org/checker)
- [ ] Open Graph validado (opengraph.xyz)
- [ ] Imagens das capas carregando (Amazon CDN)
- [ ] Links de compra funcionando (todos os ASINs)
- [ ] Navegação entre idiomas funcionando
- [ ] Mobile: responsivo em 375px (testado)

---

## 10. PRÓXIMAS 5 AÇÕES DE MAIOR IMPACTO

| # | Ação | Onde | Impacto | Tempo |
|---|---|---|---|---|
| 1 | Deploy do site + Google Search Console | GitHub Pages + GSC | MUITO ALTO | 30 min |
| 2 | Reivindicar perfil Goodreads | goodreads.com | MUITO ALTO | 20 min |
| 3 | Configurar Author Central Amazon | author.amazon.com | MUITO ALTO | 30 min |
| 4 | Criar perfil BookBub (gratuito) | bookbub.com | ALTO | 15 min |
| 5 | Submeter sitemap ao Bing Webmaster | bing.com/webmasters | ALTO | 10 min |

---

*Site criado por Claude Sonnet 4.6 | Setembro 2026*
*Investimento: R$ 0,00*
*Conteúdo 100% canônico. Nenhuma informação inventada.*
