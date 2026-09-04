# Lista de Feira

App de lista de compras com controle de limite de gastos. Roda 100% no navegador, sem servidor — os dados (produtos, quantidade, valor e limite) ficam salvos no próprio aparelho, então a lista continua lá mesmo se a página for fechada ou atualizada sem querer.

## Colocar no ar com GitHub Pages

1. Crie um repositório novo no GitHub e envie o arquivo `index.html` para ele (pode subir só esse arquivo).
2. No repositório, vá em **Settings → Pages**.
3. Em **Branch**, selecione `main` e a pasta `/ (root)`, depois clique em **Save**.
4. Em alguns minutos o GitHub mostra o link do site, algo como `https://seu-usuario.github.io/nome-do-repositorio/`.

Abra esse link no celular e, se quiser, adicione à tela inicial — ele passa a abrir como um app.

## Rodar localmente antes de subir

Não precisa instalar nada: dá para abrir o `index.html` direto no navegador. Se preferir simular como ficaria no ar:

```
npx serve .
```

## Como foi feito

- React, Tailwind CSS e as fontes são carregados por CDN direto no HTML — não existe passo de build, então qualquer alteração no arquivo já reflete ao recarregar a página.
- Os dados ficam salvos no `localStorage` do navegador. Isso é por aparelho/navegador: a lista feita no celular não aparece automaticamente no computador, por exemplo.
