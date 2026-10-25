# PROJECT HANDOVER

> Documento iniciado em 2026-09-07 a partir do código, histórico Git e configurações. Revisto em 2026-09-25 durante a preparação para o Codex e a recuperação autorizada de sete ficheiros de media. O código prevalece sobre descrições contraditórias. As regras de trabalho estão em `AGENTS.md`; as melhorias aqui identificadas não ficam automaticamente autorizadas.

---

## 1. Visão geral do projeto

**Contacto WhatsApp em 2026-10-25:** O texto WhatsApp abre `https://wa.me/351927302779` numa nova aba para iniciar conversa; o número continua com ligação telefónica. Nenhuma mensagem é enviada automaticamente.

**Miniatura Videografia em 2026-10-25:** O cartão Videografia usa `Images/Videos/Video.mp4` como miniatura animada, em ciclo e sem som.

**Miniatura Branding em 2026-10-25:** Cartão Redes Sociais e Branding usa `Images/Videos/GRS&B.mp4` como vídeo de fundo, com autoplay, muted, loop e playsinline, mantendo o texto e o formato do cartão.

**Otimização para GitHub em 2026-10-25:** Original `Lote21.mp4` preservado localmente e ignorado no Git. Site usa `Lote21-web.mp4` em H.264/AAC, 1080 × 1920, com faststart. As eliminações locais preexistentes ficam fora do commit.

**Galeria de fotografia em 2026-10-25:** Galeria única com as 51 imagens de `Images/Galeria Atual/`, sem separação entre interiores, exteriores e drone. Novos ficheiros exigem atualização da lista estática.

**Galerias de plantas e renders em 2026-10-25:** Atualizadas as listas da galeria para os cinco ficheiros de `Images/PLANTAS/` (Planta Simples em primeiro lugar) e os 25 ficheiros de `Images/RENDERS 3D/`. Preservados separadores e miniatura do cartão; não foram movidos nem restaurados ficheiros.

**Vídeo AI Development em 2026-10-25:** Vídeo da respetiva pestana atualizado para `Images/Videos/Lote21-web.mp4`, com controlos nativos e reprodução manual com som ativado (sem autoplay nem muted). A reprodução pausa ao trocar de pestana ou fechar a galeria.

**Atualização Branding em 2026-10-25:** Pestana preenchida com formato vertical, descrição, três aplicações ideais e cinco itens incluídos da referência fornecida. Mantida a regra de omitir preços e o título maior e amarelo.

**Vídeo Showcase em 2026-10-25:** Adicionado `Images/Videos/SHOWCASE.mp4` à pestana Showcase, com controlos, reprodução manual e som ativado. Pausa ao trocar de pestana ou fechar a galeria.

**Atualização Showcase em 2026-10-25:** Pestana preenchida com formato horizontal, descrição, três aplicações ideais e cinco itens incluídos da referência fornecida, sem preços e mantendo o título amarelo e maior.

**Atualização em 2026-10-25:** Pestana AI Development preenchida segundo a referência fornecida: formato vertical ou horizontal, descrição, três aplicações ideais e cinco itens incluídos. Por indicação do utilizador, não apresentar preços no website, mesmo quando constem das referências. Todos os títulos de estilos de videografia usam o destaque do Cinematic: amarelo e 1,8 rem. Preservadas as restantes alterações locais e eliminações de media preexistentes.

**Atualização em 2026-10-24:** O website apresenta apenas a área de Marketing Imobiliário. A antiga área Comercial foi retirada da interface, navegação, formulário e código das galerias; os ficheiros de media continuam preservados. O cartão Video AI foi substituído por "Redes Sociais e Branding"; a galeria AI permanece separada, sem cartão de entrada.

**Localização confirmada em 2026-09-25:** `/Users/jorgeramos/Documents/Website Building folder`, com repositório Git próprio. Esta pasta e `/Users/jorgeramos/Documents/Kitchen APP` são irmãs; o website não está dentro de Kitchen APP. Não foram encontrados `AGENTS.md` nas pastas antecessoras. O `AGENTS.md` de Kitchen APP não é herdado por este website; as suas regras de SQLite, Excel, receitas e servidor Express pertencem ao outro projeto.

**Estado Git na preparação:** branch `main`, commit `a3c7e21`, alinhada com a referência local `origin/main` (sem `fetch`, pelo que não se verificou o remoto em tempo real). As sete eliminações locais inicialmente detetadas fora da área de preparação foram resolvidas por recuperação autorizada a partir do Git local (secção 7.1). Não restam eliminações ou modificações em ficheiros versionados. Este handover já era um ficheiro não acompanhado pelo Git; `AGENTS.md` foi criado nesta preparação e também permanece não acompanhado. Não há alterações preparadas para commit. Não foram feitos commits ou pushes. O código do website permanece inalterado; foram recuperados apenas os sete ficheiros de media autorizados.

**Nome do projeto:** SayCheese Fotografia — landing page institucional.

