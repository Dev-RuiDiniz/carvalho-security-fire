# Design System — Carvalho Security Fire

Base visual e editorial usada na landing page da Carvalho Security Fire. Este documento descreve o sistema atual para orientar ajustes, novas seções e futuras páginas sem perder a linguagem da marca.

## 1. Princípio de direção

**Autoridade técnica com urgência controlada.**

O design combina registro documental de campo, contraste editorial e sinais claros de prontidão. A interface precisa parecer precisa, robusta e confiável, com espaço para a fotografia provar o trabalho e com o vermelho reservado para ação, risco e orientação.

Evitar: estética de template genérico, excesso de efeitos, gradientes coloridos, ícones decorativos sem função, textos longos em blocos densos e imagens com aparência de banco de imagens.

## 2. Tokens visuais

### Cores

| Token | Valor | Uso |
| --- | --- | --- |
| `--bg` | `#0b0e0f` | fundo principal escuro |
| `--bg-deep` | `#070909` | rodapé e áreas de maior contraste |
| `--panel` | `#111617` | painéis escuros e conformidade |
| `--panel-2` | `#161b1c` | superfícies secundárias |
| `--ink` | `#f3f0ea` | texto claro principal |
| `--muted` | `#a7aaa7` | texto secundário em fundo escuro |
| `--paper` | `#f0ede7` | seções claras e áreas de leitura |
| `--paper-2` | `#e4e0d8` | variação off-white e divisores claros |
| `--ink-dark` | `#131718` | texto principal em fundo claro |
| `--muted-dark` | `#535754` | texto secundário em fundo claro |
| `--accent` | `#e43128` | CTA, links, ícones e marcadores de ação |
| `--accent-dark` | `#ae201b` | variação escura do vermelho |
| `--line` | `rgba(255,255,255,.15)` | linhas sobre fundos escuros |
| `--line-dark` | `rgba(19,23,24,.18)` | linhas sobre fundos claros |

O vermelho deve funcionar como sinal: uma ação principal por grupo, estados ativos, setas, ícones e pequenos indicadores. Não usar o vermelho como fundo dominante de seções extensas.

### Tipografia

As fontes são carregadas pelo Google Fonts:

- **Barlow Condensed, peso 500:** títulos, números de impacto e chamadas editoriais. Sempre em caixa alta, com largura compacta e `letter-spacing` negativo.
- **Inter, pesos 400–800:** corpo de texto, navegação, botões e informações de contato.
- **IBM Plex Mono, peso 600:** etiquetas técnicas, eyebrow, listas de checklist, microcopy e dados operacionais.

Papéis tipográficos:

| Papel | Família | Tratamento |
| --- | --- | --- |
| Display | Barlow Condensed | uppercase, `line-height: .88`, tracking aproximado de `-.035em` |
| Corpo | Inter | leitura confortável, `line-height: 1.5–1.65` |
| Label técnico | IBM Plex Mono | uppercase, tracking de `.08–.20em`, tamanho reduzido |
| Botão | Inter | peso 800, uppercase, tracking de `.06em` |

### Forma, bordas e movimento

- Bordas predominantemente retas; o sistema não usa cantos arredondados como linguagem principal.
- Divisores de `1px` organizam os módulos e reforçam a leitura técnica.
- Sombras devem ser discretas; o menu mobile usa a sombra do token `--shadow` já definido no documento principal.
- Hover de botões: deslocamento vertical de aproximadamente `2px`, reforço da borda e mudança de superfície.
- Transições curtas, entre `200ms` e `300ms`, com easing suave.
- Em `prefers-reduced-motion: reduce`, remover transformações e transições não essenciais.

## 3. Grade e responsividade

### Casca da página

- Conteúdo central com largura máxima aproximada de `1280px`.
- Em desktop, a moldura interna usa margem lateral equivalente a `36px`.
- A página é dividida em blocos de fundo escuro e off-white, sempre com linhas e cortes nítidos.
- O header começa sobre o hero e se torna fixo após a rolagem, com fundo escuro translúcido e blur.

### Breakpoints atuais

- **Acima de 1080px:** composição desktop completa, grade de serviços em quatro colunas e FM-200 em três colunas.
- **Até 1080px:** redução de espaçamentos e simplificação da grade para preservar leitura.
- **Até 800px:** menu recolhido, hero empilhado, confiança em duas colunas, serviços em duas colunas e blocos técnicos em uma coluna.
- **Até 470px:** conteúdo em coluna única, cards de serviço sem divisores laterais e CTAs em largura total.

O objetivo é manter a hierarquia e o contraste, não preservar a quantidade de colunas a qualquer custo. Nenhum viewport deve gerar overflow horizontal.

## 4. Arquitetura da página

1. **Hero / início:** fotografia ampla de técnico diante de painel vermelho, overlay escuro, navegação e CTA.
2. **Faixa de confiança:** cinco indicadores: confiança técnica, 24/7, NBR 17240, equipe própria e continuidade.
3. **Serviços / capacidades:** título editorial, texto de apoio, quatro cards e painel lateral de engenharia.
4. **FM-200:** checklist, fotografia do cilindro e explicação da solução para áreas críticas.
5. **Em campo / sobre:** texto introdutório, quatro imagens e nota lateral sobre disciplina técnica.
6. **Conformidade / NBR 17240:** imagem arquitetônica institucional e três provas de entrega.
7. **Contato:** CTA final para atendimento 24h e orçamento.
8. **Rodapé:** marca, navegação, contato, redes e aviso legal.

