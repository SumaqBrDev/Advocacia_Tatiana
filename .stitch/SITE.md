# Brief de Build — Advocacia Tatiana de Oliveira
## Para uso em: Antigravity / Claude Code
## Tipo: Landing Page Profissional — Idioma: Português PT-BR
## Estilo: Sério · Dinâmico · Autoridade Jurídica · Elegância Premium
## Skills: design-taste-frontend + page-cro + copywriting + marketing-psychology + seo-audit
## Data: 2026

---

## PROMPT PRINCIPAL PARA ANTIGRAVITY

```
Construa uma Landing Page profissional, séria e elegante para a Dra. Tatiana de Oliveira,
advogada especialista em Direito de Família, Civil e do Consumidor, localizada em
Pomerode, SC, Brasil. 15 anos de experiência.

ESTÉTICA: "Lex Aurea" — Bordô profundo (#6B1A2C) como cor âncora de autoridade jurídica.
Dourado champagne (#C9A96E) como accent de distinção e premium. Preto profundo (#0F0F0F)
nos fundos hero e footer. Branco quente (#FAF8F5) nas seções de leitura. Tipografia
serifa elegante (Cormorant Garamond) nos títulos, Raleway nos subtítulos, Lato no corpo.

SENSAÇÃO: Entrar no site deve transmitir "Estou em boas mãos. Esta advogada sabe o que faz."
Sério sem ser frio. Elegante sem ser inacessível. Feminino profissional — não rosé, não
corporativo sem personalidade.

Stack: HTML5 + CSS3 + JavaScript Vanilla. Zero dependências externas exceto Google Fonts.
Otimizado para performance (Core Web Vitals), SEO local (Pomerode/SC) e conversão
(consulta via WhatsApp como CTA primário).

Siga rigorosamente os JSON de conteúdo e os design tokens abaixo.
```

---

## SKILLS A ATIVAR

### De `coreyhaines31/marketingskills`:
```
page-cro              Hierarquia visual para conversão: hero → prova social → áreas → CTA
copywriting           Copy jurídico confiante e humanizado — PT-BR, tom de autoridade
signup-flow-cro       Fluxo: consulta WhatsApp ou formulário — mínimo atrito
marketing-psychology  Prova social (15 anos, depoimentos), autoridade (OAB), urgência (vagas)
site-architecture     Estrutura de landing page com âncoras e scroll contínuo
seo-audit             Schema LegalService + Person, meta tags locais Pomerode/SC
```

### De `sickn33/antigravity-awesome-skills`:
```
design-taste-frontend Design premium editorial: serifa + sans, tokens, motion refinado
gpt-taste             Hero AIDA: headline aspiracional + sub + CTA duplo + credencial
performance-marketer  WhatsApp como CTA primário, formulário como secundário
seo-audit             Schema JSON-LD LegalService, Open Graph, canonical
```

---

## ARQUITETURA DO PROJETO

```
advocacia-tatiana/
├── index.html              # Landing Page completa (single-page com âncoras)
│
├── css/
│   ├── tokens.css          # Design tokens completos
│   ├── reset.css           # Normalize + box-sizing
│   ├── layout.css          # Sections, container, grid utils
│   ├── components.css      # Navbar, cards, botões, forms, FAQ, footer
│   ├── animations.css      # Keyframes, reveal classes, transitions
│   └── main.css            # @import de todos
│
├── js/
│   ├── navbar.js           # Scroll behavior: branco → bordô, mobile menu
│   ├── counter.js          # Animação de números nas stats
│   ├── faq.js              # Acordeão FAQ
│   ├── form.js             # Validação + envio WhatsApp/email
│   ├── reveal.js           # Intersection Observer scroll reveal
│   └── main.js             # Inicializa todos os módulos
│
├── assets/
│   ├── foto-tatiana.jpg           # Foto profissional (FORNECER — alta resolução)
│   ├── foto-tatiana-sobre.jpg     # Foto secundária para seção Sobre (opcional)
│   ├── og-image.jpg               # Open Graph 1200x630
│   └── favicon.ico                # Balança ou inicial "T"
│
├── robots.txt
└── sitemap.xml
```

---

## DESIGN SYSTEM — tokens.css