**Objetivo da aplicação:** Site de apresentação (one-page) para o negócio de fotografia/videografia de Jorge Ramos ("SayCheese Fotografia"), dedicado a Marketing Imobiliário: fotografia, videografia, visitas virtuais 360°, landing pages para imóveis, plantas 2D/3D e gestão de redes sociais/branding.

O objetivo funcional do site é gerar contactos/orçamentos (lead generation) através de um formulário de contacto, mostrando portfólio visual segmentado por categoria.

**Público-alvo:** Agências imobiliárias, promotores imobiliários, consultores imobiliários e proprietários na zona de Lisboa e arredores (ver zonas de atuação na secção de contacto).

**Funcionalidades principais:**
- Hero com imagem de fundo, animação de "bokeh" e headline de marketing.
- Barra de estatísticas com contadores animados (projetos, anos de experiência, satisfação, visitas virtuais).
- Secção de Serviços dedicada a Marketing Imobiliário, com cards de subserviços.
- Galerias em lightbox (imagens) e em "video gallery" (vídeos) abertas a partir dos cards de serviço.
- Links externos para exemplos reais: visita virtual (Metareal) e landing page de exemplo (Vercel).
- Secção "Sobre Mim", depoimentos de clientes, CTA band, e formulário de contacto ligado ao Formspree.
- Footer simples.

---

## 2. Stack tecnológica

- **Frontend:** HTML5 + CSS3 (inline, num único `<style>`) + JavaScript vanilla (sem framework, sem bundler). **Não usa Tailwind CSS** — o CSS é escrito à mão com custom properties (`:root` com variáveis de cor `--gold`, `--black`, etc.). O template de `CLAUDE.md` menciona Tailwind via CDN, mas não corresponde à implementação. A razão histórica dessa diferença não está documentada.
- **Linguagens:** HTML, CSS, JavaScript (ES6+, sem TypeScript).
- **Fontes:** Google Fonts — `Playfair Display` (display/serif, títulos) + `Inter` (sans, corpo de texto), carregadas via `<link>` para `fonts.googleapis.com`.
- **Base de dados:** Nenhuma. Site 100% estático, sem backend próprio.
- **Serviços externos:**
  - **Formspree** (`https://formspree.io/f/mojrlvoa`) — processa as submissões do formulário de contacto (envio de email), sem backend próprio.
  - **Unsplash** — imagem de stock usada como placeholder no hero (`images.unsplash.com`).
  - **Metareal** — plataforma externa de tour virtual 360°, link direto hardcoded (não hospedado neste projeto).
  - **Vercel** — hospeda um projeto separado (`real-estate-lp-rouge.vercel.app`) usado como exemplo de "Landing page para Real Estate"; não faz parte deste repositório.
- **APIs:** Nenhuma API própria. Formspree é consumido via `fetch()` (POST, `Accept: application/json`).
- **Autenticação:** Não existe (site público, sem login/áreas privadas).
- **Hosting/deployment:** **Não identificado nem configurado no repositório.** Não há `vercel.json`, `netlify.toml`, `CNAME`, GitHub Actions (`.github/workflows`) nem qualquer outro ficheiro de configuração de deploy. O repositório remoto é `https://github.com/jorsil1968/Site-ScheeseFotografia.git` (branch `main`). **Confirmar com o utilizador onde/como o site está atualmente publicado** (ex: GitHub Pages manual, upload FTP, outro serviço) — não há evidência disso no código.

**Ferramentas de desenvolvimento (auxiliares, não fazem parte do site publicado):**
- `puppeteer` (`package.json`, única dependência) — usado por `screenshot.mjs` para tirar screenshots do site em `localhost` durante o desenvolvimento (fluxo atualizado em `AGENTS.md`).
- `screenshot.mjs` — script Node standalone (40 linhas) que abre a página no Puppeteer, força elementos `.fade-up` a ficarem visíveis, faz scroll da página completa (para disparar `IntersectionObserver`s) e grava PNG em `./temporary screenshots/screenshot-N[-label].png`.
- **`serve.mjs` — referido em `CLAUDE.md` como o servidor local (`node serve.mjs`, porta 3000) mas o ficheiro NÃO existe no repositório.** A visualização funciona com o servidor estático Python descrito na secção 11; não é necessário criar este ficheiro.

---

## 3. Estrutura do projeto

