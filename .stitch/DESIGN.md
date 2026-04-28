# Brief de Design UX — Advocacia Tatiana de Oliveira
## Para uso em: https://stitch.withgoogle.com/
## Tipo: Landing Page | Idioma: Português PT-BR
## Estilo: Sério · Dinâmico · Autoridade Jurídica · Elegância Feminina Profissional

---

## 1. IDENTIDADE DA MARCA

### Perfil da Advogada
- **Nome completo:** Dra. Tatiana de Oliveira
- **Profissão:** Advogada — OAB/SC
- **Experiência:** 17 anos de atuação
- **Áreas de excelência:** ESPECIALISTA EM DIREITO DE FAMÍLIA,EXCELÊNCIA EM DIRETO CIVIL, CONSUMIDOR, CRIMINAL E TRABALHISTA
- **Localização:** Pomerode, Santa Catarina
- **Tagline da marca:** "Advocacia com Seriedade e Compromisso"
- **Instagram:** @dra.tatiana_advogada
- **Facebook:** facebook.com/tatiadv

### Análise de Branding (com logo fornecido no arquivo ./img/LogoSite.jpg)
- **Personalidade visual:** Autoridade + Proximidade + Confiança
- **Arquétipo de marca:** O Sábio + O Protetor
- **Diferencial:** Advogada mulher especialista em Direito de Família — combina firmeza jurídica com humanização no atendimento
- **Sensação que o site deve transmitir:** "Estou em boas mãos. Ela sabe o que faz."

### Paleta de Cores

```
Bordô/Vinho escuro:    #6B1A2C   (cor primária — autoridade, seriedade, tradição jurídica)
Bordô médio:           #8B2238   (hover, gradientes, botões)
Dourado champagne:     #C9A96E   (accent premium — elegância, distinção)
Dourado claro:         #E8C99A   (destaques suaves, ícones)
Preto profundo:        #0F0F0F   (textos principais, fundo hero)
Cinza escuro:          #1C1C1C   (fundos seções alternadas)
Cinza médio:           #3A3A3A   (texto corpo em fundo escuro)
Branco quente:         #FAF8F5   (fundos claros — não branco frio)
Cinza claro:           #E8E4DF   (separadores, bordas suaves em seções claras)
Cinza texto:           #5A5A5A   (texto secundário em fundo claro)
```

### Tipografia Sugerida (Stitch)

```
Display/Hero:    Cormorant Garamond Bold Italic  — elegância jurídica, serifa premium feminina
                 OU Playfair Display Bold         — alternativa mais neutra mas igualmente elegante
Subtítulos H2:   Raleway SemiBold               — moderno, limpo, respeitoso
H3/Labels:       Raleway Medium                 — consistência
Corpo:           Lato Regular                   — leitura fluida e neutra
Detalhes/OAB:   Lato Italic                    — sutileza para dados institucionais
```

**Racionale:** Serifa elegante nos títulos (tradição e autoridade jurídica) + sans-serif limpa no corpo (modernidade e clareza). Evitar fontes sem personalidade.

---

## 2. CONCEITO DE DESIGN

### Direção Estética
**"Lex Aurea"** — Latim para "Lei Dourada". Design editorial sério e elegante. Bordô profundo como fundo dominante nas seções âncora. Dourado como metal de precisão e distinção. Tipografia serifa clássica modernizada. Espaçamento generoso. Nenhum elemento supérfluo — cada pixel serve um propósito.

Dinâmico através de: linhas diagonais sutis, elementos que entram em scroll com fade direcional, destaques em dourado que "brilham" no hover, não por animações agressivas, mas por elegância controlada.

### Tom de Voz Visual
- Sério sem ser intimidador
- Confiante e assertivo
- Humano — a advogada é acessível, mesmo sendo especialista
- Feminino profissional — não rosé, não corporativo frio

### Mood Board
- Fundo bordô escuro hero + texto branco + linha dourada
- Foto profissional da Dra. Tatiana em pose de autoridade
- Seções claras em branco quente intercaladas com seções escuras
- Ícones de balança, §, proteção estilizados em dourado outline
- Textura sutil de papel/granulado em fundos claros (5% opacidade)

---

## 3. ESTRUTURA DE SEÇÕES — LANDING PAGE