```css
:root {
  /* ─── MARCA JURÍDICA ─── */
  --bordeaux:          #6B1A2C;   /* primário — autoridade, tradição */
  --bordeaux-hover:    #8B2238;   /* estados hover */
  --bordeaux-deep:     #4A1020;   /* gradientes escuros, hero accent */
  --bordeaux-glow:     rgba(107, 26, 44, 0.35);
  --bordeaux-subtle:   rgba(107, 26, 44, 0.08);

  --gold:              #C9A96E;   /* dourado champagne — distinção */
  --gold-light:        #E8C99A;   /* dourado claro — hover, ícones */
  --gold-subtle:       rgba(201, 169, 110, 0.15);
  --gold-border:       rgba(201, 169, 110, 0.25);

  /* ─── NEUTROS ─── */
  --black-deep:        #0F0F0F;   /* hero, footer */
  --black-surface:     #1C1C1C;   /* cards em fundo escuro */
  --black-raised:      #252525;   /* cards hover, dropdowns */
  --white-warm:        #FAF8F5;   /* fundos claros — nunca branco frio */
  --gray-border:       #E8E4DF;   /* separadores em seções claras */
  --gray-text:         #5A5A5A;   /* texto corpo em fundo claro */
  --gray-muted:        #8A8A8A;   /* texto secundário, placeholders */

  /* ─── TEXTO ─── */
  --text-light:        #FFFFFF;
  --text-gold:         #C9A96E;
  --text-dark:         #1A1A1A;

  /* ─── TIPOGRAFIA ─── */
  --font-serif:    'Cormorant Garamond', Georgia, serif;
  --font-heading:  'Raleway', sans-serif;
  --font-body:     'Lato', sans-serif;

  --fw-light:      300;
  --fw-regular:    400;
  --fw-semi:       600;
  --fw-bold:       700;

  /* Escala fluida */
  --fs-hero:   clamp(2.8rem, 6.5vw, 5.5rem);
  --fs-h1:     clamp(2.4rem, 5vw, 4.5rem);
  --fs-h2:     clamp(1.8rem, 3vw, 2.8rem);
  --fs-h3:     clamp(1.1rem, 1.8vw, 1.4rem);
  --fs-body:   1rem;             /* 16px base */
  --fs-sm:     0.875rem;
  --fs-xs:     0.75rem;

  --ls-tight:   -0.03em;
  --ls-normal:   0;
  --ls-wide:     0.06em;
  --ls-widest:   0.18em;

  /* ─── ESPAÇAMENTO ─── */
  --section-pad:    clamp(64px, 9vw, 128px);
  --container-max:  1200px;
  --container-pad:  clamp(20px, 5vw, 60px);
  --gap-sm:         16px;
  --gap-md:         28px;
  --gap-lg:         48px;
  --gap-xl:         72px;

  /* ─── RADII ─── */
  --radius-sm:   3px;
  --radius-md:   6px;
  --radius-lg:   12px;
  --radius-pill: 100px;

  /* ─── SOMBRAS ─── */
  --shadow-card:      0 2px 20px rgba(0,0,0,0.12);
  --shadow-card-dark: 0 4px 32px rgba(0,0,0,0.5);
  --shadow-gold:      0 0 24px rgba(201,169,110,0.20);
  --shadow-bordeaux:  0 4px 24px rgba(107,26,44,0.30);

  /* ─── ANIMAÇÕES ─── */
  --ease-elegant:  cubic-bezier(0.25, 0.46, 0.45, 0.94);
  --ease-spring:   cubic-bezier(0.34, 1.56, 0.64, 1);
  --dur-fast:      0.18s;
  --dur-normal:    0.35s;
  --dur-slow:      0.65s;
  --dur-reveal:    0.75s;

  /* ─── BORDAS ─── */
  --border-gold:     1px solid var(--gold-border);
  --border-subtle:   1px solid rgba(255,255,255,0.07);
  --border-warm:     1px solid var(--gray-border);
  --accent-line:     3px solid var(--gold);  /* linha dourada decorativa */
}
```

---

## JSON DE CONTEÚDO — data.js

