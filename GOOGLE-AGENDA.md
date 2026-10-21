# Ativar "Puxar do Google Agenda"

O botão já está no app (Seus dados → Puxar do Google Agenda). Para funcionar para todo mundo:

## 1. Ligar a API
console.cloud.google.com → seu projeto → **APIs e serviços → Biblioteca** → busque **Google Calendar API** → **Ativar**.

## 2. Adicionar o escopo
**APIs e serviços → Tela de permissão OAuth (Google Auth Platform) → Acesso a dados → Adicionar ou remover escopos** → marque:
`https://www.googleapis.com/auth/calendar.events.readonly` → Salvar.

## 3. Pedir verificação
**Central de verificação → Preparar para verificação**. O Google vai pedir:
- Link da política de privacidade: `https://design-performance.github.io/gestordeeventos/privacidade.html` (já atualizada com o uso da agenda)
- Justificativa (pode colar): "O app lê os compromissos do usuário apenas quando ele toca em 'Puxar do Google Agenda', mostra a lista para ele escolher quais viram eventos, e salva somente os escolhidos no próprio aparelho/Drive do usuário. Somente leitura, sem servidor próprio."
- **Vídeo** (YouTube, não listado, 1–2 min): mostre a tela de permissão do Google aparecendo, a lista de compromissos, marcar alguns e tocar em Importar.

Prazo típico: 2 a 6 semanas.

## Enquanto não aprovam
Funciona para até 100 pessoas, com aviso "app não verificado" (tocar em Avançado → Continuar). Para testar só você: **Público-alvo → Usuários de teste → adicionar seu e-mail**.
