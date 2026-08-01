# Relatório Final - Landing Page Venda de Móveis Usados

## 1. Visão Geral do Projeto

### 1.1 Objetivo
Desenvolver uma landing page de alta conversão para a venda de móveis usados, transmitindo confiança, qualidade e sustentabilidade. O projeto visa conectar vendedores de móveis de segunda mão com compradores que buscam peças curadas, higienizadas e com garantia, a preços acessíveis.

### 1.2 Público-Alvo
- **Demografia**: Adultos de 25 a 55 anos, classe média e média-alta.
- **Perfil psicográfico**: Pessoas preocupadas com sustentabilidade e economia circular; primeiros compradores de imóvel; quem busca reformar ou decorar com orçamento limitado; empresas de escritório que necessitam de móveis funcionais.
- **Dores**: Preço elevado de móveis novos; desconfiança com a qualidade de móveis usados; falta de garantia e documentação em compras de segunda mão.

---

## 2. Estrutura de Arquivos e Tecnologias

### 2.1 Estrutura de Diretórios

```
landing-page-moveis-usados/
├── index.html
├── styles.css
├── assets/
│   ├── sofa-placeholder.svg
│   ├── mesa-placeholder.svg
│   ├── cadeira-placeholder.svg
│   └── armario-placeholder.svg
└── RELATORIO.md
```

### 2.2 Tecnologias Utilizadas

| Tecnologia | Finalidade |
|-----------|-----------|
| HTML5 | Estrutura semântica da página |
| CSS3 (Custom Properties, Grid, Flexbox) | Estilização e layout responsivo |
| JavaScript (Vanilla ES6+) | Manipulação do formulário de contato |
| Google Fonts (Inter) | Tipografia web com fallbacks nativos |
| Schema.org (JSON-LD) | Dados estruturados para SEO |

### 2.3 Decisões Arquiteturais
- **Sem framework CSS**: Escolha por CSS puro para garantir performance máxima e ausência de dependências externas (além da fonte).
- **CSS Variables**: Uso de custom properties para facilitar manutenção da paleta de cores e espaçamentos.
- **SVG inline para placeholders**: Assets vetoriais leves para garantir carregamento rápido mesmo sem imagens reais.

---

## 3. Decisões de Design

### 3.1 Paleta de Cores

A paleta foi construída para evocar calor, confiança e sustentabilidade:

| Variável | Valor Hex | Uso |
|----------|-----------|-----|
| `--color-wood` | `#5D4037` | Header, footer, títulos principais |
| `--color-wood-light` | `#8D6E63` | Textos secundários, citações |
| `--color-beige` | `#F5F0E8` | Acentos sutis |
| `--color-olive` | `#7CB342` | CTAs, indicadores, elementos interativos |
| `--color-olive-dark` | `#689F38` | Hover states |
| `--color-olive-light` | `#AED581` | Focus indicators, underlines |
| `--color-bg` | `#FAFAF5` | Fundo principal |
| `--color-bg-alt` | `#F0EBE0` | Seções alternadas |
| `--color-text` | `#3E2723` | Texto principal |
| `--color-text-light` | `#6D4C41` | Texto secundário |
| `--color-white` | `#FFFFFF` | Fundo de cartões, texto sobre gradientes |

**Justificativa**: Tons terrosos (madeira) transmitem rusticidade e confiança; o verde-oliva representa sustentabilidade e natureza; o bege suaviza a experiência visual sem perder contraste.

### 3.2 Tipografia

- **Fonte principal**: Inter (Google Fonts)
  - Pesos utilizados: 400 (corpo), 500 (navegação), 600 (subtítulos), 700 (títulos)
  - Fallbacks: Roboto, Segoe UI, Helvetica, Arial, sans-serif
- **Tamanho base**: 16px
- **Escala modular**:
  - H1 hero: 2.5rem → 4.5rem (responsivo)
  - H2 seções: 2rem
  - H3 cards: 1.25rem
  - Corpo: 1rem → 1.3rem
  - Legenda/citação: 0.9rem → 0.95rem

**Justificativa**: Inter é uma fonte neutra, altamente legível em telas e com amplo suporte a pesos, ideal para interfaces modernas e acessíveis.

### 3.3 Layout e Espaçamento