```javascript
// Incorporar diretamente no <script> do HTML ou arquivo separado
window.TATIANA_DATA = {

  lawyer: {
    name: "Dra. Tatiana de Oliveira",
    title: "Advogada | OAB/SC",
    tagline: "Advocacia com Seriedade e Compromisso",
    experience_years: 15,
    specialty: "Direito de Família",
    areas: ["Direito de Família", "Direito Civil", "Direito do Consumidor"],
    description: [
      "Advogada inscrita na OAB/SC há 15 anos, a Dra. Tatiana de Oliveira construiu sua trajetória em Pomerode com base em três princípios: seriedade jurídica, compromisso com o cliente e resultados reais.",
      "Especialista em Direito de Família, atua com excelência também nas áreas Cível e do Consumidor — áreas que tocam diretamente a vida cotidiana das pessoas.",
      "Cada caso é tratado com atenção individualizada. Porque para quem está passando por um momento difícil, ter ao lado uma advogada de confiança faz toda a diferença."
    ]
  },

  contact: {
    whatsapp_number: "[CONFIRMAR COM CLIENTE]",
    whatsapp_link: "https://wa.me/55[CONFIRMAR]",
    email: "[CONFIRMAR COM CLIENTE]",
    address: "[CONFIRMAR COM CLIENTE] — Pomerode, SC",
    city: "Pomerode",
    state: "SC",
    zip: "89107-000",
    maps_link: "https://maps.app.goo.gl/hE6qXoeJZjj93mMs9",
    instagram: "https://www.instagram.com/dra.tatiana_advogada/",
    facebook: "https://www.facebook.com/tatiadv",
    hours: "Segunda a Sexta: 09h–18h | Atendimento remoto disponível"
  },

  hero: {
    badge: "⚖️ OAB/SC · Pomerode, SC",
    headline: "Seus Direitos Merecem Uma Defesa à Altura",
    sub: "15 anos de experiência em Direito de Família, Civil e do Consumidor. Atendimento humanizado, estratégia jurídica séria.",
    cta_primary: "AGENDAR CONSULTA",
    cta_secondary: "Ver Áreas de Atuação"
  },

  stats: [
    { value: 15,   suffix: " anos",  label: "de Experiência Jurídica" },
    { value: 3,    suffix: "",       label: "Áreas de Especialização" },
    { value: 100,  suffix: "%",      label: "Sigilo e Ética Profissional" },
    { value: 314,  suffix: "+",      label: "Clientes Atendidos em Pomerode" }
  ],

  practice_areas: [
    {
      id: "familia",
      icon: "⚖️",
      title: "Direito de Família",
      badge: "Especialidade Principal",
      is_specialty: true,
      services: [
        "Divórcio consensual e litigioso",
        "Guarda e convivência familiar",
        "Pensão alimentícia",
        "Inventário e partilha de bens",
        "União estável",
        "Adoção"
      ],
      description: "Especialidade principal da Dra. Tatiana, com 15 anos de atuação nas questões mais sensíveis da vida familiar."
    },
    {
      id: "civil",
      icon: "📄",
      title: "Direito Civil",
      badge: null,
      is_specialty: false,
      services: [
        "Contratos e rescisão contratual",
        "Responsabilidade civil e indenizações",
        "Questões imobiliárias",
        "Cobranças e execuções",
        "Revisão de dívidas"
      ],
      description: "Atuação sólida nas questões cíveis que afetam pessoas físicas e jurídicas no dia a dia."
    },
    {
      id: "consumidor",
      icon: "🛡️",
      title: "Direito do Consumidor",
      badge: null,
      is_specialty: false,
      services: [
        "Cobranças indevidas e negativação",
        "Produtos defeituosos",
        "Propaganda enganosa",
        "Cancelamento de contratos abusivos",
        "Ação em Procon e judicialmente"
      ],
      description: "Defesa dos direitos do consumidor com eficiência e conhecimento da legislação vigente."
    }
  ],

  process_steps: [
    {
      number: "01",
      title: "Consulta Inicial",
      icon: "💬",
      text: "Entre em contato pelo WhatsApp ou formulário. A Dra. Tatiana analisa seu caso de forma confidencial e sem compromisso."
    },
    {
      number: "02",
      title: "Análise e Estratégia",
      icon: "🔍",
      text: "Avaliação detalhada da sua situação jurídica e elaboração da melhor estratégia para o seu caso."
    },
    {
      number: "03",
      title: "Defesa e Resultado",
      icon: "⚖️",
      text: "Acompanhamento completo do processo. Você é informado em cada etapa, sem surpresas e com total transparência."
    }
  ],

  testimonials: [
    {
      text: "A Dra. Tatiana me orientou em um processo de divórcio muito delicado. Foi profissional, humana e sempre clara sobre cada passo. Sinto que meus direitos foram verdadeiramente defendidos.",
      author: "M.S.",
      city: "Pomerode, SC",
      area: "Direito de Família",
      stars: 5
    },
    {
      text: "Tive um problema sério com um produto defeituoso e não sabia como agir. A Dra. Tatiana resolveu tudo em poucas semanas. Recomendo sem hesitar.",
      author: "R.K.",
      city: "Blumenau, SC",
      area: "Direito do Consumidor",
      stars: 5
    },
    {
      text: "Questão de guarda dos filhos — o momento mais difícil da minha vida. A Dra. Tatiana foi firme quando precisou e humana sempre. Resultado excelente.",
      author: "F.O.",
      city: "Pomerode, SC",
      area: "Direito de Família",
      stars: 5
    }
  ],

  faq: [
    {
      q: "A consulta inicial tem custo?",
      a: "Entre em contato pelo WhatsApp para verificar as condições de atendimento e agendar sua consulta inicial."
    },
    {
      q: "A Dra. Tatiana atende fora de Pomerode?",
      a: "Sim. Atendimentos presenciais em Pomerode/SC e consultoria remota para toda Santa Catarina e demais estados."
    },
    {
      q: "Quanto tempo leva um processo?",
      a: "O prazo varia conforme a complexidade. Em Direito de Família, acordos podem ser resolvidos em semanas; processos litigiosos levam meses ou mais. A Dra. Tatiana orienta sobre cada caso individualmente."
    },
    {
      q: "O que devo levar para a primeira consulta?",
      a: "Documentos pessoais (RG, CPF) e documentos relacionados ao caso (contratos, certidão de casamento, notas fiscais, etc.). A Dra. Tatiana orienta sobre o que for necessário."
    },
    {
      q: "Como funciona o sigilo das informações?",
      a: "O sigilo é absoluto e garantido pelo Código de Ética da OAB. Todas as informações compartilhadas são protegidas integralmente pelo segredo profissional."
    }
  ],

  form: {
    areas_select: [
      "Direito de Família",
      "Direito Civil",
      "Direito do Consumidor",
      "Outra área"
    ],
    whatsapp_template: "Olá, Dra. Tatiana! Meu nome é {nome} e gostaria de uma consulta sobre {area}. {mensagem}"
  },

  seo: {
    title: "Dra. Tatiana de Oliveira | Advogada em Pomerode SC — Família, Civil e Consumidor",
    description: "Advogada há 15 anos em Pomerode/SC. Especialista em Direito de Família. Excelência em Direito Civil e do Consumidor. Atendimento humanizado, OAB/SC. Agende sua consulta.",
    keywords: "advogada pomerode sc, direito de família pomerode, advocacia pomerode, advogada civil consumidor sc, tatiana de oliveira advogada, dra tatiana advogada pomerode",
    schema: {
      "@context": "https://schema.org",
      "@type": "LegalService",
      "name": "Advocacia Tatiana de Oliveira",
      "description": "Escritório de advocacia especializado em Direito de Família, Direito Civil e Direito do Consumidor. Pomerode, SC.",
      "url": "[URL do site — confirmar domínio]",
      "telephone": "[CONFIRMAR]",
      "email": "[CONFIRMAR]",
      "address": {
        "@type": "PostalAddress",
        "addressLocality": "Pomerode",
        "addressRegion": "SC",
        "postalCode": "89107-000",
        "addressCountry": "BR"
      },
      "geo": {
        "@type": "GeoCoordinates",
        "latitude": -26.7445,
        "longitude": -49.1757
      },
      "openingHoursSpecification": [
        {
          "@type": "OpeningHoursSpecification",
          "dayOfWeek": ["Monday","Tuesday","Wednesday","Thursday","Friday"],
          "opens": "09:00",
          "closes": "18:00"
        }
      ],
      "knowsAbout": ["Direito de Família", "Direito Civil", "Direito do Consumidor"],
      "sameAs": [
        "https://www.instagram.com/dra.tatiana_advogada/",
        "https://www.facebook.com/tatiadv"
      ]
    }
  }
};
```

---