### SEÇÃO 1: NAVBAR (fixo no topo)
```
LAYOUT: Fundo branco quente (#FAF8F5), borda-bottom 1px #E8C99A (dourado suave)
- Logo (mascara cuadrada de bordes redondeados con la foto./img/LogoSite.jpg)/Nome (esquerda): "Dra. Tatiana de Oliveira" em Cormorant Garamond + 
  "Advocacia" em Raleway light abaixo — ou logotipo se fornecido pela cliente
- Links centro/direita: Sobre · Áreas de Atuação · Processo · Contato
- CTA navbar: Botão bordô pequeno [AGENDAR CONSULTA] com texto branco
- Mobile: hamburger bordô, drawer lateral branco quente

Ao scroll > 60px:
  → fundo muda para #6B1A2C (bordô) com texto branco + borda dourada
  → transição suave 0.4s ease
```

### SEÇÃO 2: HERO (Fullscreen — fundo escuro + foto profissional)
```
LAYOUT: Divisão assimétrica — 55% texto/esquerda | 45% foto profissional/direita
Fundo: #0F0F0F com textura de granulado sutil (noise 3%, opacity 40%)
Detalhe: Linha vertical dourada (2px) dividindo texto e imagem

ELEMENTOS (lado esquerdo):
- Badge topo: "⚖️ OAB/SC · Pomerode, SC" em Raleway small, dourado, tracking amplo
- H1: "Seus Direitos Merecem Uma Defesa à Altura"
  (Cormorant Garamond Bold Italic, branco, enorme — clamp 3.5rem → 6rem)
- Sub: "15 anos de experiência em Direito de Família, Civil e do Consumidor.
  Atendimento humanizado, estratégia jurídica séria."
- CTA Duplo:
    [AGENDAR CONSULTA GRATUITA] — botão bordô sólido, dourado no hover
    [Ver Áreas de Atuação ↓]    — link texto branco com sublinhado dourado
- Detalhe decorativo: "§" grande em bordô muito sutil (opacity 0.04) atrás do texto

ELEMENTOS (lado direito):
- Foto profissional da Dra. Tatiana (FORNECIDA PELA CLIENTE)
  → Tratamento: P&B ou levemente dessaturado com overlay bordô 15%
  → Formato: sem moldura, integrada ao fundo escuro
  → Posição: centralizada verticalmente, levemente para baixo
- Detalhe dourado: linha horizontal fina abaixo do nome/credenciais na foto

MOBILE: Foto por cima, texto por baixo — foto com crop no rosto (3:2)
```

### SEÇÃO 3: NÚMEROS / CREDIBILIDADE (strip rápido)
```
LAYOUT: Fundo bordô (#6B1A2C), 3-4 stats em linha, dourado + branco

STATS:
  15 anos       de Experiência Jurídica
  2.500+        Clientes Atendidos  [estimativa — confirmar com a cliente]
  3             Áreas de Especialização
  100%          Sigilo e Ética Profissional

Tipografia: número em Cormorant Garamond Bold grande, branco
            label em Raleway small, dourado/champagne

Separadores: linha vertical 1px dourada (opacity 0.3) entre stats
Counter animado: ao entrar na viewport, números contam de 0 ao valor
```

### SEÇÃO 4: SOBRE A ADVOGADA
```
LAYOUT: Fundo branco quente (#FAF8F5), 2 colunas — foto esquerda | texto direita
TÍTULO: "Quem é a Dra. Tatiana"

FOTO: Foto profissional secundária (se disponível) ou mesma do hero
  → Formato retângulo vertical, borda-left 4px dourado
  → Moldura sutil: box-shadow com tom bordô

TEXTO:
  "Advogada inscrita na OAB/SC há 15 anos, a Dra. Tatiana de Oliveira 
  construiu sua trajetória em Pomerode com base em três princípios: 
  seriedade jurídica, compromisso com o cliente e resultados reais.

  Especialista em Direito de Família, atua com excelência também nas 
  áreas Cível e do Consumidor — áreas que tocam diretamente a vida 
  cotidiana das pessoas.

  Cada caso é tratado com atenção individualizada. Porque para quem 
  está passando por um momento difícil, ter ao lado uma advogada de 
  confiança faz toda a diferença."

CREDENCIAIS (abaixo do texto, ícones + texto):
  ⚖️ OAB/SC — Advogada regularmente inscrita
  🏛️ 15 anos de atuação ativa
  📍 Pomerode, SC — Atendimento presencial e remoto

CTA: [FALE COMIGO AGORA →] — link bordô com hover dourado
```

