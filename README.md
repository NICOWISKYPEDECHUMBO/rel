# Processador de Guias Médicas

Este projeto foi estruturado como um projeto Vite para facilitar a publicação no GitHub e no Vercel. Os arquivos principais são:

- `index.html`: a aplicação web completa, com o código JavaScript embutido.
- `package.json`: define as dependências e os scripts do Vite para desenvolvimento (`npm run dev`), build de produção (`npm run build`) e preview (`npm run preview`).
- `vercel.json`: configura uma regra de rewrite para garantir que todas as rotas sejam encaminhadas ao `index.html`, permitindo que a aplicação funcione como uma SPA no Vercel.

## Como rodar localmente

1. Instale as dependências (é necessário ter Node.js instalado):
   ```sh
   npm install
   ```

2. Execute o servidor de desenvolvimento:
   ```sh
   npm run dev
   ```

   O Vite exibirá um endereço local (por exemplo, `http://localhost:5173`) onde você poderá testar a aplicação.

## Como publicar no GitHub Pages

Este projeto é um SPA estático, por isso você pode simplesmente enviar os arquivos para a branch configurada no GitHub Pages (por exemplo, `main` ou `gh-pages`). Certifique-se de que o arquivo `index.html` esteja na raiz da pasta usada para o Pages. O `package.json` e os demais arquivos não são servidos diretamente, mas são úteis para desenvolvimento local.

## Como implantar no Vercel

1. Crie um novo projeto no Vercel apontando para o repositório do GitHub que contém esta pasta.
2. No Vercel, escolha o framework **Other** e defina os seguintes comandos:
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
3. O arquivo `vercel.json` incluído já contém um rewrite para direcionar todas as rotas para `index.html`, o que é necessário para aplicações SPA.

Depois do deploy, o Vercel servirá o conteúdo da pasta `dist` com base no build feito pelo Vite.

