# Treinoway Landing Page — CLAUDE.md

## Visão Geral

Landing page de marketing da **Treinoway** — plataforma SaaS para personal trainers que fazem consultoria online. Objetivo principal: converter visitantes em leads (cadastro na lista de espera ou sign-up direto).

- URL: https://www.treinoway.com.br
- Deploy: GitHub Pages (branch `master`, domínio customizado via `CNAME`)
- Stack: HTML5 + CSS3 + JavaScript vanilla — **sem frameworks, sem build tools**

---

## Persona

**Personal trainer brasileiro** que:
- Atende alunos online (WhatsApp, planilhas, Google Drive)
- Quer profissionalizar e escalar a consultoria
- Sente dor com ferramentas amadoras e fluxos bagunçados
- Busca controle, imagem profissional e mais tempo

Toda copy deve falar diretamente com essa persona.

---

## Stack & Arquitetura

| Item | Detalhe |
|------|---------|
| Arquivo principal | `index.html` (HTML + CSS inline + JS inline) |
| Fonte | Exo 2 (Google Fonts — já carregada) |
| Ícones | SVG inline — sem bibliotecas externas |
| Imagens | `treino_way_transparente.png`, `treinoway.ico` |
| Deploy | GitHub Pages — push em `master` publica automaticamente |

**Regra crítica:** Não adicionar dependências externas, npm packages, ou frameworks.

---

## Design Tokens (CSS Variables)

Definidos em `:root` no `index.html`. **Sempre use as variáveis — nunca hardcode valores.**

```css
--color-primary:      #1e6fdb   /* Azul principal */
--color-primary-dark: #1554a6   /* Azul hover/pressed */
--color-accent:       #ff8a1f   /* Laranja — CTAs, destaques */
--color-dark:         #0f172a
--color-gray-900:     #111827
--color-gray-700:     #374151
--color-gray-600:     #4b5563
--color-gray-500:     #6b7280
--color-gray-400:     #9ca3af
--color-gray-200:     #e5e7eb
--color-gray-100:     #f3f4f6
--color-gray-50:      #f9fafb
--color-white:        #ffffff

--radius-sm:   0.5rem
--radius-md:   1rem
--radius-lg:   1.5rem
--radius-full: 999px

--shadow-card:       0 1px 3px rgba(0,0,0,0.06), 0 4px 12px rgba(0,0,0,0.04)
--shadow-card-hover: 0 4px 16px rgba(0,0,0,0.08), 0 14px 32px rgba(0,0,0,0.06)

--max-width:    1120px
--page-px:      1.25rem
--section-gap:  4.5rem
```

---

## Regras de Copy

1. **Idioma:** Todo texto visível ao usuário em **pt-BR**
2. **Tom:** Direto, confiante, sem jargão excessivo
3. **Foco em benefício:** "organize sua rotina" > "software de gestão"
4. **CTA principal:** Direciona para cadastro/sign-up na plataforma principal (treinoway-web)
5. **Hierarquia:** Um `<h1>` por página, `<h2>` para seções, `<h3>` para sub-itens

---

## Regras de SEO

- Manter todas as meta tags: `description`, `keywords`, `og:*`, `twitter:*`
- `<title>` deve conter a keyword principal e o nome da marca
- URL canônica: `https://www.treinoway.com.br/`
- `robots.txt` e `sitemap.xml` devem refletir a estrutura atual
- Alt text em todas as imagens, descritivo e em pt-BR

---

## Regras de CSS

- **Mobile-first:** estilos base para mobile, `@media (min-width: ...)` para desktop
- Não criar classes genéricas demais — escopo pelo componente
- Checar se uma classe existente já resolve antes de criar nova
- Breakpoints em uso: `640px` (sm), `768px` (md), `1024px` (lg)

---

## Estrutura de Seções (index.html)

| Seção | Propósito |
|-------|-----------|
| `<nav>` | Navegação fixa com logo e CTA |
| Hero | Headline principal + sub + CTA primário |
| Problema | Dores do personal trainer |
| Solução / Funcionalidades | O que a Treinoway resolve |
| Como funciona | Passo a passo |
| Prova social / Depoimentos | Credibilidade |
| Pricing / Planos (se houver) | Converter com oferta |
| FAQ | Reduzir objeções |
| Footer + CTA final | Última chance de conversão |

---

## Backend / Integrações

- O formulário de cadastro envia para a API em: `https://treinoway-service-production.up.railway.app`
- Qualquer mudança no endpoint deve ser feita com cuidado — verificar com o time antes

---

## Checklist antes de fazer commit

- [ ] Nenhum valor hardcoded (cores, fontes, espaçamentos) — usar variáveis CSS
- [ ] HTML válido e semântico
- [ ] Sem dependências externas novas
- [ ] Copy em pt-BR
- [ ] Meta tags SEO intactas
- [ ] Layout mobile verificado
- [ ] CTA principal visível acima do fold no mobile