## ESTRUTURA HTML COMPLETA — index.html

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- SEO -->
  <title><!-- JS injeta do data.seo.title --></title>
  <meta name="description" content="<!-- JS injeta -->">
  <meta name="keywords" content="<!-- JS injeta -->">
  <link rel="canonical" href="[URL]">

  <!-- Open Graph -->
  <meta property="og:type" content="website">
  <meta property="og:title" content="Dra. Tatiana de Oliveira — Advogada Pomerode SC">
  <meta property="og:description" content="15 anos de experiência. Direito de Família, Civil e Consumidor.">
  <meta property="og:image" content="assets/og-image.jpg">
  <meta property="og:url" content="[URL]">

  <!-- Schema JSON-LD -->
  <script type="application/ld+json"><!-- JS injeta do data.seo.schema --></script>

  <!-- Preloads críticos -->
  <link rel="preload" as="image" href="assets/foto-tatiana.jpg">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;0,700;1,400;1,700&family=Raleway:wght@300;400;500;600;700&family=Lato:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">

  <!-- CSS -->
  <link rel="stylesheet" href="css/main.css">
  <link rel="icon" href="assets/favicon.ico">
</head>

<body>

  <!-- SKIP LINK -->
  <a href="#main-content" class="skip-link">Ir para o conteúdo principal</a>

  <!-- ═══════════════════════════════════════ NAVBAR -->
  <header id="navbar" role="banner">
    <div class="container navbar__inner">
      <a href="#hero" class="navbar__brand" aria-label="Advocacia Tatiana de Oliveira — Início">
        <span class="navbar__name">Dra. Tatiana de Oliveira</span>
        <span class="navbar__subtitle">Advocacia</span>
      </a>

      <nav aria-label="Menu principal">
        <ul class="navbar__links" role="list">
          <li><a href="#sobre">Sobre</a></li>
          <li><a href="#areas">Áreas de Atuação</a></li>
          <li><a href="#processo">Como Funciona</a></li>
          <li><a href="#contato">Contato</a></li>
        </ul>
      </nav>

      <a href="#contato" class="btn btn--primary btn--sm navbar__cta">
        Agendar Consulta
      </a>

      <button class="navbar__hamburger" aria-label="Abrir menu" aria-expanded="false">
        <span></span><span></span><span></span>
      </button>
    </div>

    <!-- Mobile drawer -->
    <div class="navbar__drawer" aria-hidden="true">
      <ul role="list">
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#areas">Áreas de Atuação</a></li>
        <li><a href="#processo">Como Funciona</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
      <a href="[WHATSAPP]" class="btn btn--whatsapp">💬 WhatsApp</a>
    </div>
  </header>

  <!-- ═══════════════════════════════════════ MAIN -->
  <main id="main-content">

    <!-- ── HERO ── -->
    <section id="hero" class="hero" aria-labelledby="hero-headline">
      <div class="hero__bg">
        <!-- Granulado noise via SVG filter ou CSS -->
      </div>
      <!-- Decorativo § -->
      <span class="hero__watermark" aria-hidden="true">§</span>

      <div class="container hero__inner">
        <!-- Texto (esquerda) -->
        <div class="hero__content">
          <div class="hero__badge reveal-item">
            <!-- data.hero.badge injetado por JS -->
          </div>
          <h1 id="hero-headline" class="hero__title reveal-item" style="--delay: 0.1s">
            <!-- data.hero.headline injetado por JS -->
          </h1>
          <p class="hero__sub reveal-item" style="--delay: 0.25s">
            <!-- data.hero.sub injetado por JS -->
          </p>
          <div class="hero__ctas reveal-item" style="--delay: 0.4s">
            <a href="[WHATSAPP]" class="btn btn--primary btn--lg" target="_blank" rel="noopener">
              <!-- data.hero.cta_primary -->
            </a>
            <a href="#areas" class="btn btn--outline-light">
              <!-- data.hero.cta_secondary --> ↓
            </a>
          </div>
        </div>

        <!-- Foto (direita) -->
        <div class="hero__photo reveal-right">
          <img src="assets/foto-tatiana.jpg"
               alt="Dra. Tatiana de Oliveira — Advogada especialista em Direito de Família em Pomerode SC"
               width="540" height="680" fetchpriority="high">
          <div class="hero__photo-line" aria-hidden="true"></div>
        </div>
      </div>

      <!-- Seta scroll -->
      <a href="#stats" class="hero__scroll-arrow" aria-label="Ver mais">
        <svg><!-- seta SVG animada --></svg>
      </a>
    </section>

    <!-- ── STATS / CREDIBILIDADE ── -->
    <section id="stats" class="stats" aria-label="Números de experiência">
      <div class="container stats__grid">
        <!-- Renderizado por JS a partir de data.stats[] -->
        <!-- Cada item: <div class="stat-item"><span class="stat-value" data-target="15">0</span><span class="stat-suffix"> anos</span><p class="stat-label">de Experiência Jurídica</p></div> -->
      </div>
    </section>

    <!-- ── SOBRE ── -->
    <section id="sobre" class="about section-light" aria-labelledby="sobre-title">
      <div class="container about__inner">
        <div class="about__photo">
          <img src="assets/foto-tatiana.jpg"
               alt="Dra. Tatiana de Oliveira em seu escritório de advocacia em Pomerode SC"
               width="480" height="600" loading="lazy">
          <div class="about__photo-accent" aria-hidden="true"></div>
        </div>
        <div class="about__content reveal-up">
          <span class="section-label">Quem é a Dra. Tatiana</span>
          <h2 id="sobre-title">
            <!-- data.lawyer.name --> —
            <em><!-- data.lawyer.experience_years --> anos de advocacia em Pomerode</em>
          </h2>
          <!-- data.lawyer.description[] parágrafos -->
          <div class="about__credentials">
            <!-- ícones + credenciais: OAB/SC, 15 anos, Pomerode/SC -->
          </div>
          <a href="#contato" class="btn btn--bordeaux">Fale Comigo Agora →</a>
        </div>
      </div>
    </section>

    <!-- ── ÁREAS DE ATUAÇÃO ── -->
    <section id="areas" class="practice-areas section-dark" aria-labelledby="areas-title">
      <div class="container">
        <div class="section-header reveal-up">
          <span class="section-label section-label--gold">Atuação</span>
          <h2 id="areas-title">Áreas de Atuação</h2>
          <p class="section-sub">Defesa jurídica especializada nas áreas que mais importam</p>
        </div>

        <div class="areas__grid">
          <!-- Renderizado por JS a partir de data.practice_areas[] -->
          <!-- Card template:
          <article class="area-card [area-card--featured]" aria-label="{title}">
            <div class="area-card__header">
              <span class="area-card__icon" aria-hidden="true">{icon}</span>
              [<span class="area-card__badge">Especialidade Principal</span>]
              <h3 class="area-card__title">{title}</h3>
            </div>
            <p class="area-card__desc">{description}</p>
            <ul class="area-card__list">
              {services.map(s => <li>• {s}</li>)}
            </ul>
            <a href="#contato" class="area-card__cta">Consultar →</a>
          </article>
          -->
        </div>

        <p class="areas__footer-cta reveal-up">
          Tem dúvidas sobre sua situação?
          <a href="#contato">Fale com a Dra. Tatiana →</a>
        </p>
      </div>
    </section>

    <!-- ── COMO FUNCIONA ── -->
    <section id="processo" class="process section-light" aria-labelledby="processo-title">
      <div class="container">
        <div class="section-header reveal-up">
          <span class="section-label">Processo</span>
          <h2 id="processo-title">Como Funciona</h2>
          <p class="section-sub">Do primeiro contato à resolução do seu caso</p>
        </div>

        <div class="process__steps">
          <!-- Renderizado por JS a partir de data.process_steps[]
          Step template:
          <div class="process-step reveal-up" style="--delay: {i*0.15}s">
            <span class="step-number">{number}</span>
            <span class="step-icon" aria-hidden="true">{icon}</span>
            <h3 class="step-title">{title}</h3>
            <p class="step-text">{text}</p>
          </div>
          -->
          <!-- Linha conectora dourada entre steps (CSS ::after + pseudo-element) -->
        </div>
      </div>
    </section>

    <!-- ── DEPOIMENTOS ── -->
    <section id="depoimentos" class="testimonials section-bordeaux" aria-labelledby="dep-title">
      <div class="container">
        <div class="section-header reveal-up">
          <h2 id="dep-title">O Que Dizem Nossos Clientes</h2>
        </div>

        <div class="testimonials__grid">
          <!-- Renderizado por JS a partir de data.testimonials[]
          Card template:
          <blockquote class="testimonial-card reveal-up" style="--delay: {i*0.15}s">
            <div class="testimonial-stars" aria-label="{stars} de 5 estrelas">
              ★★★★★
            </div>
            <p class="testimonial-text">"{text}"</p>
            <footer class="testimonial-footer">
              <cite>{author} — {city}</cite>
              <span class="testimonial-area">{area}</span>
            </footer>
          </blockquote>
          -->
        </div>
      </div>
    </section>

    <!-- ── FAQ ── -->
    <section id="faq" class="faq section-light" aria-labelledby="faq-title">
      <div class="container faq__inner">
        <div class="section-header reveal-up">
          <span class="section-label">Dúvidas</span>
          <h2 id="faq-title">Perguntas Frequentes</h2>
        </div>

        <dl class="faq__accordion">
          <!-- Renderizado por JS a partir de data.faq[]
          Item template:
          <div class="faq-item">
            <dt>
              <button class="faq-question" aria-expanded="false" aria-controls="faq-{i}">
                {q}
                <span class="faq-icon" aria-hidden="true">+</span>
              </button>
            </dt>
            <dd id="faq-{i}" class="faq-answer" hidden>
              <p>{a}</p>
            </dd>
          </div>
          -->
        </dl>
      </div>
    </section>

    <!-- ── CONTATO / CTA FINAL ── -->
    <section id="contato" class="contact section-black" aria-labelledby="contato-title">
      <div class="container contact__inner">

        <!-- Esquerda — Info -->
        <div class="contact__info reveal-left">
          <span class="section-label section-label--gold">Contato</span>
          <h2 id="contato-title">Agende Sua Consulta</h2>
          <p class="contact__sub">
            Seu caso merece atenção especializada.
            Fale com a Dra. Tatiana e dê o primeiro passo.
          </p>

          <address class="contact__details">
            <div class="contact-item">
              <span class="contact-icon" aria-hidden="true">📞</span>
              <a href="tel:[CONFIRMAR]">[CONFIRMAR TELEFONE]</a>
            </div>
            <div class="contact-item">
              <span class="contact-icon" aria-hidden="true">📧</span>
              <a href="mailto:[CONFIRMAR]">[CONFIRMAR EMAIL]</a>
            </div>
            <div class="contact-item">
              <span class="contact-icon" aria-hidden="true">📍</span>
              <span>[CONFIRMAR ENDEREÇO] — Pomerode, SC</span>
            </div>
            <div class="contact-item">
              <span class="contact-icon" aria-hidden="true">⏰</span>
              <span>Seg–Sex: 09h–18h | Remoto disponível</span>
            </div>
          </address>

          <div class="contact__buttons">
            <a href="[WHATSAPP]" class="btn btn--whatsapp btn--lg"
               target="_blank" rel="noopener"
               aria-label="Falar com a Dra. Tatiana pelo WhatsApp">
              💬 WHATSAPP
            </a>
            <a href="[MAPS]" class="btn btn--outline-gold"
               target="_blank" rel="noopener"
               aria-label="Ver localização no Google Maps">
              📍 VER NO MAPS
            </a>
          </div>
        </div>

        <!-- Direita — Formulário -->
        <div class="contact__form-wrap reveal-right">
          <form id="contact-form" class="contact-form" novalidate>
            <h3>Envie sua mensagem</h3>

            <div class="form-field">
              <label for="nome">Nome completo *</label>
              <input type="text" id="nome" name="nome" required
                     autocomplete="name" placeholder="Seu nome">
              <span class="form-error" aria-live="polite"></span>
            </div>

            <div class="form-field">
              <label for="telefone">Telefone/WhatsApp *</label>
              <input type="tel" id="telefone" name="telefone" required
                     autocomplete="tel" placeholder="(47) 9 0000-0000">
              <span class="form-error" aria-live="polite"></span>
            </div>

            <div class="form-field">
              <label for="email">E-mail</label>
              <input type="email" id="email" name="email"
                     autocomplete="email" placeholder="seu@email.com">
              <span class="form-error" aria-live="polite"></span>
            </div>

            <div class="form-field">
              <label for="area">Área de interesse *</label>
              <select id="area" name="area" required>
                <option value="">Selecione uma área</option>
                <!-- data.form.areas_select[] -->
              </select>
              <span class="form-error" aria-live="polite"></span>
            </div>

            <div class="form-field">
              <label for="mensagem">Resumo do caso (opcional)</label>
              <textarea id="mensagem" name="mensagem" rows="3"
                        placeholder="Descreva brevemente sua situação..."></textarea>
            </div>

            <!-- Honeypot anti-spam -->
            <input type="text" name="website" style="display:none" tabindex="-1" autocomplete="off">

            <button type="submit" class="btn btn--primary btn--full">
              ENVIAR MENSAGEM
            </button>

            <p class="form-privacy">
              🔒 Suas informações são protegidas pelo sigilo profissional.
            </p>

            <!-- Estado de sucesso (hidden → visível após submit) -->
            <div class="form-success" hidden role="alert" aria-live="polite">
              <span>✅</span>
              <p>Mensagem enviada! A Dra. Tatiana entrará em contato em breve.</p>
            </div>
          </form>
        </div>

      </div>
    </section>

  </main>

  <!-- ═══════════════════════════════════════ FOOTER -->
  <footer id="footer" role="contentinfo">
    <div class="container footer__inner">
      <div class="footer__brand">
        <p class="footer__name">Dra. Tatiana de Oliveira</p>
        <p class="footer__tagline">Advocacia com Seriedade e Compromisso</p>
        <div class="footer__social">
          <a href="https://www.instagram.com/dra.tatiana_advogada/"
             target="_blank" rel="noopener noreferrer"
             aria-label="Instagram da Dra. Tatiana">
            <!-- SVG Instagram outline dourado -->
          </a>
          <a href="https://www.facebook.com/tatiadv"
             target="_blank" rel="noopener noreferrer"
             aria-label="Facebook da Dra. Tatiana">
            <!-- SVG Facebook outline dourado -->
          </a>
        </div>
      </div>

      <nav class="footer__nav" aria-label="Navegação do rodapé">
        <div class="footer__col">
          <h4>Áreas</h4>
          <ul>
            <li><a href="#areas">Direito de Família</a></li>
            <li><a href="#areas">Direito Civil</a></li>
            <li><a href="#areas">Direito do Consumidor</a></li>
          </ul>
        </div>
        <div class="footer__col">
          <h4>Contato</h4>
          <ul>
            <li><a href="#contato">WhatsApp</a></li>
            <li><a href="#contato">E-mail</a></li>
            <li><a href="#contato">Localização</a></li>
            <li><a href="#faq">Dúvidas</a></li>
          </ul>
        </div>
        <div class="footer__col">
          <h4>Institucional</h4>
          <ul>
            <li><a href="#sobre">Sobre</a></li>
            <li><a href="#">Política de Privacidade</a></li>
            <li><a href="#">Termos de Uso</a></li>
          </ul>
        </div>
      </nav>
    </div>

    <div class="footer__bottom">
      <p>© 2026 Advocacia Tatiana de Oliveira — Pomerode, SC</p>
      <p>Desenvolvido por StratAi Consulting</p>
      <p class="footer__legal">
        As informações deste site têm caráter meramente informativo e não
        constituem consulta jurídica. OAB/SC.
      </p>
    </div>
  </footer>

  <!-- WhatsApp FAB -->
  <a href="[WHATSAPP]"
     class="whatsapp-fab"
     target="_blank"
     rel="noopener"
     aria-label="Falar com a Dra. Tatiana pelo WhatsApp"
     title="WhatsApp">
    <!-- SVG WhatsApp -->
  </a>

  <!-- Scripts -->
  <script>
    // Injetar TATIANA_DATA inline
    window.TATIANA_DATA = { /* ... JSON completo ... */ };
  </script>
  <script src="js/main.js" type="module"></script>

