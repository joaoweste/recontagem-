# Contagem de Estoque — app Android (Revalle Nordeste)

App Android (Capacitor) com a ferramenta de contagem/recontagem. Funciona offline; Excel e CSV são lidos dentro do próprio app.

## Como gerar o APK (sem instalar nada)
1. Crie um repositório no GitHub e envie todo o conteúdo desta pasta (já inclui `.github/workflows/apk.yml`).
2. No GitHub: aba **Actions → Gerar APK → Run workflow** (ou basta dar push na branch main).
3. Quando terminar (uns 5–8 min), abra a execução e baixe **contagem-estoque-apk** (contém `app-debug.apk`).
4. Passe o APK para o celular, permita "instalar apps desconhecidos" e instale.

## Ou, com Android Studio
`npm install` → `npx cap sync android` → `npx cap open android` → Build ▸ Build APK.

## Onde mexer
- `www/app.js` — toda a lógica. `www/index.html` e `www/style.css` — tela.
- `www/base.js` — base de 20.177 produtos (do Base_Produtos.csv). EAN veio em notação científica (7,89E+12) e foi descartado; reimporte na aba Produtos um arquivo com EAN em texto.
- Depois de mexer em `www/`: `npx cap sync android`.
