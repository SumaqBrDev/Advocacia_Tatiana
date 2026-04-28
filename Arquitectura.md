# Arquitetura do Projeto — Advocacia Tatiana de Oliveira

Este documento descreve as decisões técnicas e a estrutura da landing page desenvolvida.

## 1. Decisões de Design (UI/UX)
- **Paleta de Cores (Lex Aurea)**:
    - **Bordô (#6B1A2C)**: Representa tradição, seriedade e a "púrpura" da autoridade jurídica.
    - **Dourado (#C9A96E)**: Representa o valor, a distinção e o nível premium do serviço.
    - **White Warm (#FAF8F5)**: Proporciona uma leitura confortável, evitando o contraste agressivo do branco puro.
- **Tipografia**:
    - **Cormorant Garamond**: Escolhida por sua elegância clássica em títulos, evocando a tradição dos escritórios de advocacia de elite.
    - **Raleway**: Para subtítulos e elementos de interface, trazendo um toque moderno e limpo.
    - **Lato**: Para o corpo de texto, garantindo legibilidade máxima em dispositivos móveis.

## 2. Pilha Tecnológica (Stack)
- **HTML5 Semântico**: Uso de tags como `<header>`, `<main>`, `<section>`, `<article>`, `<address>` e `<footer>` para melhor acessibilidade e SEO.
- **Tailwind CSS 4**: Utilizado para uma prototipagem rápida e consistente, permitindo uma interface responsiva sem a sobrecarga de arquivos CSS externos pesados.
- **JavaScript Vanilla**: Implementado para manter a performance alta (Core Web Vitals). Responsável por:
    - Menu mobile.
    - Scroll suave e efeitos de navegação.
    - Animações de entrada (Intersection Observer).
    - Lógica de FAQ e contadores.

## 3. SEO e Metadados
- **Schema.org**: Implementação de `LegalService` e `Person` para que os motores de busca compreendam a natureza do negócio e a autoridade da profissional.
- **SEO Local**: Inclusão estratégica de termos geográficos (Pomerode, SC) para capturar tráfego regional qualificado.
- **Otimização de Imagens**: Uso de preloads para imagens críticas (hero) e carregamento lento (lazy loading) para o restante.

## 4. Estrutura de Seções
1. **Hero**: Proposta de valor clara e CTA imediato.
2. **Stats**: Validação rápida de autoridade (17 anos, clientes, etc).
3. **Sobre**: Humanização e construção de confiança (foto de trabalho).
4. **Áreas de Atuação**: Detalhamento técnico dos serviços.
5. **Processo**: Alinhamento de expectativas e transparência.
6. **Testemunhos**: Prova social baseada em casos reais.
7. **FAQ**: Redução de atritos e objeções comuns.
8. **Contato**: Múltiplos canais (Formulário, WhatsApp, Maps).

---
*Documento gerado como parte do protocolo de observabilidade Antigravity.*
