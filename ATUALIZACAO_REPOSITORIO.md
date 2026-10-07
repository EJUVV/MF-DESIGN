# Atualização do repositório

Data de preparação: 7 de outubro de 2026

Branch: `main`

Repositório: `https://github.com/EJUVV/MF-DESIGN.git`

## Alterações preparadas

- Reorganização das seções para: Soluções → Projetos em destaque → Como funciona.
- Substituição do ícone de impressora convencional por uma impressora 3D.
- Atualização do botão final para o Instagram da MF Design, com ícone e link corretos.
- Inversão das etiquetas “Personalizado” e “Sob encomenda” nos projetos correspondentes.
- Inclusão de uma transição visual entre Soluções e Projetos em destaque.
- Carrossel de soluções dividido em duas páginas: 01/02 e 03/04.
- Navegação do carrossel somente pelas setas, sem os seletores de grupo.
- Encerramento automático do carrossel na página com os itens 03 e 04.
- Remoção da pasta local `node_modules`; ela não era versionada e permanece protegida por `.gitignore`.

## Arquivos da atualização

- `app/page.tsx`
- `app/globals.css`
- `ATUALIZACAO_REPOSITORIO.md`

## Validação antes do envio

Resultados obtidos durante a preparação:

- `npx.cmd tsc --noEmit`: aprovado.
- `git diff --check`: aprovado.
- Página local: HTTP 200.
- Renderização: dois grupos, quatro cartões e seletores de grupo removidos.
- `npm.cmd run build`: precisa ser repetido com o servidor de desenvolvimento encerrado; a tentativa atingiu o limite de 180 segundos enquanto `next dev` permanecia ativo.

Encerre o servidor de desenvolvimento e execute no PowerShell:

```powershell
npm.cmd ci
npx.cmd tsc --noEmit
npm.cmd run build
```

## Atualização do GitHub

Revise as alterações antes de criar o commit:

```powershell
git status
git diff --check
git diff
```

Depois da revisão:

```powershell
git add app/page.tsx app/globals.css ATUALIZACAO_REPOSITORIO.md
git commit -m "Atualiza conteúdo e carrossel da página inicial"
git push origin main
```

O `commit` e o `push` devem ser executados somente depois da aprovação final da página.
