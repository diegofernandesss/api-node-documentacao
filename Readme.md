# Projeto em Nodejs

### Iniciando o Projeto

#### Criando o package.json:

- Para iniciar o projeto, execute o comando abaixo para gerar automaticamente o arquivo package.json:

```bash
npm init -y
```

### Configurando typescript:

#### Instalando as dependências no modo de desenvolvimento:

- tsup: Ferramenta para gerar o build do projeto.
- tsx: Permite executar o projeto no Node.js com suporte a TypeScript.
- typescript: Transpilador para TypeScript.
- -D: Flag para instalar as dependências no modo de desenvolvimento.
- @types/node: Definições de tipos para as APIs do Node.js, garantindo suporte completo no TypeScript.

#### Execute o comando abaixo para instalar as dependências:

```bash
npm install -D typescript @types/node tsx tsup
```

### Configurando tsconfig.json:

#### Iniciando tsconfig.json:

- Para criar o arquivo tsconfig.json, use o comando:
```bash 
npx tsc --init
``` 
#### Verificar Versão do Nodejs:

- Para garantir que está utilizando a versão correta do Node.js, execute o comando:

```bash
node --version
```

#### Documentação

- Acessar documentação para saber do tsconfig de acordo com a versão do node utilizado no host:
- Acessar Link da Documentação: [Nodejs - Click Aqui](https://github.com/tsconfig/bases)

#### Configurando package.json:

No arquivo package.json, adicione os seguintes scripts na propriedade "scripts" para facilitar o gerenciamento do projeto:

- "dev": Inicia o servidor em modo de desenvolvimento, assistindo mudanças nos arquivos utilizando o "watch".
- "build": Gera o diretório build com a versão compilada do projeto.
- "start": Executa o projeto a partir da pasta build.

Aqui está um exemplo de como deve ficar o seu package.json:
```json
{
  "name": "node",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "dev": "tsx watch ./src/server.ts",
    "build": "tsup src --out-dir build",
    "start": "node build/server.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "description": "",
  "devDependencies": {
    "@types/node": "^22.10.10",
    "tsup": "^8.3.5",
    "tsx": "^4.19.2",
    "typescript": "^5.7.3"
  }
}
```

#### Rodando Projeto em modo de Desenvolvimento:

```bash
npm run dev
```