```
/ (raiz)
├── index.html                # Toda a aplicação: markup + CSS + JS inline (1344 linhas)
├── package.json               # Só declara a dependência "puppeteer"
├── package-lock.json
├── screenshot.mjs             # Script de screenshot via Puppeteer (dev only)
├── AGENTS.md                  # Regras atuais de trabalho para o Codex
├── PROJECT_HANDOVER.md         # Contexto, estado e melhorias futuras
├── CLAUDE.md                  # Referência histórica do fluxo Claude Code
├── .gitignore
├── brand_assets/
│   └── Logos/                 # Logos oficiais da marca (PNG/JPG) — usar sempre estes, nunca placeholders
├── Images/                    # Biblioteca de media usada no site (≈1.1 GB)
│   ├── 3D/                    # Renders 3D de imóveis (perspetivas, plantas 3D mobiladas)
│   ├── Comercial/              # Fotos de espaços comerciais (escritórios, restaurantes)
│   ├── Fotos Drone/            # Fotografia aérea
│   ├── Fotos Imobiliário/      # Fotografia imobiliária, subdividida em:
│   │   ├── Interiores/, Exteriores/, Crepusculo/
│   │   ├── Cozinhas. e WCs/{Cozinhas, Casas de Banho}/
│   │   └── Design de Interiores/
│   ├── Pessoas/                # Fotos de perfil/depoimentos, logos de clientes
│   ├── Plantas/                # Plantas 2D e 3D
│   └── Videos/                 # Vídeos usados nos cards e na galeria Video AI (sete ficheiros recuperados; ver secção 7.1)
└── temporary screenshots/      # Output do screenshot.mjs (git-ignorado, não versionado)
```

**Responsabilidade de cada pasta:**
- `brand_assets/Logos/` — única fonte de verdade para logótipos (branco, preto, favicon). Regra do `CLAUDE.md`: verificar sempre esta pasta antes de usar placeholders.
- `Images/*` — biblioteca de conteúdo real do cliente (não são placeholders), referenciada diretamente por caminho relativo no `index.html` e nos objetos `galleries` em JavaScript.
- `temporary screenshots/` — artefactos de trabalho, nunca deve ser commitada (está no `.gitignore`).

**Ficheiros críticos:**
- `index.html` — o site inteiro. Qualquer alteração de design, copy, serviços ou galeria é feita aqui.
- `AGENTS.md` — regras atuais para o Codex, incluindo arquitetura, identidade visual, execução local e validação.
- `CLAUDE.md` — referência histórica preservada; contém instruções desatualizadas sobre servidor, caminhos Windows, Tailwind e uma skill que não estava disponível na sessão de migração.
- `.gitignore` — exclui `node_modules/`, `temporary screenshots/`, ficheiros `.DS_Store`, e dois vídeos específicos (`Moradia Alto do Lagoal PT.mp4`, `T3_Feijo.mov`) que nunca chegaram a ser versionados.

---

## 4. Arquitetura

**Fluxo da aplicação:** Site estático de página única. Não há routing — tudo é âncoras (`#services`, `#contact`, etc.) e `scroll-behavior: smooth`. Não há SSR/SSG, não há build step: o `index.html` é servido tal como está.

**Comunicação frontend/backend:** Não existe backend. A única "chamada de API" é o `fetch()` do formulário de contacto para o Formspree (`POST https://formspree.io/f/mojrlvoa`), tratado com feedback visual no próprio botão (estado "A enviar...", sucesso, erro) — ver `index.html:958-991`.

**Gestão de estado:** Nenhuma gestão de estado formal. Estado local em variáveis JS soltas no `<script>` final:
- `currentGallery` / `currentIndex` — controlam qual galeria de imagens e qual imagem está ativa no lightbox.
- Toggle de classes CSS (`.active`, `.open`, `.visible`) controla pestanas das galerias, lightboxes abertos/fechados e animações fade-up.
- `IntersectionObserver` (x2) — um para o contador animado da stats-bar, outro para as animações `.fade-up` ao scroll.

**Estrutura da base de dados:** N/A — não existe base de dados. Os dados das galerias são definidos em arrays de caminhos de imagem e objetos JavaScript no próprio `index.html`.

**Autenticação e permissões:** Não aplicável — não há autenticação, contas de utilizador nem áreas restritas.

**Componentes principais do JavaScript (dois blocos `<script>` no fim do `<body>`):**
1. **Script principal:** geração de bokeh no hero, nav sticky ao scroll, contagem animada das stats, fade-up on scroll e submissão do formulário de contacto.
2. **Script de galerias:** lightbox de imagens para Fotografia e Plantas/3D; galeria de Videografia com cinco estilos e descrições, ainda sem vídeos; galeria de vídeo "Video AI" separada (`#vgOverlay`) com três exemplos.

---

## 5. Funcionalidades já implementadas

A tabela descreve código implementado, não uma certificação de funcionamento. Os seis vídeos e a fotografia antes ausentes foram recuperados e validados (secção 7.1); o envio real do formulário e os serviços externos não foram testados nesta revisão.