</body>
</html>
```

---

## JAVASCRIPT — Especificações dos Módulos

### navbar.js
```javascript
// Estado: { scrolled: false, menuOpen: false }
//
// scroll > 60px → add class .scrolled ao #navbar
//   .scrolled = fundo #6B1A2C, texto branco, logo text branco
//   transição: background 0.4s var(--ease-elegant)
//
// Hamburger click → toggle .open no drawer
//   .open: translateX(0) — drawer aparece da esquerda
//   !.open: translateX(-100%)
//   aria-expanded atualizado
//
// Links drawer → fechar ao clicar
// Click fora do drawer → fechar
// ESC → fechar
//
// Active link: detectar seção visível via IntersectionObserver
//   adicionar aria-current="page" ao link correspondente
```

### counter.js
```javascript
// IntersectionObserver em #stats (threshold: 0.5)
// Ao entrar: animar cada .stat-value de 0 ao data-target
// Duração: 1800ms, easing: easeOutCubic = t => 1 - Math.pow(1-t, 3)
// Sufixo: adicionar data-suffix após o número
// Rodar apenas uma vez (disconnect após trigger)
```

### faq.js
```javascript
// Renderizar data.faq[] como <dl> accordion
// Click no <button> da pergunta:
//   toggle aria-expanded="true/false"
//   toggle hidden no <dd> correspondente
//   rotacionar ícone + → ×  (transform: rotate(45deg))
//   max-height transition suave via CSS (0 → auto emulado)
// Fechar outros ao abrir um (behavior: single open)
```

### form.js
```javascript
// Renderizar data.form.areas_select[] no <select>
//
// VALIDAÇÃO em tempo real (blur) + no submit:
//   nome: minLength 3
//   telefone: regex /^\(?\d{2}\)?\s?\d{4,5}-?\d{4}$/
//   email: regex email válido (se preenchido — opcional)
//   area: não vazia
//   Erro: add .error ao .form-field + texto no .form-error
//   Ok: remove .error + limpa .form-error
//
// ANTI-SPAM: se #website (honeypot) preenchido → abort silencioso
//
// SUBMIT SUCCESS:
//   1. Montar URL WhatsApp com dados formatados:
//      const msg = template.replace('{nome}', nome).replace('{area}', area).replace('{mensagem}', mensagem)
//      const url = `https://wa.me/${number}?text=${encodeURIComponent(msg)}`
//      window.open(url, '_blank')
//   2. Mostrar .form-success (hidden → visible)
//   3. Reset form
//
// MÁSCARA telefone: auto-formatar ao digitar
//   (XX) XXXXX-XXXX ou (XX) XXXX-XXXX
```

### reveal.js
```javascript
// Classes: .reveal-up, .reveal-left, .reveal-right, .reveal-item (com --delay CSS var)
//
// CSS inicial:
//   .reveal-up:    transform: translateY(28px); opacity: 0
//   .reveal-left:  transform: translateX(-28px); opacity: 0
//   .reveal-right: transform: translateX(28px); opacity: 0
//
// IntersectionObserver threshold: 0.15
// Ao entrar: add .is-visible
//   .is-visible: transform: none; opacity: 1
//   transition: var(--dur-reveal) var(--ease-elegant) var(--delay, 0s)
//
// Grupos .stagger-group: delay escalonado automático
//   children: nth-child * 0.12s
```

---

## CSS — Componentes Críticos

### Hero
```css
.hero {
  min-height: 100vh;
  background: var(--black-deep);
  position: relative;
  overflow: hidden;
  display: grid;
  place-items: center;
}

