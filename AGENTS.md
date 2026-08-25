# AGENTS.md — Diretrizes para Agentes de IA

Este documento define padrões, estrutura organizacional e diretrizes operacionais para Agentes de IA (como Antigravity, Claude, ChatGPT, Cursor, Devin, etc.) que interagem com o repositório **key-notes**.

---

## 🎯 Objetivo do Repositório

O repositório **key-notes** é o hub central de apresentações, palestras, workshops e notas de suporte de **Leandro Leite**.
O objetivo é organizar, catalogar e facilitar o compartilhamento de apresentações em múltiplos formatos para a comunidade e eventos.

---

## 📂 Estrutura de Diretórios e Organização

O repositório é categorizado por **tópicos técnicos / temas** no nível raiz:

```text
key-notes/
├── AGENTS.md                     # Este arquivo (guia para agentes e automações)
├── LICENSE                       # Licença MIT
├── README.md                     # Catálogo público e índice das apresentações
├── <categoria>/                  # Ex: ai/, java/, cloud/, architecture/, devops/
│   └── <nome-da-apresentacao>/   # Pasta do evento ou palestra (ou arquivo direto se simples)
│       ├── README.md             # (Opcional) Resumo da talk, data, evento e links
│       ├── slides.key            # Arquivo Apple Keynote
│       ├── slides.pptx           # Arquivo Microsoft PowerPoint
│       ├── slides.pdf            # Export em PDF (ideal para compartilhamento rápido)
│       ├── index.html            # Apresentação web (Reveal.js, Marp, Slidev, etc.)
│       └── assets/               # Imagens, diagramas e mídias usadas
```

### Categorias Existentes e Sugeridas:
- `ai/` — Inteligência Artificial, LLMs, Agentes Autônomos, Engenharia de Prompt, MLOps.
- `java/` — Ecossistema Java, Spring, Quarkus, GraalVM, JVM internals, Serverless.
- `cloud/` — AWS, GCP, Azure, Arquitetura Serverless, Cloud Native.
- `architecture/` — Arquitetura de Software, Microsserviços, Design Patterns, DDD, Event-Driven.
- `devops/` — CI/CD, Kubernetes, Docker, Observabilidade, Infra as Code.

---

## 📄 Formatos Suportados e Recomendações

| Formato | Extensão | Descrição & Uso | Boas Práticas |
| :--- | :--- | :--- | :--- |
| **Apple Keynote** | `.key` | Formato nativo do macOS para apresentações ricas e animações fluidas. | Sempre que possível, disponibilizar também um export `.pdf` para não usuários de Mac. |
| **PowerPoint** | `.pptx` / `.ppt` | Padrão corporativo e compatível com Google Slides. | Manter fontes padrão ou embutidas para evitar quebra de layout. |
| **Web / HTML** | `.html` | Slides baseados em web (Reveal.js, Marp, Slidev, HTML/CSS). | Manter assets locais ou com links CDN estáveis para funcionamento offline. |
| **PDF** | `.pdf` | Export estático para distribuição, visualização no GitHub e compartilhamento rápido. | Recomendado como export complementar para qualquer deck `.key` ou `.pptx`. |
| **Markdown / Notas** | `.md` | Roteiros de fala, anotações de orador (*speaker notes*) e referências. | Incluir referências, links externos e código de exemplo na pasta da palestra. |

---

## 🤖 Papéis e Fluxos de Trabalho do Agente

Ao receber instruções para manipular este repositório, o Agente de IA deve seguir estes fluxos:

### 1. Adicionar uma Nova Apresentação
1. Identificar ou solicitar a **categoria** correta (ex: `ai/`, `java/`, `cloud/`). Se não existir, criar a pasta da categoria com nome em minúsculas e hifens se necessário.
2. Definir nome claro e semântico para a pasta ou arquivo:
   - Formato recomendado para pastas de talks: `kebab-case` (ex: `ai/devin-software-engineer/`, `java/java-no-mundo-serverless/`).
3. Se fornecido apenas o arquivo fonte (`.key` ou `.pptx`):
   - Sugerir/gerar a exportação para `.pdf` para visualização rápida no GitHub.
4. Adicionar ou atualizar um `README.md` contextual na pasta da apresentação se houver detalhes do evento (data, evento, resumo, links).
5. **Atualizar o `README.md` principal** adicionando a nova talk na tabela de catálogo.

### 2. Atualizar o Catálogo no `README.md`
Sempre que uma apresentação for adicionada, renomeada ou removida:
- Manter o índice categorizado atualizado.
- Incluir colunas: **Tema / Título**, **Formatos Disponíveis**, **Descrição Resumida**, **PDF / Link**.

### 3. Criar Apresentações em HTML / Web Slides
Se o usuário solicitar a criação de uma nova apresentação do zero:
- Considerar frameworks leves em HTML (como **Reveal.js** via CDN ou template autossuficiente em arquivo único) para fácil abertura direta no navegador sem necessidade de build complexo.
- Garantir responsividade e modo tela cheia (`F`).

### 4. Boas Práticas de Versionamento
- **Arquivos Grandes**: Se arquivos `.key` ou `.pptx` ultrapassarem 50MB-100MB, alertar sobre o uso de Git LFS (Large File Storage) ou links para nuvem/drive.
- **Commits Semânticos**: Usar mensagens claras, por exemplo:
  - `feat(java): add serverless java presentation deck and pdf`
  - `docs(readme): update presentations catalog table`
  - `feat(ai): add devin overview html presentation`

---

## 📋 Convenções de Nomenclatura

- **Pastas de Categorias**: `kebab-case` minúsculo (ex: `ai`, `java`, `cloud-native`, `software-architecture`).
- **Pastas de Apresentações**: `kebab-case` minúsculo (ex: `devin-agente-ia`, `java-mundo-serverless`).
- **Arquivos**:
  - Preferencialmente descritivos: `Titulo_Da_Apresentacao.key` ou `slides.key` / `slides.pdf` se dentro de pasta própria.
  - Evitar caracteres especiais, acentos em nomes de arquivos gerados programaticamente ou usar UTF-8 consistente.

---

## 💡 Comandos Úteis

```bash
# Listar todas as apresentações organizadas por formato
find . -type f \( -name "*.key" -o -name "*.pptx" -o -name "*.ppt" -o -name "*.pdf" -o -name "*.html" \) ! -path "*/.git/*"

# Verificar tamanho dos arquivos de apresentação
du -sh */*
```