| Funcionalidade | Estado |
|---|---|
| Hero com headline, badge de serviços, CTAs e animação de bokeh/light sweep | ✅ Completo |
| Nav fixa com efeito de scroll (fundo translúcido + blur) | ✅ Completo |
| Barra de estatísticas com contador animado (500+ projetos, 8+ anos, 98% satisfação, 100+ visitas virtuais) | ✅ Completo |
| Secção de Serviços dedicada a Marketing Imobiliário | ✅ Completo |
| Cards de subserviço com overlay de descrição on-hover (e sempre visível em touch, via `@media (hover:none)`) | ✅ Completo |
| Galeria de Fotografia (lightbox com tabs Interiores/Exteriores/Drone) | Implementada; imagem de exteriores recuperada |
| Galeria de Plantas e 3D (lightbox com tabs Plantas 2D+3D / Renders 3D) | ✅ Completo |
| Galeria de Videografia com cinco pestanas, sem vídeos por enquanto | ✅ Implementada |
| Área Comercial e galerias associadas | Removidas da interface; media preservado |
| Card "Redes Sociais e Branding" com ícone estático, sem autoplay | ✅ Implementado |
| Galeria "Video AI" com 3 exemplos | Preservada separadamente, sem cartão de entrada |
| Links externos para exemplo real de Visita Virtual (Metareal) e Landing Page (Vercel) | ✅ Completo |
| Secção "Sobre Mim" com foto, citação e biografia | ✅ Completo |
| Secção de Depoimentos (3 testemunhos reais com avatar, nome, cargo) | ✅ Completo |
| CTA band entre secções | ✅ Completo |
| Formulário de contacto (nome, email, área de interesse com optgroups, mensagem) ligado ao Formspree, com feedback de envio/erro | ✅ Completo |
| Footer com logo, copyright e links | ✅ Completo |
| Responsividade mobile (breakpoints 900px e 640px) | Parcial; menu oculto e grelhas com três colunas inline (secção 6) |
| Fluxo de screenshot/comparação via Puppeteer para QA visual | Script existente; usar servidor Python (secção 11); capturas não executadas nesta revisão |

---

## 6. Funcionalidades incompletas

- **Links de redes sociais** (`Instagram`, `Facebook`, `LinkedIn`, `Houzz` na secção de Contacto, `index.html:798-803`) apontam para `href="#"` — placeholders nunca preenchidos com os URLs reais dos perfis.
- **Nav mobile sem menu hambúrguer:** em `@media (max-width: 900px)` a regra `nav .nav-links { display: none; }` simplesmente esconde toda a navegação (incluindo o CTA "Pedir Orçamento") em ecrãs pequenos, sem qualquer alternativa (nem hambúrguer, nem CTA sticky). Os botões do hero e os separadores continuam disponíveis, mas não substituem todas as ligações do menu.
- **Grelhas em mobile:** as duas grelhas de serviços definem `grid-template-columns: repeat(3, 1fr)` em atributos `style`, sobrepondo-se à regra de duas colunas abaixo de 640 px.
- **Acessibilidade:** há cartões `div` clicáveis sem suporte equivalente de teclado e etiquetas do formulário sem associação explícita aos campos. Validar também foco nas galerias quando esta área for trabalhada.
- **SEO/Meta tags:** não há `<meta name="description">`, Open Graph (`og:*`), Twitter Card, `favicon` real (não há `<link rel="icon">` no `<head>`), `robots.txt` nem `sitemap.xml`. O `<title>` existe mas mais nada de SEO foi implementado.
- **Analytics/Pixel:** não há Google Analytics, GA4, Meta Pixel ou qualquer tracking de conversão instalado — a sua introdução é uma decisão futura, não um requisito acordado. Não foram inspecionadas métricas do alojamento ou da conta Formspree.
- **`lang="pt-BR"`** no `<html>` (`index.html:2`) mas todo o copy está em português europeu — inconsistência a corrigir para `pt-PT`.
- **Documentação antiga de execução:** `CLAUDE.md` refere `serve.mjs`, que não existe. Usar os comandos válidos da secção 11; a criação de um servidor Node é opcional.
- **Deployment/hosting:** nenhuma configuração de deploy foi encontrada no repositório (sem `vercel.json`, `netlify.toml`, GitHub Actions, etc.) — não está claro, a partir do código, onde/como o site está atualmente publicado em produção.

**Dependências:** esclarecer os perfis sociais e o alojamento com o utilizador antes de resolver os respetivos itens. A recuperação de media foi autorizada e concluída. O backlog não constitui autorização de implementação.

---

## 7. Bugs conhecidos

### 7.1 — Media recuperado do Git local (resolvido em 2026-09-25)

- **Estado anterior:** sete ficheiros apagados apenas no working tree (` D`), sem eliminações staged ou commitadas, ainda referenciados pelo website.
- **Intenção esclarecida:** o utilizador confirmou que não os eliminou intencionalmente e autorizou recuperar apenas os sete caminhos abaixo. A causa técnica da eliminação não foi determinada.
- **Origem:** blobs completos disponíveis no `HEAD` local, commit `a3c7e21`. Não foi necessário acesso à rede, Git LFS ou outro backup. Os objetos contêm dados binários reais, não ponteiros LFS nem ficheiros vazios.
- **Recuperação:** apenas os sete caminhos foram repostos no working tree, sem alterar o índice, o código, `AGENTS.md` ou outros ficheiros. Não houve commit ou push.