### SEÇÃO 5: ÁREAS DE ATUAÇÃO (Cards — seção escura)
```
LAYOUT: Fundo #1C1C1C, título centralizado + 3 cards em grid
TÍTULO: "Áreas de Atuação"
SUBTÍTULO: "Defesa jurídica especializada nas áreas que mais importam"

CARD 1 — DIREITO DE FAMÍLIA (ESPECIALIDADE PRINCIPAL)
  Ícone: ⚖️ ou família estilizada (outline dourado)
  Badge: "Especialidade Principal" — pill dourado
  Título: "Direito de Família"
  Itens:
    • Divórcio consensual e litigioso
    • Guarda e convivência familiar
    • Pensão alimentícia
    • Inventário e partilha de bens
    • União estável
    • Adoção
  Destaque: Borda-top 3px dourado, card levemente maior que os outros

CARD 2 — DIREITO CIVIL
  Ícone: 📄 documento/contrato (outline dourado)
  Título: "Direito Civil"
  Itens:
    • Contratos e rescisão contratual
    • Responsabilidade civil e indenizações
    • Questões imobiliárias
    • Cobranças e execuções
    • Revisão de dívidas

CARD 3 — DIREITO DO CONSUMIDOR
  Ícone: 🛡️ escudo (outline dourado)
  Título: "Direito do Consumidor"
  Itens:
    • Cobranças indevidas e negativação
    • Produtos defeituosos
    • Propaganda enganosa
    • Cancelamento de contratos abusivos
    • Ação em Procon e judicialmente

ESTILO CARDS:
  Fundo: #252525
  Borda: 1px rgba(201,169,110,0.2) — dourado muito suave
  Border-radius: 8px
  Hover: border-color dourado 100% + leve sombra dourada (glow suave)
  Ícone: círculo bordô com ícone branco dentro

CTA ABAIXO: "Tem dúvidas sobre sua situação? [Fale com a Dra. Tatiana →]"
```

### SEÇÃO 6: COMO FUNCIONA O ATENDIMENTO (3 etapas)
```
LAYOUT: Fundo branco quente, processo em 3 steps horizontais conectados
TÍTULO: "Como Funciona"
SUBTÍTULO: "Do primeiro contato à resolução do seu caso"

STEP 1: "Consulta Inicial"
  Número: "01" grande, bordô, Cormorant Garamond
  Ícone: telefone/chat
  Texto: "Entre em contato pelo WhatsApp ou formulário.
          A Dra. Tatiana analisa seu caso de forma confidencial."

STEP 2: "Análise e Estratégia"
  Número: "02" grande, bordô
  Ícone: lupa/documento
  Texto: "Avaliação detalhada da situação jurídica e elaboração 
          da melhor estratégia para o seu caso."

STEP 3: "Defesa e Resultado"
  Número: "03" grande, bordô
  Ícone: balança/check
  Texto: "Acompanhamento completo do processo. 
          Você é informado em cada etapa, sem surpresas."

CONECTOR: Linha tracejada dourada (horizontal, desktop) ligando os 3 steps
MOBILE: Steps empilhados verticalmente com linha vertical à esquerda
```

### SEÇÃO 7: DEPOIMENTOS / PROVA SOCIAL
```
LAYOUT: Fundo bordô (#6B1A2C), cards de depoimentos com stars douradas
TÍTULO: "O Que Dizem Nossos Clientes"

CARD 1:
  "A Dra. Tatiana me orientou em um processo de divórcio muito delicado.
   Foi profissional, humana e sempre clara sobre cada passo. 
   Sinto que meus direitos foram verdadeiramente defendidos." ★★★★★
   — M.S., Pomerode SC

CARD 2:
  "Tive um problema sério com um produto defeituoso e não sabia como agir.
   A Dra. Tatiana resolveu tudo em poucas semanas. Recomendo sem hesitar." ★★★★★
   — R.K., Blumenau SC

CARD 3:
  "Questão de guarda dos filhos — o momento mais difícil da minha vida.
   A Dra. Tatiana foi firme quando precisou e humana sempre. Resultado excelente." ★★★★★
   — F.O., Pomerode SC

NOTA: Depoimentos são representativos — confirmar com depoimentos reais da cliente
      via Google/Facebook reviews ou solicitar autorização para uso.

ESTILO CARDS:
  Fundo: rgba(255,255,255,0.08)
  Borda-left: 3px solid #C9A96E
  Stars: dourado #E8C99A
  Texto: branco, Lato Italic, 15px
  Assinatura: Raleway SemiBold, dourado champagne
```

