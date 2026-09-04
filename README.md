# Cédula de Ideias — Eixos & Posições (Eleição Presidencial)

Ferramenta pedagógica para os alunos compararem suas próprias posições políticas com as de 13 candidatos à Presidência, sem saber de antemão de quem é cada posição.

## Arquivos

- **`index.html`** — a cédula que os alunos respondem (40 perguntas, 4 eixos, termômetro Estado × Mercado, resultado exportável).
- **`professor.html`** — o painel onde você importa os resultados baixados pelos alunos e vê tudo agregado por turma.
- **`README.md`** — este arquivo.

## Fluxo de uso em sala

1. Você compartilha o link de `index.html` com a turma (ver publicação abaixo).
2. Cada aluno preenche **nome (opcional) e turma (obrigatório)**, responde e, no final, clica em **"Baixar meu resultado"** — isso baixa um arquivo `.json` pequeno.
3. Os alunos te enviam esse arquivo (Classroom, e-mail, WhatsApp, pen-drive — como preferir).
4. Você abre `professor.html` no seu computador e arrasta todos os `.json` recebidos para dentro. O painel agrega tudo por turma: ranking de convergência, candidato mais citado por eixo, termômetro médio, e uma tabela individual.

**Nada é enviado para nenhum servidor** — tanto a cédula quanto o painel rodam inteiramente no navegador. Os arquivos `.json` só existem no dispositivo do aluno e no seu, então não há necessidade (nem função) de login, banco de dados ou conexão com a internet depois de carregada a página.

## Como publicar no GitHub Pages (sem programar)

1. Crie uma conta em [github.com](https://github.com) se ainda não tiver.
2. Clique em **"New repository"** (Novo repositório). Dê um nome, ex.: `cedula-de-ideias`. Marque como **Public**. Não marque "Add a README" (você já tem um).
3. Na tela do repositório recém-criado, clique em **"uploading an existing file"** (ou "Add file" → "Upload files").
4. Arraste os três arquivos (`index.html`, `professor.html`, `README.md`) para a área de upload e clique em **"Commit changes"**.
5. Vá em **Settings** (do repositório) → **Pages** (menu lateral).
6. Em "Source", selecione **"Deploy from a branch"**, branch **`main`**, pasta **`/ (root)`**, e clique em **Save**.
7. Espere 1–2 minutos. O GitHub mostrará o link, algo como:
   `https://SEU-USUARIO.github.io/cedula-de-ideias/`
8. Esse é o link da cédula. O painel do professor fica em:
   `https://SEU-USUARIO.github.io/cedula-de-ideias/professor.html`
   (mas você também pode simplesmente abrir `professor.html` direto do seu computador, sem publicar — ele não precisa estar online, já que só você vai usá-lo.)

## Sobre o termômetro Estado × Mercado

A posição no termômetro é calculada a partir das 10 perguntas do eixo Economia: cada opção recebeu uma nota de -3 (mercado livre / Estado mínimo) a +3 (Estado forte / economia dirigida), atribuída manualmente a partir do conteúdo de cada posição na sua tabela original. É uma simplificação didática para gerar debate — não uma medição científica exata. A metodologia completa aparece no próprio app, no "Como isso foi calculado?" dentro do resultado.

## Atualizando o conteúdo depois

Se você editar a tabela de eixos/candidatos no futuro, me chame de novo com os dados atualizados — regenero o `index.html` e você só precisa repetir o passo 4 (upload) para atualizar o site no ar.