| Ficheiro recuperado | Tamanho exato (bytes) | Formato e resolução | Duração aproximada |
|---|---:|---|---:|
| `Images/Fotos Imobiliário/Exteriores/HC_Z62_0115.png` | 51841811 | PNG, 6048 × 4024 | — |
| `Images/Videos/CR_Moradia_Galiza_2.mp4` | 38045932 | H264, 1920 × 1080 | 158.53 s |
| `Images/Videos/LPEx.mp4` | 9151356 | H264, 1920 × 1080 | 45.52 s |
| `Images/Videos/Living_Big.mov` | 50061112 | H264, 1080 × 1920 | 29.75 s |
| `Images/Videos/Terreno.mov` | 43458802 | H264, 1080 × 1920 | 25.21 s |
| `Images/Videos/Timelapse construção.mov` | 50940294 | H264, 1080 × 1920 | 29.71 s |
| `Images/Videos/VTEx.mp4` | 30511201 | H264, 1920 × 1080 | 126.16 s |

- **Integridade:** 274 010 508 bytes recuperados no total. O hash Git de cada ficheiro recuperado corresponde exatamente ao respetivo blob em `HEAD`. `ffprobe` identificou os formatos e as dimensões; `ffmpeg -v error -xerror` descodificou integralmente a imagem e a faixa de vídeo de cada um dos seis vídeos, sem erros. As faixas de áudio foram identificadas, mas não submetidas a descodificação integral nesta verificação.
- **Referências do website:** nova verificação de 123 caminhos locais distintos em `index.html`, incluindo dados das galerias e caminhos com codificação URL: zero ficheiros ausentes. As referências existentes não precisaram de alterações.
- **Limites da validação:** não foi feita uma nova revisão visual no navegador nem verificada a reprodução em todos os browsers. As restantes pendências de interface e serviços externos mantêm-se.
- **Documentação preservada:** `AGENTS.md` mantém o registo datado do estado anterior à recuperação; consultar esta secção para o resultado posterior autorizado. Ambos os documentos continuam não acompanhados pelo Git.

### 7.2 — Atributos `id` duplicados nas tab-panes de serviços (resolvido em 2026-10-24)
- **Descrição:** As duas tab-panes declaravam atributos `id` duplicados. Ao simplificar a página para uma única área, a estrutura de tabs foi removida e a secção passou a ter apenas `id="services"`.
- **Estado:** Resolvido; já não existem tab-panes nem IDs duplicados associados a essas áreas.

### 7.3 — CSS morto da secção "Portfolio"
- **Descrição:** Existem ~30 linhas de CSS (`.portfolio`, `.portfolio-header`, `.portfolio-grid`, `.portfolio-item`, `.portfolio-label`, `.portfolio-overlay`, `.portfolio-plus` — `index.html:224-251`) sem markup correspondente no `<body>`. Segundo a mensagem do commit `a3c7e21`, a secção "Portfolio" foi removida da página (passou a ser acessível via o card de Fotografia), mas o CSS não foi limpo.
- **Gravidade:** Muito baixa (cosmético/manutenção). Não afeta o utilizador final, apenas aumenta o peso do CSS e pode confundir quem editar o ficheiro no futuro.
- **Solução:** Remover as regras `.portfolio*` não usadas, ou confirmar que não há intenção de reintroduzir essa secção.

### 7.4 — `serve.mjs` em falta
- **Descrição:** `CLAUDE.md` instrui a iniciar sempre `node serve.mjs` antes de tirar screenshots, mas este ficheiro não existe no repositório.
- **Impacto:** o comando antigo falha, mas não bloqueia a visualização nem as capturas quando se usa o servidor Python da secção 11.
- **Estado:** execução alternativa documentada em `AGENTS.md` e neste handover. `CLAUDE.md` foi preservado como referência histórica. Criar `serve.mjs` é uma melhoria opcional.

### 7.5 — Repositório Git com >1 GB de ficheiros binários de media
- **Descrição:** Na inspeção de 2026-09-25, `Images/` ocupa aproximadamente 1,1 GB e `.git` 1,4 GB. A biblioteca está (na sua maioria) versionada em Git, incluindo várias fotos de 10-50 MB e vídeos de 30-50 MB, tudo em commits normais (sem Git LFS).
- **Gravidade:** Média — não é um "bug" funcional, mas é uma dívida técnica séria: clones do repositório são lentos/pesados, e o histórico Git só cresce (eliminar ficheiros no futuro não reduz o `.git` sem reescrever histórico).
- **Solução recomendada:** Avaliar migração para Git LFS ou mover a biblioteca de media para um serviço externo (bucket S3/R2, Cloudinary, CDN de imagens) e manter no repositório só o necessário para desenvolvimento local.

---

## 8. Decisões técnicas importantes