### SEÇÃO 8: FAQ (Dúvidas Frequentes)
```
LAYOUT: Fundo branco quente, acordeão elegante em 1 coluna (max 680px centrado)
TÍTULO: "Dúvidas Frequentes"

Q: O que é a consulta inicial e ela tem custo?
A: A consulta inicial tem como objetivo entender sua situação jurídica.
   Entre em contato para verificar as condições de atendimento.

Q: Atende fora de Pomerode?
A: Sim. A Dra. Tatiana realiza atendimentos presenciais em Pomerode/SC
   e consultoria remota para toda Santa Catarina e demais estados.

Q: Quanto tempo leva um processo?
A: O prazo varia conforme a área e a complexidade. Em Direito de Família,
   acordos podem ser resolvidos em semanas; processos litigiosos levam meses
   a anos. A Dra. Tatiana orienta sobre cada situação individualmente.

Q: O que levo para a primeira consulta?
A: Documentos pessoais (RG, CPF), documentos relacionados ao caso
   (contratos, certidão de casamento, notas fiscais, etc.) e um 
   resumo da situação. Não se preocupe — ela orienta no que for necessário.

Q: Como funciona o sigilo das informações?
A: O sigilo é absoluto e garantido pelo Código de Ética da OAB.
   Todas as informações compartilhadas são protegidas pelo segredo profissional.

ESTILO:
  Pergunta: Raleway SemiBold 16px, bordô, ícone + dourado à direita
  Resposta: Lato Regular 15px, #5A5A5A, padding-left 16px
  Aberto: fundo bordô 5% + borda-left 2px dourado
  Transição: max-height 0.35s ease
```

### SEÇÃO 9: CONTATO / CTA FINAL
```
LAYOUT: Fundo #0F0F0F (preto), 2 colunas — texto esquerda | card formulário direita
Detalhe decorativo: linha dourada horizontal no topo da seção (2px, 60px largura)

ESQUERDA:
  Título: "Agende Sua Consulta"
         (Cormorant Garamond Bold Italic, branco, 3rem)
  Sub: "Seu caso merece atenção especializada.
        Fale com a Dra. Tatiana e dê o primeiro passo."

  Info de contato (ícones dourados):
  📞 [confirmar número com a cliente]
  📧 [confirmar email com a cliente]
  📍 Pomerode, SC — [confirmar endereço com a cliente]
  ⏰ Seg–Sex: 09h–18h | Atendimento remoto disponível

  Botões diretos:
  [💬 WHATSAPP] — verde, ícone WA
  [📍 VER NO MAPS] — bordô outline

DIREITA — Card formulário (fundo #1C1C1C, borda 1px dourado suave):
  Título card: "Envie sua mensagem"
  Campos:
    Nome completo (text, required)
    Telefone/WhatsApp (tel, required)
    E-mail (email)
    Área de interesse (select):
      Direito de Família
      Direito Civil
      Direito do Consumidor
      Outra área
    Mensagem resumida (textarea, 3 linhas)
  Botão: [ENVIAR MENSAGEM] — bordô, full-width, dourado no hover
  Nota: "Suas informações são protegidas pelo sigilo profissional."
        (Lato 12px, cinza, ícone cadeado)
```

### SEÇÃO 10: FOOTER
```
LAYOUT: Fundo #0F0F0F, texto cinza e branco, linha dourada no topo
- Nome: "Dra. Tatiana de Oliveira — Advocacia" (Cormorant Garamond, branco)
- Tagline: "Advocacia com Seriedade e Compromisso" (Raleway Light, dourado)
- 3 colunas:
    Áreas: Direito de Família · Direito Civil · Direito do Consumidor
    Contato: WhatsApp · E-mail · Localização · Agendamento
    Institucional: OAB/SC · Código de Ética · Privacidade · Termos
- Redes sociais: Instagram + Facebook (ícones outline dourados)
- Rodapé: "© 2026 Advocacia Tatiana de Oliveira — Pomerode, SC | 
           Desenvolvido por StratAi Consulting"
- NOTA LEGAL: "As informações deste site têm caráter meramente informativo 
               e não constituem consulta jurídica."
               (Lato 11px, cinza muito claro)
```

---

## 4. DIRETRIZES DE COMPONENTES UI

### Botões
```
Primário:    fundo #6B1A2C (bordô) | texto branco | border-radius 4px | 
             padding 14px 32px | Raleway SemiBold uppercase
             hover: #8B2238 + box-shadow 0 4px 20px rgba(107,26,44,0.4)
Dourado:     fundo #C9A96E | texto #0F0F0F | elegante para CTAs premium
             hover: #E8C99A
Outline:     borda 2px #C9A96E | texto #C9A96E | fundo transparente
             hover: fundo #C9A96E | texto #0F0F0F
WhatsApp:    fundo #25D366 | texto branco
```

### Elementos Decorativos
```
- Símbolo § estilizado em bordô (opacity 0.04) como watermark em seções escuras
- Linha dourada 2px como separador entre seções e como detalhe nos cards
- Textura de granulado/noise 3% nos fundos para adicionar profundidade
- Aspas tipográficas " " grandes em dourado (opacity 0.15) nos depoimentos
- Número da seção em Cormorant Garamond enorme (opacity 0.06) como background
```

