---
name: web-slides
description: >-
  Cria e customiza apresentações técnicas interativas em HTML/CSS/JS em arquivo único
  no padrão visual Leandro Leite Tech (suporte a passador de slides, teclado, tela cheia,
  notas de orador, visualizador em grid, temas modernos dark/glassmorphism e snippets copiáveis).
---

# Web Slides — Criação de Apresentações Interativas

Use esta skill para criar apresentações de slides modernas, fluidas e autossuficientes em **um único arquivo HTML** para palestras, workshops e meetups técnicos.

## 🌟 Características do Formato

Todas as apresentações geradas seguem o **Design System Leandro Leite Tech**:
- **Zero Build / Standalone**: Funciona abrindo diretamente o arquivo `.html` no navegador ou servido no GitHub Pages.
- **Suporte a Controle Passador & Teclado**:
  - `→`, `↓`, `Espaço`, `PageDown`, `N` para avançar.
  - `←`, `↑`, `Backspace`, `PageUp`, `P` para retroceder.
  - `F` ou `F5` para alternar modo Tela Cheia.
  - `S` para abrir as Notas do Apresentador (*Speaker Notes*).
  - `O` ou `Esc` para abrir o Visão Geral / Grid View dos slides.
  - `B` para Black Screen / tela preta e `W` para White Screen.
  - Suporte a toque/deslize (*swipe touch*) em tablets e smartphones.
- **Blocos de Código & Prompts Copiáveis**: Botão interativo com feedback visual ("Copiar" -> "Copiado!").
- **Design Moderno**: Tema dark profundo, glassmorphism com backdrop blur, gradientes cyan/purple/orange (Itaú), tipografia limpa (Inter & Plus Jakarta Sans).

---

## 🛠️ Como Criar uma Nova Apresentação

1. **Definir a Localização**:
   - Crie a pasta da palestra dentro do tema correspondente: `<categoria>/<nome-da-talk>/`.
   - Exemplo: `ai/deep-dive-agentes/index.html` ou `cloud/arquitetura-serverless/index.html`.

2. **Utilizar o Template Base**:
   - Copie a estrutura de [template.html](./resources/template.html).
   - Ajuste título, tags, bio do palestrante e lista de slides.

3. **Estrutura de Cada Slide**:
   Cada slide é uma tag `<section class="slide" data-title="Título Resumido" data-notes="Anotações para o orador...">`:
   ```html
   <section class="slide" data-title="Visão Geral" data-notes="Explicar o conceito X e enfatizar o benefício Y">
     <div class="slide-content-wrapper">
       <span class="slide-tag">🏷️ Categoria / Tópico</span>
       <h2 class="slide-title">Título com <span class="gradient-text">Destaque</span></h2>
       <p class="slide-subtitle">Subtítulo explicativo ou contexto direto.</p>

       <!-- Layouts disponíveis: .grid-2, .grid-3, .grid-4, .card, .code-box, etc. -->
       <div class="grid-2">
         <div class="card">...</div>
         <div class="card">...</div>
       </div>
     </div>
   </section>
   ```

4. **Gerar README da Palestra & Atualizar Catálogo**:
   - Crie um arquivo `README.md` na pasta da palestra com resumo, data/evento e atalhos.
   - Atualize a tabela de apresentações no `README.md` principal do repositório.
