# Design System & Padrões — Leandro Leite Tech Slides

## 🎨 Paleta de Cores & Tokens

| Token | Valor CSS | Descrição / Uso |
| :--- | :--- | :--- |
| `--bg-dark` | `#07090e` | Fundo principal ultra dark |
| `--bg-surface` | `#0d121f` | Fundo de containers e menus |
| `--bg-card` | `rgba(18, 24, 38, 0.7)` | Fundo translúcido com glassmorphism |
| `--accent-sky` | `#38bdf8` | Azul ciano de destaque primário |
| `--accent-purple` | `#8b5cf6` | Roxo elétrico para gradientes |
| `--accent-orange` | `#ff6200` | Laranja de destaque (Itaú brand) |
| `--accent-emerald` | `#10b981` | Verde de sucesso e badges ativas |
| `--border-subtle` | `rgba(255, 255, 255, 0.08)` | Bordas finas e elegantes |

---

## 🔤 Tipografia

- **Títulos & Headings**: `Plus Jakarta Sans`, 700 / 800 / 900
- **Corpo & Texto**: `Inter`, 400 / 500 / 600
- **Código & Terminal**: `JetBrains Mono`, 400 / 500 / 700

---

## 🧩 Componentes Disponíveis

### 1. Slide Wrapper
```html
<section class="slide" data-title="Nome do Slide" data-notes="Roteiro de fala">
  <div class="slide-content-wrapper">
    <span class="slide-tag">🏷️ Tag</span>
    <h2 class="slide-title">Título <span class="gradient-text">Gradiente</span></h2>
    <p class="slide-subtitle">Texto de apoio</p>
    ...
  </div>
</section>
```

### 2. Grids de Conteúdo
- `.grid-2`: 2 colunas proporcionais.
- `.grid-3`: 3 colunas (ideal para pilares e tópicos de agenda).
- `.grid-4`: 4 colunas (cards compactos ou métricas).

### 3. Cards & Glassmorphism
```html
<div class="card">
  <div class="card-icon">🚀</div>
  <h3 class="card-title">Título do Card</h3>
  <p class="card-desc">Descrição explicativa.</p>
</div>
```

### 4. Bloco de Código com Botão Copiar
```html
<div class="code-box">
  <div class="code-header">
    <div class="code-dots">
      <div class="code-dot red"></div>
      <div class="code-dot yellow"></div>
      <div class="code-dot green"></div>
    </div>
    <span class="code-lang">arquivo.ext</span>
    <button class="copy-btn" onclick="copySnippet(this)">
      <span>Copiar</span>
    </button>
  </div>
  <pre class="code-content"><code>// Seu código ou prompt aqui</code></pre>
</div>
```
