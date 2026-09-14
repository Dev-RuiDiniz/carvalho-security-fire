# Carvalho Security Fire

Landing page institucional e comercial da Carvalho Security Fire, criada para apresentar serviços de proteção contra incêndio e transformar visitas em contatos qualificados.

## Visão comercial

A Carvalho Security Fire se posiciona como uma parceira técnica para empresas que precisam manter pessoas, ativos e operações protegidos contra incêndios. A mensagem central da marca é:

> Proteção que responde antes do risco virar crise.

O site traduz essa promessa em uma experiência direta, técnica e orientada à conversão. A comunicação combina autoridade operacional, atendimento 24 horas e clareza sobre o próximo passo: falar com a equipe para avaliar a necessidade da operação.

### Oferta apresentada

- **Preventiva:** inspeções, testes e manutenções programadas para aumentar a confiabilidade do sistema.
- **Corretiva:** diagnóstico e reparo especializado com agilidade e peças originais.
- **Emergencial:** atendimento 24 horas para situações críticas.
- **Readequação:** adequação de instalações e projetos às normas e às necessidades técnicas do local.
- **FM-200:** solução de supressão para áreas críticas, com foco em proteção avançada e preservação dos equipamentos.

### Público prioritário

O conteúdo foi estruturado para falar com responsáveis por manutenção, facilities, segurança patrimonial, engenharia e operação de ambientes comerciais e industriais, especialmente locais em que uma parada ou um incidente representa alto impacto financeiro e operacional.

Entre os contextos destacados estão salas técnicas, data centers, centros de controle, áreas elétricas, infraestruturas industriais e operações que precisam demonstrar conformidade em auditorias e vistorias.

### Funil de conversão

1. **Atenção:** hero com benefício claro, fotografia de campo e linguagem de prevenção.
2. **Confiança:** indicadores de atendimento 24/7, NBR 17240, equipe própria e profissionais certificados.
3. **Compreensão:** quatro frentes de serviço, checklist técnico e aplicação do FM-200.
4. **Prova:** galeria de atuação em campo e bloco de conformidade em cada entrega.
5. **Ação:** contato direto com a equipe pelo WhatsApp 24h ou solicitação de orçamento por e-mail.

### Contatos exibidos

- Telefone e WhatsApp: **11 93000-0000**
- E-mail: **contato@carvalhosecurityfire.com.br**
- Área de atendimento: **São Paulo — SP e região metropolitana**

Os dados acima são os contatos atualmente presentes no layout e devem ser confirmados antes da publicação definitiva.

## Direção da experiência

A interface usa uma estética industrial premium: fundos pretos e grafite, vermelho de ação, áreas off-white para leitura e fotografias com iluminação dramática. O resultado deve comunicar precisão, prontidão e responsabilidade sem parecer genérico ou excessivamente promocional.

A moldura de navegador presente na imagem de referência não faz parte do site. O projeto preserva o símbolo da chama como SVG inline e usa imagens locais em WebP para evitar dependência de imagens externas.

## Estrutura do projeto

```text
.
├── index.html
├── assets/
│   ├── hero-fire-alarm.webp
│   ├── engineering.webp
│   ├── fm200.webp
│   ├── field-technician.webp
│   ├── field-valve.webp
│   ├── field-detector.webp
│   ├── field-panel.webp
│   ├── compliance-architecture.webp
│   ├── og-cover.webp
│   └── favicon.svg
├── design_system.md
├── robots.txt
└── sitemap.xml
```

## Visualização local

O site é standalone, sem framework, build ou dependência de Node.js. Para servir os arquivos localmente:

```powershell
python -m http.server 4173 --bind 127.0.0.1
```

Depois, acesse [http://127.0.0.1:4173/](http://127.0.0.1:4173/).

## SEO e publicação

O `index.html` já contém idioma `pt-BR`, viewport, title, description, canonical, Open Graph, Twitter Cards e JSON-LD de `ProfessionalService`. Também foram incluídos `robots.txt` e `sitemap.xml`.

Antes de publicar, substitua o placeholder `https://SEU-DOMINIO-AQUI.com.br/` pelo domínio real em:

- `index.html`
- `robots.txt`
- `sitemap.xml`

Na hospedagem, envie `index.html`, a pasta `assets/`, `robots.txt` e `sitemap.xml` para a raiz pública do site. Confirme também telefone, WhatsApp, e-mail, perfis sociais e o uso da marca oficial.

## Qualidade e acessibilidade

O layout possui versões para desktop, tablet e celular, menu mobile expansível, âncoras de navegação, foco visível, textos alternativos nas imagens, carregamento otimizado das imagens e suporte a `prefers-reduced-motion`.

Consulte o [design system](design_system.md) para conhecer os tokens visuais, tipografia, componentes e regras de composição usadas na implementação.
