# MF Design e Modelagem 3D

Site institucional desenvolvido com Next.js e pronto para publicação na
Vercel.

## Desenvolvimento local

Requer Node.js 22 ou mais recente.

### Windows PowerShell

Neste projeto, use o executável `npm.cmd` para evitar o bloqueio do `npm.ps1`
pela política de execução do Windows:

```powershell
npm.cmd ci
npm.cmd run dev
```

Depois que o terminal exibir `Ready`, acesse `http://localhost:3000`.

Se aparecer a mensagem de que `next` não é reconhecido, as dependências ainda
não foram instaladas. Execute `npm.cmd ci` antes de iniciar o servidor.

### Prompt de Comando, Git Bash, Linux ou macOS

```bash
npm ci
npm run dev
```

Para validar a versão de produção:

```powershell
npm.cmd run lint
npm.cmd run build
```

## Publicação na Vercel

Importe o repositório na Vercel. O framework Next.js e os comandos de build
são detectados automaticamente, portanto não é necessário preencher
configurações adicionais.