- **Site estático de ficheiro único, sem framework/bundler.** Decisão implícita no próprio `CLAUDE.md` ("Single `index.html` file, all styles inline, unless user says otherwise") — prioriza simplicidade de deployment e edição direta sobre modularidade. Não há registo de uma rejeição explícita de frameworks; apenas se confirma que não foram usados.
- **CSS custom em vez de Tailwind**, apesar de o `CLAUDE.md` recomendar Tailwind via CDN por omissão para novos projetos frontend. A implementação usa a paleta de marca (`--gold #FFB800`, `--black #0a0a0a`, etc.) e Playfair Display + Inter. Preservar esta escolha; não foi estabelecida a cronologia relativamente à convenção de Tailwind.
- **Formspree em vez de backend próprio** para o formulário de contacto — evita ter de manter servidor/API só para receber emails de contacto. Trade-off aceite: dependência de serviço terceiro e o endpoint (`mojrlvoa`) fica hardcoded no HTML.
- **Galerias construídas como dados JS inline (arrays de paths)** em vez de, por exemplo, gerar a lista dinamicamente a partir de uma pasta (não é possível sem backend) ou usar um CMS headless. Decisão pragmática dado que o site é 100% estático e o número de imagens por categoria é gerido manualmente.
- **Vídeos de fundo em autoplay/muted/loop** nos cards de serviço em vez de imagens estáticas, para comunicar qualidade de produção de vídeo diretamente na grelha de serviços — trade-off consciente entre impacto visual e peso de página (vários MB por vídeo, sem otimização/compressão adicional nem lazy-loading dos `<video>`).
- **Exemplos reais em vez de mockups** para "Visitas Virtuais" e "Landing Pages" — em vez de construir uma demo fake, os cards abrem projetos reais já publicados (Metareal, Vercel), reduzindo trabalho duplicado e mostrando prova social real.

---

## 9. APIs e serviços externos

| Serviço | Finalidade | Onde está configurado | Variáveis de ambiente necessárias |
|---|---|---|---|
| **Formspree** | Receber submissões do formulário de contacto por email | `action="https://formspree.io/f/mojrlvoa"` em `index.html:806`; endpoint chamado via `fetch()` em `index.html:965` | Nenhuma (endpoint público hardcoded, sem chave de API no frontend) |
| **Google Fonts** | Servir `Playfair Display` e `Inter` | `<link>` tags em `index.html:7-9` | Nenhuma |
| **Unsplash** (`images.unsplash.com`) | Imagem de stock usada no fundo do hero | URL em `index.html` | Nenhuma |
| **Metareal** | Player de tour virtual 360° (link externo) | URL hardcoded em `index.html:614` (`onclick="window.open(...)"`) | Nenhuma — gerido fora deste projeto |
| **Vercel** (`real-estate-lp-rouge.vercel.app`) | Exemplo de landing page real (link externo, projeto separado) | URL hardcoded em `index.html:625` | N/A — repositório/projeto distinto, não gerido aqui |

Não há ficheiro `.env` nem qualquer gestão de variáveis de ambiente neste projeto — é expectável, dado que é 100% estático e não tem segredos/chaves privadas no cliente.

---

## 10. Base de dados

Não aplicável. Este projeto não tem base de dados, ORM, migrações nem regras de segurança/RLS — é um site estático sem persistência própria. Os "dados" (textos, arrays de imagens) vivem diretamente no `index.html`.

---

## 11. Execução local e publicação

### Visualização local

Não há build nem necessidade de instalar dependências para servir o website. Python 3 está disponível no ambiente inspecionado. Na raiz do projeto:

```bash
cd "/Users/jorgeramos/Documents/Website Building folder"
python3 -m http.server 8080 --bind 127.0.0.1
```

Manter o Terminal aberto e visitar `http://127.0.0.1:8080/`. Parar com `Ctrl+C`. Não usar `node serve.mjs`, `npm start` ou `npm run dev`: o ficheiro e esses scripts não existem.

Antes de iniciar outra instância, verificar a porta com `lsof -nP -iTCP:8080 -sTCP:LISTEN` e confirmar que o processo serve este projeto. Em 2026-09-25 foi iniciado um servidor Python nesta pasta e obtida resposta HTTP 200. Isto não garante que o processo continue ativo numa sessão futura. A porta 3000 estava ocupada por Real Estate - Villa Lumiere; não terminar servidores de outros projetos. Se 8080 estiver ocupada por outra aplicação, escolher uma porta livre e ajustar o URL.

Para confirmar a resposta:

```bash
curl --silent --show-error --output /dev/null --write-out '%{http_code}\n' http://127.0.0.1:8080/
```

Uma recusa de ligação normalmente significa que não há servidor acessível nessa porta. Se o ambiente restrito bloquear o arranque ou a verificação, pedir a permissão necessária; não confundir esse bloqueio com uma falha do website.

Quando a tarefa incluir validação visual, com Puppeteer e o navegador disponíveis:

```bash
node screenshot.mjs http://127.0.0.1:8080/ revisao
```

Este comando cria PNGs em `temporary screenshots/` (ignorada pelo Git). Usa 1440 × 900 e força `.fade-up` a ficar visível, pelo que não substitui testes de mobile, animações e interações. Os caminhos Windows de Puppeteer em `CLAUDE.md` não se aplicam a este ambiente. Google Fonts, Unsplash e serviços externos precisam de Internet; iniciar o servidor não recupera media eliminado.

