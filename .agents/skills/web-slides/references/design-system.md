# Design System & Padrões — Leandro Leite Tech Slides

## 🎨 Paleta de Cores & Tokens

| Token | Dark Mode | Light Mode | Descrição / Uso |
| :--- | :--- | :--- | :--- |
| `--bg-dark` | `#07090e` | `#f8fafc` | Fundo principal da página |
| `--bg-surface` | `#0d121f` | `#ffffff` | Fundo de containers e menus |
| `--bg-card` | `rgba(18, 24, 38, 0.7)` | `rgba(255, 255, 255, 0.85)` | Cards translúcidos em glassmorphism |
| `--accent-sky` | `#38bdf8` | `#0284c7` | Azul ciano de destaque primário |
| `--accent-purple` | `#8b5cf6` | `#7c3aed` | Roxo elétrico para gradientes |
| `--accent-orange` | `#ff6200` | `#ea580c` | Laranja de destaque (Itaú brand) |
| `--accent-emerald` | `#10b981` | `#059669` | Verde de sucesso e badges ativas |
| `--border-subtle` | `rgba(255, 255, 255, 0.08)` | `rgba(0, 0, 0, 0.08)` | Bordas finas |

---

## 🔤 Tipografia

- **Títulos & Headings**: `Plus Jakarta Sans`, 700 / 800 / 900
- **Corpo & Texto**: `Inter`, 400 / 500 / 600
- **Código & Terminal**: `JetBrains Mono`, 400 / 500 / 700

---

## 🧩 Componentes do Template

### 1. Slide de Capa de Evento (Banner Oficial)
```html
<section class="slide active" data-title="Capa do Evento" data-notes="Slide de abertura">
  <div class="slide-content-wrapper">
    <div class="cover-image-wrapper">
      <div class="cover-image-card">
        <img src="./assets/capa-evento.jpeg" alt="Capa Oficial" class="cover-image-banner">
      </div>
    </div>
  </div>
</section>
```

### 2. Slide Sobre Mim (Leandro Leite)
```html
<div class="profile-card">
  <div class="profile-main-grid">
    <!-- Foto Retrato -->
    <div class="profile-portrait-card">
      <img src="./assets/profile.jpeg" alt="Leandro Leite" class="profile-portrait-img">
    </div>

    <!-- Conteúdo Direto -->
    <div class="profile-right-content">
      <div class="profile-header-info">
        <h2 class="speaker-name">Prazer, sou o <span class="gradient-text">Leandro Leite</span></h2>
        <p class="speaker-role">AI-Augmented Engineer & Palestrante de Tecnologia</p>
      </div>

      <div class="bio-vertical-list">
        <div class="bio-list-row">
          <span class="bio-bullet"></span>
          <div class="bio-text">Engenheiro de Software — <span class="itau-badge">Itaú Unibanco</span></div>
        </div>
        <div class="bio-list-row">
          <span class="bio-bullet"></span>
          <div class="bio-text">Focado em soluções <strong>Java</strong> & <strong>Cloud Native</strong></div>
        </div>
        <div class="bio-list-row">
          <span class="bio-bullet"></span>
          <div class="bio-text">Coordenador <span class="soujava-badge">SouJava</span> & <strong>Dev’s Fora da Curva</strong></div>
        </div>
        <div class="bio-list-row">
          <span class="bio-bullet"></span>
          <div class="bio-text">Membro ativo e palestrante da comunidade tech</div>
        </div>
        <div class="bio-list-row">
          <span class="bio-bullet"></span>
          <div class="bio-text">Pai e Marido (25 anos)</div>
        </div>
        <div class="bio-list-row">
          <span class="bio-bullet"></span>
          <div class="bio-text">Entusiasta na criação de cavalos (desde a infância)</div>
        </div>
      </div>
    </div>
  </div>

  <!-- Links no Rodapé -->
  <div class="profile-footer-links">
    <a href="https://linkedin.com/in/leandroleitetech" target="_blank" class="footer-social-pill">
      <span>linkedin.com/in/leandroleitetech</span>
    </a>
    <a href="https://leandroleitetech.com" target="_blank" class="footer-social-pill">
      <span>leandroleitetech.com</span>
    </a>
    <a href="https://github.com/leandroleitetech" target="_blank" class="footer-social-pill">
      <span>github.com/leandroleitetech</span>
    </a>
  </div>
</div>
```

### 3. Grids de Conteúdo
- `.grid-2`: 2 colunas proporcionais (ideal para comparativos).
- `.grid-3`: 3 colunas (ideal para agenda e pilares).
- `.grid-4`: 4 colunas (cards rápidos ou métricas).

### 4. Bloco de Código / Prompt Copiável
```html
<div class="code-box">
  <div class="code-header">
    <div class="code-dots">
      <div class="code-dot red"></div>
      <div class="code-dot yellow"></div>
      <div class="code-dot green"></div>
    </div>
    <span class="code-lang">prompt-template.md</span>
    <button class="copy-btn" onclick="copySnippet(this)">
      <span>Copiar</span>
    </button>
  </div>
  <pre class="code-content"><code>// Conteúdo ou prompt copiável aqui</code></pre>
</div>
```
