# Gestor de Eventos

App mobile (PWA) para quem produz eventos: agenda mensal/anual, cadastro e edição direta de eventos, controle de gastos por categoria e painel comparativo entre períodos.

## O que já funciona

- **Agenda** — visões de Mês, Semana, Ano e Lista. Toque num dia vazio cria evento; segurar e arrastar um evento muda a data; cores por tipo; dias bloqueados.
- **Ano** — 12 mini-meses com contagem de eventos e barra de ocupação.
- **Edição direta no card** — nome, tipo, status, data, hora, local, cliente, convidados, equipe, orçamento, fornecedores, anexos, notas e checklist.
- **Financeiro** — lançamento de gastos por categoria (Buffet, Estrutura, Som & Luz, Equipe, Marketing, Deslocamento, Outros), total automático, % do orçamento e alerta de estouro.
- **Painel** — KPIs com variação, gráfico ano a ano, comparação livre entre quaisquer dois meses ou anos, "Onde o dinheiro foi", custo médio por evento e por convidado, mix de tipos, alertas e próximos eventos.

## Rodar localmente

```bash
npx serve .
```

Abra o endereço mostrado no terminal. Em celular, use "Adicionar à tela de início" para instalar como app.

## Publicar

**GitHub Pages** — Settings → Pages → Source: `main` / root. O app fica em `https://<org>.github.io/gestordeeventos/`.

**Vercel** — importe o repositório, sem build step, output directory = raiz.

## Estado atual

Protótipo de produto: os dados são gerados em memória (2025–2026) e não persistem. Próximos passos para virar produto vendável:

1. **Contas e login** — Supabase Auth (e-mail/senha + Google).
2. **Dados na nuvem** — Postgres com tabelas `eventos`, `gastos`, `tarefas`, `usuarios`, `assinaturas`; RLS obrigatório para isolar dados por usuário.
3. **Cobrança** — Asaas (Pix/cartão/boleto) ou Stripe; teste de 14 dias sem cartão, planos mensal e anual.
4. **Telas faltantes** — cadastro/login, onboarding, planos, paywall, minha conta, convidar equipe, exportar relatório em PDF.

## Estrutura

| Arquivo | Papel |
| --- | --- |
| `index.html` | App |
| `manifest.webmanifest` | Metadados PWA (nome, ícones, cor) |
| `service-worker.js` | Cache offline |
| `icon-192.png`, `icon-512.png` | Ícones de instalação |