- **Largura máxima**: 1200px (`--max-width`)
- **Sistema de espaçamento**: Escala baseada em `rem` (0.25rem → 6rem)
- **Grid responsivo**:
  - Mobile (<576px): 1 coluna
  - Tablet (576px–767px): 2 colunas
  - Desktop (≥768px): 4 colunas (produtos), 3 colunas (depoimentos)
- **Border radius**: 6px (sm), 12px (md), 16px (lg)
- **Sombras**: Sistema de 3 níveis (sm, md, lg)

---

## 4. Copywriting e Estratégia

### 4.1 Tom de Voz
- **Tom**: Acolhedor, transparente, profissional e inspirador.
- **Personalidade**: Uma marca que cuida de cada peça como se fosse da sua casa.

### 4.2 Estrutura de Conteúdo

| Seção | Objetivo |
|-------|----------|
| **Hero** | Impacto imediato: headline com diferencial (história + sustentabilidade + qualidade) + CTA claro |
| **Sobre Nós** | Construção de confiança: narrativa da curadoria e proposta de economia circular |
| **Produtos** | Apresentação das 4 categorias principais (Sofás, Mesas, Cadeiras, Armários) com benefícios específicos |
| **Depoimentos** | Prova social: 3 depoimentos de clientes de diferentes capitais |
| **FAQ** | Esclarecimento de objeções comuns (higienização, garantia, entrega, documentação) |
| **Contato** | Captura de leads via formulário |
| **CTA Final** | Chamada reforçada para conversão |

### 4.3 Estratégia de Conversão
- **CTAs estratégicos**: Dois pontos de conversão (Hero + seção final), ambos levando ao formulário de contato.
- **Redução de atrito**: Formulário enxuto (3 campos apenas).
- **Prova social**: Depoimentos com nomes e cidades.
- **Esclarecimento de objeções**: FAQ responde às principais inseguranças do comprador de usados.

---

## 5. SEO Implementado

### 5.1 Meta Tags Básicas

```html
<title>Móveis Usados São Paulo - Compre Móveis de Segunda Mão</title>
<meta name="description" content="Compre móveis usados de segunda mão com qualidade e garantia. Sofás, mesas, cadeiras e armários higienizados a preço baixo. Economia circular em cada peça.">
<link rel="canonical" href="https://www.moveisusados.com.br/">
```

### 5.2 Open Graph

```html
<meta property="og:title" content="Móveis Usados São Paulo - Compre Móveis de Segunda Mão">
<meta property="og:description" content="...">
<meta property="og:type" content="website">
<meta property="og:url" content="https://www.moveisusados.com.br/">
<meta property="og:image" content="https://www.moveisusados.com.br/assets/og-image.jpg">
<meta property="og:locale" content="pt_BR">
```

