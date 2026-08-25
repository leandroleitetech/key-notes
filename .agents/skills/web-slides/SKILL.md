---
name: web-slides
description: >-
  Cria e customiza apresentações técnicas interativas em HTML/CSS/JS em arquivo único
  no padrão visual Leandro Leite Tech (suporte a passador de slides, teclado, tela cheia,
  notas de orador, visualizador em grid, temas modernos dark/glassmorphism, modo claro/escuro,
  capa de evento e snippets copiáveis).
---

# Web Slides — Criação de Apresentações Interativas

Use esta skill para criar apresentações de slides modernas, fluidas e autossuficientes em **um único arquivo HTML** para palestras, workshops e meetups técnicos no padrão visual oficial de **Leandro Leite**.

## 🌟 Características & Funcionalidades

Todas as apresentações geradas seguem o **Design System Leandro Leite Tech**:
- **Zero Build / Standalone**: Funciona abrindo diretamente o arquivo `.html` no navegador ou servido no GitHub Pages sem nenhuma dependência de build.
- **Modo Claro & Escuro (Dark / Light Mode)**:
  - Alternância instantânea via tecla **`T`** ou botão no topo, persistido em `localStorage`.
- **Suporte Completo a Passador de Slides & Teclado**:
  - `→`, `↓`, `Espaço`, `PageDown`, `N` para avançar.
  - `←`, `↑`, `Backspace`, `PageUp`, `P` para retroceder.
  - `T` para alternar modo Claro / Escuro.
  - `F` ou `F5` para alternar modo Tela Cheia (*Fullscreen*).
  - `S` para abrir as Notas do Apresentador (*Speaker Notes*).
  - `O` ou `Esc` para abrir o Visão Geral / Grid View de todos os slides.
  - `B` para Blackout (tela preta) e `W` para Whiteout (tela branca).
  - Suporte a toque/deslize (*swipe touch*) em dispositivos móveis e tablets.
- **Slide de Capa do Evento**: Suporte a banner oficial com emolduramento em gradiente e sombra suave.
- **Slide Sobre Mim**: Layout com foto ampla em formato retrato à esquerda, lista de qualificações diretas à direita e links de redes sociais no rodapé.
- **Blocos de Código & Prompts Copiáveis**: Botão interativo com feedback visual ("Copiar" -> "Copiado!").
- **Design Moderno**: Glassmorphism com `backdrop-filter`, luzes ambiente, gradientes cyan/purple/orange (Itaú), e tipografia *Plus Jakarta Sans*, *Inter* e *JetBrains Mono*.

---

## 🛠️ Procedimento para Nova Apresentação

1. **Definir a Pasta da Palestra**:
   - Crie a pasta correspondente: `<categoria>/<nome-da-talk>/`.
   - Exemplo: `ai/devin/index.html` ou `cloud/arquitetura-serverless/index.html`.

2. **Copiar o Template Base**:
   - Utilize o arquivo [template.html](./resources/template.html).
   - Preencha o título da palestra, tags, banners e tópicos.

3. **Componentes Padrão Disponíveis**:
   Consulte a documentação em [references/design-system.md](./references/design-system.md) para os modelos de:
   - Capa de evento (`.cover-image-card`)
   - Perfil do Orador (`.profile-card`, `.profile-portrait-card`, `.bio-vertical-list`)
   - Grids de 2, 3 e 4 colunas (`.grid-2`, `.grid-3`, `.grid-4`)
   - Box de código copiável (`.code-box`, `.copy-btn`)

4. **Gerar README da Palestra & Atualizar Catálogo**:
   - Crie um arquivo `README.md` na pasta da palestra com atalhos de apresentação e resumo.
   - Atualize a tabela do catálogo no `README.md` raiz do repositório.