---

## 5. RESPONSIVIDADE

```
Mobile:  < 768px   — Hero vertical (foto acima), stats 2x2, cards área 1 coluna
Tablet:  768-1024px — Hero 2 col reduzido, cards 2+1, processo steps verticais
Desktop: > 1024px  — Layout completo conforme especificado
```

### Mobile First Crítico
- Hero: botão WhatsApp flutuante SEMPRE visível
- Navbar: apenas logo + hamburger + CTA pequeno
- Cards área de atuação: accordion no mobile (colapsa lista de itens)
- Formulário: campos full-width empilhados

---

## 6. ACESSIBILIDADE

```
- lang="pt-BR" no html
- Contraste: bordô sobre branco quente = ratio > 7:1 ✓
- Contraste: dourado sobre preto = ratio > 4.5:1 ✓
- Focus: outline 2px #C9A96E em todos elementos interativos
- Alt text em foto da Dra. Tatiana com descrição profissional
- aria-label nos botões de ícone
- Heading hierarchy: h1 > h2 > h3
- Links com texto descritivo (não "clique aqui")
- Formulário: labels visíveis em todos os campos
```

---

## 7. MICROINTERAÇÕES PRIORITÁRIAS

```
1. NAVBAR: Transição de branco → bordô ao scroll (suave, 0.4s)
2. HERO foto: Entrada com fade-in suave da direita (0.8s delay 0.3s)
3. HEADLINE: Palavras entram com stagger 60ms (fade-up + blur suave)
4. STATS: Counter animado de 0 ao valor ao entrar na viewport
5. CARDS ÁREA: Hover → borda dourada + sombra bordô glow muito suave
6. FAQ: Acordeão com max-height transition, ícone + roda 45°
7. BOTÃO WHATSAPP FAB: Pulse bordô suave a cada 4s (scale 1.05)
8. DEPOIMENTOS: Carrossel automático suave (mobile) — manual no desktop
9. LINKS NAV: Underline dourado desliza da esquerda para direita no hover
10. FORMULÁRIO SUCCESS: Substituição elegante com mensagem e checkmark dourado
```

---

## 8. SEO E META

```html
<title>Dra. Tatiana de Oliveira | Advogada em Pomerode SC — Família, Civil e Consumidor</title>
<meta name="description" content="Advogada há 15 anos em Pomerode/SC. Especialista em Direito de Família. Excelência em Direito Civil e do Consumidor. Atendimento humanizado e resultados reais. OAB/SC.">
<meta name="keywords" content="advogada pomerode sc, direito de família pomerode, advocacia pomerode, advogada família civil consumidor sc, tatiana de oliveira advogada">
<meta property="og:title" content="Dra. Tatiana de Oliveira — Advocacia em Pomerode SC">
<meta property="og:description" content="15 anos de experiência. Especialista em Direito de Família, Civil e do Consumidor em Pomerode, SC. Agende sua consulta.">
<meta property="og:image" content="[foto profissional da Dra. Tatiana]">
```

---

## 9. DADOS A CONFIRMAR COM A CLIENTE
```
⚠️  Antes do build, confirmar com a Dra. Tatiana:
    □ Número de WhatsApp: (47) 99112-9016
    □ E-mail de contato: [EMAIL_ADDRESS]
    □ Endereço completo do escritório: R. Independência, 105 - sala 02 - Centro, Pomerode - SC, 89107-000
    □ Foto profissional (alta qualidade, fundo neutro ou profissional): ./img/FotoProfissional.jpg
    □ Número OAB/SC: 28.117
    □ Depoimentos reais de clientes (com autorização)
    □ Número aproximado de clientes atendidos (para o stat): 17 anos de experiência
    □ Horários de atendimento: Seg–Sex: 09h–18h | Atendimento remoto disponível
    □ Aceita atendimento remoto? (expandir para SC/Brasil?)
    □ Logo existe? Se sim, enviar arquivo vetorial
    □ Domínio do site (ex: tatianadeoliveiraadv.com.br)
```
  
## 10. Criterios de Aceptación (Definition of Done)
- [ ] La web carga sin errores en el navegador
- [ ] El diseño es responsive
- [ ] El modo claro y oscuro funcionan correctamente
- [ ] El contenido está completamente en español
- [ ] El CTA es claro y visible
- [ ] El código está limpio, organizado y comentado cuando sea necesario
- [ ] Cumple con las reglas definidas en AGENTS.md.
- [ ] La landing es adecuada para demostración pública y uso real