## 5. Componentes

### Navegação

Logo com símbolo de chama em SVG inline, nome da marca e descriptor técnico. Os links são curtos e apontam para âncoras da própria página: `Início`, `Serviços`, `Soluções`, `NBR 17240`, `Sobre` e `Contato`.

No mobile, o botão de menu precisa ter `aria-expanded`, `aria-controls` e rótulo acessível. O estado aberto deve ser claro visualmente e permitir fechar pelo próprio botão.

### Eyebrow

Etiqueta curta em IBM Plex Mono, vermelha, uppercase e com tracking amplo. Usar para contextualizar uma seção, não para repetir o título.

### Botões

- **Primary:** fundo `--accent`, texto branco e seta opcional; usado em “Falar com a equipe 24h”.
- **Secondary:** transparente, borda clara e texto claro; usado em “Ver serviços” e “Solicitar orçamento”.
- **Link técnico:** sem caixa, vermelho, IBM Plex Mono e seta; usado em ações secundárias de cards.

Todos os botões devem ter foco visível com outline vermelho e área clicável confortável.

### Faixa de confiança

Fundo `--paper`, texto `--ink-dark`, módulos separados por linhas finas. Cada item deve ter uma mensagem curta e verificável. Números como `24/7` e `NBR 17240` podem receber Barlow Condensed para ganhar presença.

### Cards de serviço

Cada card contém número ordinal, ícone linear vermelho, título curto, descrição objetiva e seta de ação alinhada na base. Os quatro serviços formam uma sequência operacional: prevenção, correção, emergência e adequação.

### Painéis de imagem

Imagens devem preencher a área com `object-fit: cover`, mantendo o enquadramento de trabalho em campo. O texto sobreposto precisa de overlay suficiente para leitura e não deve depender apenas da imagem para transmitir informação.

### Checklist técnico

Lista em IBM Plex Mono, com marcadores vermelhos e separadores horizontais. Os itens atuais são: centrais de alarme, detectores de fumaça e calor, acionadores manuais, sirenes e dispositivos audiovisuais, sistemas de supressão FM-200, painéis e quadros de comando, infraestrutura elétrica, relatórios técnicos e conformidade NBR 17240.

### Provas de conformidade

Três itens com ícone vermelho, título em Barlow Condensed e explicação curta. A função é reduzir objeção comercial e mostrar que o serviço cobre projeto, documentação e acompanhamento especializado.

## 6. Imagens e tratamento

Todos os assets são locais, em WebP, e devem preservar a paleta preto/vermelho/off-white, contraste alto e textura industrial. Não inserir logotipos, textos artificiais ou marcas d’água nas fotografias.

| Arquivo | Aplicação |
| --- | --- |
| `hero-fire-alarm.webp` | hero principal, carregamento prioritário |
| `engineering.webp` | painel vertical de engenharia na seção de serviços |
| `fm200.webp` | fotografia central do bloco FM-200 |
| `field-technician.webp` | galeria de atuação em painel |
| `field-valve.webp` | galeria de válvula e manutenção |
| `field-detector.webp` | galeria de detector de fumaça |
| `field-panel.webp` | galeria de gabinete vermelho |
| `compliance-architecture.webp` | imagem institucional de conformidade |
| `og-cover.webp` | compartilhamento social e Open Graph |
| `favicon.svg` | identificação do site no navegador |

O hero usa `fetchpriority="high"`. As demais imagens de conteúdo usam `loading="lazy"` e `decoding="async"`, sempre com `alt` descritivo quando a imagem comunica informação. Imagens meramente decorativas devem usar `alt=""`.

## 7. Conteúdo e tom de voz

- Direto, técnico e seguro; evitar superlativos sem evidência.
- Preferir verbos de ação: inspecionar, diagnosticar, adequar, responder, preservar.
- Falar de continuidade operacional e redução de risco, não de medo.
- Manter títulos curtos, em caixa alta, com quebras controladas apenas no desktop.
- Não inventar endereço físico, clientes, certificações adicionais ou métricas não confirmadas.

## 8. SEO, semântica e acessibilidade

- Documento em `lang="pt-BR"`, com um único `h1` e hierarquia progressiva de `h2` e `h3`.
- Title e description orientados a proteção contra incêndio, atendimento rápido e conformidade.
- Canonical, Open Graph, Twitter Cards e JSON-LD `ProfessionalService` usam o placeholder `https://SEU-DOMINIO-AQUI.com.br/` até a confirmação do domínio final.
- `robots.txt` aponta para `sitemap.xml`, ambos na raiz pública.
- Links de telefone, WhatsApp e e-mail devem continuar funcionais.
- Foco visível, navegação por teclado, contraste suficiente e menu mobile com estado anunciado.
- Respeitar `prefers-reduced-motion` e evitar informação transmitida somente por cor.

## 9. Regras de manutenção

1. Reutilizar os tokens acima antes de criar novas cores ou tamanhos.
2. Manter o site standalone, sem introduzir framework ou etapa de build sem decisão explícita.
3. Preservar a ordem de leitura e as âncoras ao alterar a composição.
4. Conferir desktop na largura da referência, desktop amplo, tablet e celular.
5. Após cada ajuste visual, validar overflow horizontal, imagens, menu mobile, âncoras, foco, console e recarregamento.