### Publicação

- **Build:** Não há processo de build. `index.html` é servido tal como está; não há passo de minificação, bundling ou otimização de imagens.
- **Publicar:** **Não documentado no repositório.** Não existem ficheiros de configuração de nenhuma plataforma de hosting (Vercel, Netlify, GitHub Pages, Cloudflare Pages, etc.), nem workflows de CI/CD (`.github/workflows` não existe). O repositório está no GitHub (`jorsil1968/Site-ScheeseFotografia`, branch `main`), mas não há evidência de deployment automático a partir daí.
  - **Ação necessária:** confirmar com o utilizador onde o site está publicado atualmente (se está) e, se aplicável, documentar aqui o processo real (ex: "arrastar pasta para Netlify", "GitHub Pages ativado nas definições do repo", etc.).
- **Domínios:** O email de contacto usa o domínio `saycheese.pt` (`jorgeramos@saycheese.pt`), o que sugere que o domínio de produção destinado é `saycheese.pt` ou similar — não confirmado no código.
- **Variáveis necessárias:** Nenhuma (site estático, sem segredos).
- **Ambiente de produção:** Desconhecido/não configurado neste repositório.

---

## 12. Testes

- **Testes existentes:** Nenhum teste automatizado (unitário, integração ou E2E). O script `test` em `package.json` é apenas o placeholder gerado por omissão pelo `npm init` (`"echo \"Error: no test specified\" && exit 1"`).
- **Como executá-los:** N/A.
- **Cobertura:** não medida; não apresentar uma percentagem como resultado de testes.
- **Validação adequada:** seguir `AGENTS.md`; testar o comportamento afetado e comparar capturas em alterações visuais. Uma resposta HTTP 200 ou uma captura não garante o funcionamento das galerias, do formulário ou da versão móvel.
- **Revisão de 2026-09-25:** inspeção do código, Git e referências locais; recuperação e validação de media conforme secção 7.1; servidor local com HTTP 200. Sem submissões reais do formulário, testes de serviços externos ou validação visual completa.

---

## 13. Segurança

- **Autenticação:** Não existe (site público).
- **Permissões:** Não aplicável — não há papéis de utilizador.
- **Gestão de secrets:** Não há segredos no projeto. O único endpoint sensível é o ID do formulário Formspree, que é público por natureza (é assim que o Formspree funciona — o ID no HTML não concede acesso administrativo a mais ninguém).
- **Pontos sensíveis:**
  - O formulário de contacto não tem proteção anti-spam visível (sem honeypot, sem reCAPTCHA) — as proteções ativas na conta Formspree não foram verificadas; avaliar apenas quando este trabalho for solicitado.
  - Os emails de contacto e telefone (`jorgeramos@saycheese.pt`, `+351 927 302 779`) estão expostos em texto simples no HTML (`mailto:`/`tel:`), o que é normal para uma página de contacto pública mas facilita scraping por bots de spam.
  - Não há Content-Security-Policy nem outros headers de segurança configurados — dependeria da configuração do servidor/host onde o site for publicado (fora do âmbito deste repositório de ficheiros estáticos).

---

## 14. Roadmap

*(Nada foi formalmente planeado em documentação — o que se segue são lacunas identificadas nas secções 6 e 7 que fazem sentido priorizar, e não compromissos confirmados com o cliente.)*

**Prioridade alta:**
1. **Concluído:** recuperar os sete ficheiros de media a partir do Git local, com autorização do utilizador e verificação de integridade (secção 7.1).
2. Decidir e documentar onde/como o site é publicado em produção (secção 11).
3. Preencher os links reais de redes sociais (secção 6).

**Prioridade média:**
4. Adicionar meta tags de SEO (description, Open Graph, favicon real) e corrigir `lang="pt-BR"` → `pt-PT`.
5. Resolver a navegação mobile, a sobreposição das regras da grelha e a acessibilidade dos controlos.
6. Opcionalmente simplificar os comandos de desenvolvimento. A execução com Python já está documentada e não depende de criar `serve.mjs`.
7. Avaliar Git LFS ou hosting externo de media para reduzir o peso do repositório.

**Prioridade baixa:**
8. Limpar CSS morto da secção Portfolio (secção 7.3).
9. Considerar analytics (GA4 ou alternativa) para medir tráfego e conversões do formulário.

---

## 15. Contexto histórico

Histórico inicial reconstruído a partir dos commits; a preparação de 2026-09-25 está registada abaixo sem novo commit:

