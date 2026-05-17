# Landing Page — Melhorias Identificadas

## Diagnóstico Central

A página tem copy acima da média, mas **não prova nada**. É 100% texto e ícones — sem screenshot do produto, sem prova social, sem número de pessoas na lista. O visitante termina a página sem saber como o produto parece.

---

## Problemas por Categoria

### Visual
- **Tipografia sem contraste de peso** — título e subtítulo do hero ficam no mesmo range de peso. Referências como Linear usam bold pesado no título e quase-fino no subtítulo para criar ritmo
- **CTA principal usa azul, secundários usam laranja** — hierarquia de cores invertida. O accent (laranja) deveria estar no botão de maior importância
- **Seções alternadas quase indistinguíveis** — `--color-gray-50` é difícil de diferenciar do branco em telas comuns
- **Sem elementos visuais do produto** — zero mockup, screenshot ou vídeo. Nenhum SaaS relevante faz isso

### Copy & Conversão
- **H1 comunica categoria, não benefício** — "O suporte tecnológico para quem leva a consultoria online a sério" não cria imagem mental. O subtítulo está fazendo o trabalho do título
- **Duas seções de cards consecutivas redundantes** — "Diferenciais" e "Funcionalidades" comunicam a mesma coisa com visual idêntico, cria sensação de repetição
- **Gap de CTA entre features e Marketplace** — visitante convencido pelos 7 cards não encontra CTA imediato
- **`alert()` nativo para erro** — quebra o tom de produto profissional

### Estrutura do Funil
- **Sem prova social** — nenhum depoimento, número de usuários, logos ou qualquer validação externa entre a apresentação do produto e o CTA final
- **Sem seção "Como funciona"** — o visitante não consegue imaginar o fluxo real de uso
- **Menu com 5 itens** — excessivo para landing page. Linear tem 3

---

## Sugestões Priorizadas por Impacto

| # | Sugestão | Impacto | Esforço | Status |
|---|----------|---------|---------|--------|
| 1 | **Mockup/screenshot do produto** no hero ou logo abaixo | Alto | Médio (precisa de asset) | ✅ Implementado (mockup de painel ilustrativo no hero — redesign v2) |
| 2 | **Reescrever o H1** com benefício concreto | Alto | Baixo | ✅ Implementado ("O padrão operacional da consultoria online está sendo construído.") |
| 3 | **Prova social antes do formulário** — depoimento de beta tester, ou perfis de persona se não houver usuário | Alto | Baixo | Pendente (ainda sem depoimentos reais) |
| 4 | **Contador de pessoas na lista** — *"Já são X personal trainers na lista"* abaixo do CTA do hero | Médio-alto | Baixo | Pendente (precisa de número real) |
| 5 | **Inverter cores dos CTAs** — laranja no hero CTA primário | Médio | Baixo | ✅ Implementado (CTA primário laranja, secundários ghost) |
| 6 | **Unificar as duas seções de cards** em uma só, remover a redundância | Médio | Baixo | ✅ Implementado (substituídas por seção de pilares com tabs) |
| 7 | **Seção "Como funciona"** com 3 passos numerados | Médio | Baixo | ✅ Implementado (seção ICP "Para quem é" com 3 estágios numerados + pilares numerados) |
| 8 | **Substituir `alert()` por erro inline** no formulário | Médio | Baixo | ✅ Implementado (`.waitlist-error` aria-live abaixo do form) |
| 9 | **Reduzir menu** de 5 itens para 2-3 | Baixo | Baixo | ✅ Implementado (4 links navegacionais + 1 CTA laranja) |

---

## Melhorias Já Implementadas

| # | Melhoria |
|---|----------|
| ✅ | Removida logo duplicada no hero (liberou espaço above the fold no mobile) |
| ✅ | CTA do hero faz scroll direto para o formulário e auto-foca o campo de e-mail |
| ✅ | Botão de submit da waitlist trocado para `var(--color-accent)` (laranja) |
| ✅ | CTA "Entrar na lista" adicionado à barra de navegação |
| ✅ | CTA "Quero acesso antecipado" adicionado ao final da seção Marketplace |
| ✅ | Placeholder do input corrigido para `var(--color-gray-400)` (passa WCAG AA) |
| ✅ | Cores hardcoded removidas (`.coming-text`, `.coming-input::placeholder`, `.waitlist-popup-icon`) |
| ✅ | Micro-copy de urgência "Vagas limitadas para o acesso beta." adicionado no hero |
| ✅ | Copy da seção "O Problema" reescrita com framework PAS |
| ✅ | Redesign visual completo aplicado a partir do mockup do time de design (dark theme, Bebas Neue + Barlow + JetBrains Mono, mockup de painel, pilares com tabs, ICP, manifesto, FAQ) |