/* Granulado noise via filter */
.hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url("data:image/svg+xml,..."); /* SVG noise */
  opacity: 0.04;
  pointer-events: none;
}

/* Watermark § decorativo */
.hero__watermark {
  position: absolute;
  font-family: var(--font-serif);
  font-size: clamp(200px, 40vw, 500px);
  font-weight: 700;
  color: var(--bordeaux);
  opacity: 0.035;
  right: -5%;
  bottom: -10%;
  line-height: 1;
  pointer-events: none;
  user-select: none;
}

.hero__inner {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: var(--gap-xl);
  align-items: center;
  max-width: var(--container-max);
  padding: 120px var(--container-pad) 80px;
}

.hero__badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-family: var(--font-heading);
  font-size: var(--fs-xs);
  font-weight: var(--fw-semi);
  letter-spacing: var(--ls-widest);
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 24px;
}

.hero__title {
  font-family: var(--font-serif);
  font-size: var(--fs-hero);
  font-weight: 700;
  font-style: italic;
  line-height: 1.1;
  color: var(--text-light);
  letter-spacing: var(--ls-tight);
  margin-bottom: 24px;
}

.hero__photo {
  position: relative;
}

.hero__photo img {
  width: 100%;
  max-height: 620px;
  object-fit: cover;
  object-position: top center;
  filter: saturate(0.8) brightness(0.9);
  border-left: var(--accent-line);
}

