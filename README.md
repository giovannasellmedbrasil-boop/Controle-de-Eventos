# Controle de Eventos 2026 — Sellmed

App estático (um único `index.html`, sem servidor, sem build). Para publicar no Vercel:

## Opção 1 — Arrastar e soltar (mais simples)

1. Acesse https://vercel.com/new
2. Procure a opção de fazer upload de uma pasta (deploy sem Git) e arraste esta pasta inteira (`Controle de Eventos - App`).
3. Confirme o deploy. O Vercel detecta automaticamente que é um site estático (sem framework) e publica o `index.html` na raiz.
4. Você recebe uma URL do tipo `https://controle-de-eventos-app.vercel.app` — acessível de qualquer aparelho, sem precisar estar logada em nada.

## Opção 2 — Vercel CLI

```bash
npm i -g vercel
cd "Controle de Eventos - App"
vercel --prod
```

Siga as perguntas (login na Vercel, nome do projeto) e ele publica.

## Opção 3 — GitHub + Vercel

1. Suba esta pasta para um repositório no GitHub.
2. Em vercel.com, clique "Add New Project" → "Import Git Repository" → selecione o repositório.
3. Deploy automático a cada alteração que você enviar ao repositório.

## Importante sobre os dados

Este app salva tudo (checklist, anotações, anexos, cotas, datas etc.) no **armazenamento local do navegador** (localStorage) de cada aparelho. Isso significa:

- Depois de publicado no Vercel, todos os aparelhos acessam o **mesmo app**, mas cada um guarda seus **próprios dados** — editar no celular não aparece automaticamente no computador.
- Não há um servidor guardando os dados centralizadamente.
- Recomendado: sempre usar o mesmo navegador/aparelho como "principal", ou pedir para reimplementar sincronização em nuvem depois, se isso virar um problema no dia a dia.