1. **`3b7d125` — "SayCheese Fotografia — landing page completa"** (commit inicial, 203 ficheiros): criação de toda a estrutura do site — `index.html`, toda a biblioteca `Images/`, `brand_assets/`, `package.json` e `screenshot.mjs`. O site nasceu já como página completa, não incrementalmente a partir de um esqueleto.
2. **`bd75555` — "Formulário de contacto ligado ao Formspree"**: o formulário de contacto foi ligado ao Formspree depois da estrutura inicial existir — ou seja, inicialmente o formulário provavelmente não submetia para lado nenhum (ou usava outro método), e foi corrigido/finalizado neste commit (+37/-13 linhas em `index.html`).
3. **`2491379` — "Melhorar legibilidade mobile nos cards de serviços e atualizar texto Landing pages"** (co-autorado com Claude Sonnet 4.6): identificou-se que em dispositivos touch o hover não existe, logo o overlay de descrição dos cards de serviço nunca aparecia em mobile — corrigido com a media query `@media (hover: none)` que força o overlay/descrição a estarem sempre visíveis em touch. Também foi atualizado o copy do card "Landing pages para Real Estate".
4. **`a3c7e21` — "Adicionar serviço Video AI, galeria de fotografia e melhorias de UX"** (co-autorado com Claude Sonnet 4.6, o commit mais recente e mais substancial: +225/-65 em `index.html`, +3 vídeos grandes):
   - Introduziu o novo serviço **Video AI** (badge "Novo Serviço", vídeo de fundo `Terreno.mov`, glow animado via `aiGlow`/`ai-overlay-scan`) com uma galeria de vídeo dedicada com 3 exemplos (Construction Timelapse, Living Experience, Localization).
   - Transformou o card "Fotografia" num trigger de galeria com tabs (Interiores/Exteriores/Drone), abrindo ao clicar.
   - **Removeu a secção "Portfolio" como secção própria da página** — o acesso ao portfólio passou a ser feito através do card de Fotografia (ver bug 7.3 — o CSS antigo do Portfolio ficou para trás).
   - Reorganizou os cards de Marketing Imobiliário em 2 linhas de 3 (grid `repeat(3, 1fr)`).
   - Fez "Landing pages" e "Visitas Virtuais" abrirem exemplos reais em nova aba, em vez de serem apenas cards informativos — decisão de mostrar prova social real em vez de mockups (ver secção 8).

5. **2026-09-25 — preparação para o Codex, sem commit:** criado `AGENTS.md` específico do website e revisto este handover. Confirmadas a localização independente de Kitchen APP, as sete eliminações não staged e a execução local por Python. Preservados código, configurações, media e histórico. Este handover era preexistente e não acompanhado; ambos os documentos permanecem fora do histórico até eventual autorização de commit.

6. **2026-09-25 — recuperação autorizada de media, sem commit:** o utilizador esclareceu que as eliminações não eram intencionais. Recuperados os sete blobs completos de `HEAD`, com igualdade de hashes e descodificação da imagem e dos vídeos sem erros. As 123 referências locais passaram a estar disponíveis. Preservados código, `AGENTS.md` e restantes ficheiros; atualizado apenas este handover além dos sete caminhos recuperados.

**Padrão observado:** as duas últimas alterações substanciais foram feitas em colaboração com Claude (Sonnet 4.6), o que indica que este handover deverá ser mantido atualizado à medida que novas sessões de IA continuarem o trabalho — antes do handover inicial não foram encontradas notas de sessões; o contexto passa agora a estar registado neste documento e as regras em `AGENTS.md`.

**Não documentado em lado nenhum (a esclarecer com o utilizador, Jorge Ramos):**
- Onde o site está efetivamente publicado hoje (se está).
- Se existe algum feedback de clientes reais sobre o site (taxa de conversão do formulário, etc.) que deva influenciar prioridades futuras.

---

## 16. Instruções para outro agente/programador

- Ler `AGENTS.md` como referência de trabalho do Codex e este handover como contexto. O pedido do utilizador define o âmbito autorizado; o backlog não autoriza alterações por si só.
- Preservar `CLAUDE.md` como contexto histórico. Não reproduzir os comandos inválidos, os caminhos Windows ou a dependência obrigatória da skill `frontend-design`. Não introduzir Tailwind para cumprir o template antigo.
- Preservar a arquitetura estática, os logótipos reais, a paleta e a tipografia. Manter português de Portugal; não inventar testemunhos, estatísticas ou promessas comerciais.
- Manter as convenções de classes (`sub-card`, `lb-*`, `vg-*`, `area-*`), os dados em `galleries`/`galleryConfigs` e `autoplay muted loop playsinline` nos vídeos de fundo, salvo alteração solicitada.
- O site não cumpre integralmente todas as orientações visuais antigas: existem transições de propriedades além de `transform` e `opacity`, incluindo `max-height`, e lacunas de foco/acessibilidade. Tratar isto como estado conhecido, não como autorização para uma reformulação global.
- Verificar o estado Git antes e depois do trabalho. Preservar alterações preexistentes e ficheiros não acompanhados. Não restaurar, preparar ou confirmar as eliminações de media sem autorização específica; não fazer commit ou push sem pedido do utilizador.
- Usar os comandos da secção 11. Validar o comportamento afetado e mobile quando houver alterações de interface; não enviar contactos reais só para testar. Comunicar o que foi e não foi validado.
- Atualizar o handover após mudanças significativas, conservando contexto válido e distinguindo observações datadas de regras permanentes.