.hero__photo-line {
  position: absolute;
  bottom: -24px;
  left: 0;
  width: 80px;
  height: 2px;
  background: var(--gold);
}
```

### Cards Áreas de Atuação
```css
.areas__grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--gap-md);
  margin-top: var(--gap-lg);
}

.area-card {
  background: var(--black-surface);
  border: 1px solid var(--gold-border);
  border-radius: var(--radius-lg);
  padding: 36px 28px;
  transition: border-color var(--dur-normal) var(--ease-elegant),
              box-shadow var(--dur-normal) var(--ease-elegant),
              transform var(--dur-normal) var(--ease-elegant);
}

.area-card:hover {
  border-color: var(--gold);
  box-shadow: var(--shadow-gold);
  transform: translateY(-4px);
}

.area-card--featured {
  border-top: var(--accent-line);
  /* Ou: border-top: 3px solid var(--gold) */
}

.area-card__badge {
  display: inline-block;
  padding: 4px 12px;
  background: var(--bordeaux);
  color: var(--gold-light);
  font-family: var(--font-heading);
  font-size: var(--fs-xs);
  font-weight: var(--fw-semi);
  letter-spacing: var(--ls-wide);
  text-transform: uppercase;
  border-radius: var(--radius-pill);
  margin-bottom: 16px;
}

.area-card__list {
  list-style: none;
  padding: 0;
  margin: 16px 0;
}

.area-card__list li {
  font-family: var(--font-body);
  font-size: var(--fs-sm);
  color: var(--gray-muted);
  padding: 6px 0;
  border-bottom: 1px solid rgba(255,255,255,0.04);
  display: flex;
  align-items: center;
  gap: 8px;
}

.area-card__list li::before {
  content: '•';
  color: var(--gold);
  font-size: 1.2em;
  flex-shrink: 0;
}
```

### Navbar com scroll behavior
```css
#navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  background: var(--white-warm);
  border-bottom: 1px solid var(--gold-border);
  transition: background var(--dur-slow) var(--ease-elegant),
              border-color var(--dur-slow) var(--ease-elegant),
              box-shadow var(--dur-slow) var(--ease-elegant);
}

