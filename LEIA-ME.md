# Ícone do Finanças no celular (página de entrada no GitHub Pages)

O iPhone e o Android pegam o ícone da página do Google, que não controlamos. Esta pasta cria um endereço fixo com a logo do Finanças como ícone; ao tocar, abre o app. Mesmo esquema usado no VRF Caixa.

Arquivos: `index.html` (página de entrada), `manifest.webmanifest` (nome e ícones para Android), `apple-touch-icon.png` (iPhone, 180px), `icon-192.png`, `icon-512.png`, `favicon.png`, `logo.svg` (original vetorial).

## Antes de subir
Abra `index.html` no Bloco de Notas e confira a linha `var APP_URL = "..."`. Tem que ser exatamente o "URL do app da Web" do Apps Script, o que termina em `/exec`.

## Publicar no GitHub (você já tem a conta Mvelani-1985)
Opção A, endereço curto `https://financas-mv.github.io/` (igual ao que foi feito para a VRF):
1. Logado no GitHub, foto do perfil (canto superior direito) › **Your organizations** › **New organization** › plano Free. Nome: `financas-mv` (ou outro livre). Conclua.
2. Dentro da organização: **New repository**. Nome exatamente `financas-mv.github.io` (o mesmo nome da organização + `.github.io`). Public. Marque **Add a README file**. **Create repository**.
3. **Add file › Upload files**. Arraste os 7 arquivos desta pasta (não a pasta). **Commit changes**.
4. Aguarde 1 a 2 minutos. O endereço `https://financas-mv.github.io/` passa a abrir a página de entrada. Repositórios com esse nome publicam sozinhos, sem configurar Pages.

Opção B, dentro da sua conta: repositório `financas` em Mvelani-1985, **Settings › Pages › Deploy from a branch › main / (root) › Save**. Endereço: `https://mvelani-1985.github.io/financas/`.

## No celular
- iPhone (Safari): abra o endereço, toque em **Compartilhar › Adicionar à Tela de Início**. O ícone é a logo azul com a seta. Ao tocar, abre o app direto.
- Android (Chrome): menu ⋮ › **Adicionar à tela inicial**.

Como funciona: aberta pelo link, a página fica parada mostrando o botão e as instruções, para dar tempo de instalar. O ícone criado guarda `?go=1`; aberta por ele, a página pula direto para o app.

## Favicon no próprio app (aba do navegador no computador)
Depois de publicar, copie o endereço do `favicon.png` (ex.: `https://financas-mv.github.io/favicon.png`) e cole na aba **Config** da planilha, na chave `favicon_url`. O app passa a mostrar a logo na aba do navegador. Precisa de uma nova versão da implantação para valer.

## Se o link do app mudar
Só muda se você criar uma implantação nova em vez de "Nova versão". Nesse caso, edite `index.html` no GitHub (lápis), troque o `APP_URL`, **Commit changes**. O ícone no celular continua funcionando sem reinstalar.
