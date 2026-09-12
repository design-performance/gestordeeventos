# Como publicar

Todos os arquivos vão **na raiz** do repositório `design-performance/gestordeeventos`. Nada de subpasta.

## Arquivos e o que cada um é

| Arquivo | O que é | Endereço final |
| --- | --- | --- |
| `index.html` | Landing page (a porta de entrada) | `design-performance.github.io/gestordeeventos/` |
| `app.html` | O aplicativo | `.../gestordeeventos/app.html` |
| `termos.html` | Termos de uso | `.../gestordeeventos/termos.html` |
| `privacidade.html` | Política de privacidade | `.../gestordeeventos/privacidade.html` |
| `manifest.webmanifest` | Faz instalar como app | — |
| `service-worker.js` | Cache e funcionamento offline | — |
| `icon-192.png` / `icon-512.png` | Ícones de instalação | — |

## Passo a passo

1. Abra `github.com/design-performance/gestordeeventos`
2. **Add file → Upload files**
3. Arraste **todos** os arquivos desta pasta (menos este `COMO-PUBLICAR.md`)
4. Confirme a substituição do `index.html` e do `service-worker.js`
5. **Commit changes**

Se ainda existirem no repositório, apague: `cobranca-anual.png` e `cobranca-mensal.png` (essas eram só para subir no Asaas).

## Conferir se deu certo

1. Abra `design-performance.github.io/gestordeeventos/` — deve aparecer a **landing page**, não o app
2. Clique em "Começar grátis" — abre o app
3. Na tela de entrada do app, embaixo, deve aparecer **v11**
4. Abra `.../gestordeeventos/privacidade.html` — é este link que vai para o Google

Se aparecer a versão antiga: feche todas as abas do site, limpe os dados dele no navegador e abra de novo. Quem já instalou o app na tela de início deve desinstalar e instalar outra vez.

## Uma mudança importante

Antes, o endereço principal abria o app. Agora abre a **landing page**, e o app fica em `/app.html`.

Quem já instalou o app na tela de início continua caindo direto no aplicativo — a landing detecta isso e redireciona sozinha.

## Depois de publicar

1. **Google Cloud** → na tela de permissão OAuth, preencha o campo de política de privacidade com `https://design-performance.github.io/gestordeeventos/privacidade.html`
2. Mesma tela → **Publicar app** → **Preparar para verificação** (tira o aviso de "app não verificado" e o limite de 100 usuários)
3. Leve os termos a um advogado antes do primeiro cliente pagante
4. Mande a landing para 10 produtores de evento