#navbar.scrolled {
  background: var(--bordeaux);
  border-bottom-color: transparent;
  box-shadow: 0 2px 32px rgba(107,26,44,0.4);
}

/* Links: cor muda conforme estado navbar */
#navbar .navbar__links a { color: var(--text-dark); }
#navbar.scrolled .navbar__links a { color: var(--text-light); }

#navbar .navbar__name { color: var(--bordeaux); font-family: var(--font-serif); }
#navbar.scrolled .navbar__name { color: var(--text-light); }

/* Hover link: underline dourado desliza */
.navbar__links a {
  position: relative;
  text-decoration: none;
}
.navbar__links a::after {
  content: '';
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0;
  height: 1px;
  background: var(--gold);
  transition: width var(--dur-normal) var(--ease-elegant);
}
.navbar__links a:hover::after,
.navbar__links a[aria-current]::after {
  width: 100%;
}
```

---

## PERFORMANCE E SEGURANÇA

```
PERFORMANCE:
□ Foto hero: loading="eager" fetchpriority="high" (LCP otimizado)
□ Demais imagens: loading="lazy"
□ CSS crítico hero+navbar: inline no <head> (above-the-fold)
□ Google Fonts: display=swap
□ JS: type="module" (defer nativo)
□ Favicon: .ico para compatibilidade + .png 32px + .png 180px (Apple Touch)
□ OG image: 1200x630px, < 200KB
□ robots.txt: Allow: / | Sitemap referenciado

SEGURANÇA:
□ Links externos: rel="noopener noreferrer"
□ Formulário: honeypot + validação client-side completa
□ CSP meta básica
□ Dados sensíveis: nunca hardcoded no JS visível
□ HTTPS obrigatório

ACESSIBILIDADE (WCAG AA):
□ Skip link ativo como primeiro elemento do body
□ lang="pt-BR" no html
□ Todos os campos do form com <label> visível e associado (htmlFor)
□ Contraste: bordô (#6B1A2C) sobre branco quente (#FAF8F5) → ratio > 7:1 ✓
□ Contraste: dourado (#C9A96E) sobre preto (#0F0F0F) → ratio > 4.8:1 ✓
□ Focus: outline 2px solid var(--gold) + offset 2px em TODOS elementos interativos
□ aria-expanded no hamburger + FAQ botões
□ aria-live="polite" nos form-errors e form-success
□ role="alert" no form-success
□ Headings hierárquicos: h1 (hero) → h2 (sections) → h3 (cards)
□ Imagem hero: alt descritivo e específico
□ Depoimentos: <blockquote> + <cite>
□ Footer: role="contentinfo"
□ Nav: aria-label nos elementos <nav>
```

---

## CHECKLIST FINAL ANTIGRAVITY

```
DADOS E CONTEÚDO:
[ ] Confirmar com cliente: WhatsApp, email, endereço, OAB/SC, horários
[ ] Receber foto profissional da Dra. Tatiana (alta resolução)
[ ] Coletar depoimentos reais (mínimo 3, com autorização)
[ ] Definir domínio do site

ARQUIVOS:
[ ] index.html — HTML semântico completo
[ ] css/tokens.css — design tokens
[ ] css/reset.css, layout.css, components.css, animations.css, main.css
[ ] js/navbar.js, counter.js, faq.js, form.js, reveal.js, main.js
[ ] assets/foto-tatiana.jpg + og-image.jpg + favicon.ico
[ ] robots.txt + sitemap.xml

FUNCIONALIDADE:
[ ] Navbar: scroll behavior branco → bordô funcionando
[ ] Navbar: mobile menu drawer funcionando
[ ] Hero: CTA primário abre WhatsApp no link correto
[ ] Stats: counter animado ao entrar na viewport
[ ] Áreas: renderização dos 3 cards a partir do JSON
[ ] Processo: 3 steps com linha conectora dourada
[ ] Depoimentos: 3 cards responsivos
[ ] FAQ: acordeão single-open funcionando com acessibilidade
[ ] Formulário: validação completa + honeypot + envio para WhatsApp
[ ] WhatsApp FAB: visível e funcional em todas as telas

SEO & META:
[ ] Title + description injetados via JS do JSON
[ ] Schema JSON-LD LegalService no <head>
[ ] Open Graph completo
[ ] canonical link correto
[ ] robots.txt + sitemap.xml

DESIGN:
[ ] Paleta bordô/dourado/preto implementada via CSS tokens
[ ] Tipografia: Cormorant Garamond (headlines) + Raleway (headings) + Lato (corpo)
[ ] Hero: foto direita + headline serifa esquerda + watermark §
[ ] Stats: fundo bordô + dourado + counter
[ ] Areas: 3 cards escuros + card featured com badge bordô
[ ] Processo: steps com números grandes Cormorant + linha dourada
[ ] Depoimentos: fundo bordô + cards com borda-left dourada + stars douradas
[ ] FAQ: acordeão elegante em fundo branco quente
[ ] Contato: preto + formulário card + botões WhatsApp + Maps
[ ] Footer: preto + nota legal em rodapé

RESPONSIVIDADE:
[ ] 320px — Mobile S ✓
[ ] 375px — Mobile M ✓
[ ] 768px — Tablet ✓
[ ] 1024px — Tablet L ✓
[ ] 1280px — Desktop ✓
[ ] 1440px — Desktop L ✓

ACESSIBILIDADE:
[ ] Skip link presente e funcional
[ ] Contraste WCAG AA em todas combinações de cor
[ ] Focus visível em todos elementos interativos
[ ] Todos campos com labels
[ ] aria attributes corretos (expanded, hidden, live, current)
[ ] Alt text em todas as imagens
[ ] Headings em ordem correta sem pular níveis
```