### 5.3 Twitter Cards

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="...">
<meta name="twitter:description" content="...">
<meta name="twitter:image" content="https://www.moveisusados.com.br/assets/og-image.jpg">
```

### 5.4 Schema.org (Dados Estruturados)

Foram implementados **3 tipos de schema** para enriquecer os resultados de busca:

1. **LocalBusiness** — Dados da empresa (nome, endereço, telefone, horário, faixa de preço).
2. **FAQPage** — Perguntas frequentes com respostas estruturadas (4 itens).
3. **ItemList + Product** — Catálogo de 4 produtos com preço, disponibilidade e URL.

### 5.5 Palavras-Chave Alvo
- Móveis usados São Paulo
- Móveis de segunda mão
- Sofás usados
- Mesas usadas
- Cadeiras usadas
- Armários usados
- Móveis higienizados
- Economia circular móveis

### 5.6 Acessibilidade e SEO Técnico
- HTML semântico (`header`, `main`, `section`, `article`, `nav`, `footer`)
- Atributos ARIA (`aria-label`, `aria-labelledby`)
- `lang="pt-BR"` no elemento `<html>`
- Links de pulo (skip-link) para navegação por teclado
- Imagens com atributos `alt` descritivos
- URL canônica definida

---

## 6. Resultados dos Testes

### 6.1 Responsividade

**Breakpoints testados**:

| Breakpoint | Largura | Layout |
|-----------|---------|--------|
| Mobile | < 576px | 1 coluna, fonte reduzida, espaçamento compacto |
| Tablet | 576px – 767px | 2 colunas (produtos e depoimentos) |
| Desktop | ≥ 768px | 4 colunas (produtos), 3 colunas (depoimentos) |
| Large Desktop | ≥ 1024px | Tipografia ampliada |
| Extra Large | ≥ 1200px | Título hero máximo (4.5rem) |

**Status**: Layout fluido em todos os breakpoints. Grid adaptativo com transições suaves.

### 6.2 Validação HTML/CSS
- HTML5 validado (estrutura DOCTYPE, charset UTF-8, tags semânticas).
- CSS sem erros de sintaxe; uso consistente de variáveis.
- Nenhum console error em testes manuais.

### 6.3 Compatibilidade
- **Navegadores**: Chrome, Firefox, Safari, Edge (testados via ferramentas de desenvolvedor).
- **CSS Grid e Flexbox**: Suporte universal nos navegadores modernos.
- **CSS Custom Properties**: Suporte total nos browsers atuais.
- **Google Fonts**: Carregamento assíncrono com fallbacks.

### 6.4 Acessibilidade
- Navegação por teclado funcional (skip-link, focus indicators).
- Contraste de cores adequado (WCAG AA compliant nos textos principais).
- Suporte a `prefers-reduced-motion` para usuários sensíveis a animações.

### 6.5 Issues Conhecidos (Pendentes de Correção - QA Rework)

Conforme identificado na revisão de QA, há **2 issues pendentes** que precisam ser resolvidas antes do fechamento final:

1. **Validação de formato de e-mail ausente** (`index.html:288`): O formulário usa `novalidate`, desativando a validação nativa do HTML5. O JavaScript atual verifica apenas campos vazios, não o formato do e-mail. É necessário adicionar uma validação de regex antes de aceitar o envio.

2. **Focus-visible styles incompletas** (`styles.css`): A regra `nav a:focus-visible` existe, mas faltam estilos `:focus-visible` para `.btn-cta` e controles de formulário (`input`, `textarea`). Usuários de teclado não conseguem identificar o foco ao navegar por botões e campos.

---

## 7. Como Acessar o Projeto

### 7.1 Pré-requisitos
- Navegador web moderno (Chrome, Firefox, Safari, Edge).

### 7.2 Acesso Local

```bash
# Navegue até o diretório do projeto
cd landing-page-moveis-usados/

# Abra o arquivo index.html no navegador
# Linux
xdg-open index.html

# macOS
open index.html

# Windows
start index.html
```

### 7.3 Acesso por Servidor Local (opcional)

```bash
# Python 3
python -m http.server 8000

# Node.js (npx)
npx serve .

# Acesse em http://localhost:8000
```

---

## 8. Próximos Passos

### 8.1 Correções Obrigatórias (QA Rework)
- [ ] Implementar validação de formato de e-mail no JavaScript do formulário.
- [ ] Adicionar estilos `:focus-visible` para `.btn-cta`, `input` e `textarea`.
- [ ] Re-executar testes de acessibilidade após as correções.

### 8.2 Melhorias Futuras (não-bloqueantes)
- [ ] Substituir placeholders SVG por fotografias reais dos produtos.
- [ ] Implementar integração com backend para envio real do formulário de contato.
- [ ] Adicionar página individual para cada categoria de produto.
- [ ] Implementar sistema de depoimentos dinâmicos.
- [ ] Adicionar Google Analytics ou alternativa para métricas de conversão.
- [ ] Otimizar imagens (WebP, lazy loading).
- [ ] Implementar PWA (Service Worker, manifest.json) para acesso offline.
- [ ] Adicionar多语言 suporte (i18n) para expansão internacional.

---

## 9. Considerações Finais

O projeto de landing page para venda de móveis usados foi desenvolvido com foco em **performance, acessibilidade e conversão**. A estrutura semântica, a paleta de cores cuidadosamente escolhida e a copywriting direcionada ao público-alvo formam uma base sólida para o lançamento.

As decisões técnicas priorizaram simplicidade e manutenibilidade, evitando dependências desnecessárias. O SEO on-page foi implementado com meta tags completas e dados estruturados (Schema.org), posicionando a página para bons resultados em motores de busca.

Após a conclusão dos ajustes de QA, o projeto estará pronto para deploy em ambiente de produção.

---

*Documento gerado em 01/08/2026.*
