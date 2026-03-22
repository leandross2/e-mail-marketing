# E-mail Marketing

Este repositório contém um template de e-mail em MJML e scripts para gerar o HTML final.

**Pré-requisitos**

- Ter o `Node.js` (versão LTS recomendada) e `npm` instalados.

**Instalação**

1. Abra um terminal e navegue até a pasta do projeto:

```
cd /Users/db/projects/e-mail-marketing
```

2. Instale as dependências do projeto:

```
npm install
```

> Observação: o projeto já declara `mjml` em `dependencies`, portanto o CLI estará disponível via `npx` ou através do script `npm run build`.

**Gerar o HTML (build)**

- Usando o script do `package.json`:

```
npm run build
```

O script atual gera o arquivo em `index.html` (equivalente a executar `mjml -o output.html`).

- Gerar manualmente com `npx` (alternativa):

```
npx mjml mail.mjml -o output.html
```

ou para sobrescrever o `output.html` existente:

```
npx mjml mail.mjml -o output.html
```

```
open output.html
```

**Estrutura do projeto**

- `mail.mjml`: arquivo principal do e-mail (usa os componentes em `components/`).
- `components/`: pedaços reutilizáveis do e-mail (`navBar.mjml`, `produtos.mjml`, `social.mjml`, etc.).
- `images/`: imagens usadas no e-mail.
- `output.html`: arquivo HTML gerado manualmente (opcional).
- `package.json`: contém o script `build` que executa `mjml -o output.html`.

**Como editar o template**

- Faça alterações nos arquivos dentro de `components/` e/ou em `mail.mjml`.
- Re-execute `npm run build` (ou o comando `npx mjml` mostrado acima) para gerar o HTML atualizado.

**Solução de problemas**

- Se o comando `mjml` não for reconhecido, use `npx mjml ...` ou instale globalmente:

```
npm install -g mjml
```

- Verifique a versão do Node com `node -v` e atualize se necessário.

**Contribuição**

- Abra uma issue ou envie um pull request no repositório: `https://github.com/TefyTete/e-mail-marketing`

**Licença**

- Consulte o campo `license` em `package.json` (atualmente: `ISC`).

---

Se quiser, eu posso:

- Rodar `npm install` e `npm run build` aqui para gerar o HTML.
- Adicionar um script de `watch` para recompilar automaticamente.

Diga o que prefere que eu faça a seguir.
