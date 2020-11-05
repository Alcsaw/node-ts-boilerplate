# Node.js Boilerplate

A sample project with Node.js with TypeScript, EditorConfig, ESLint, Prettier e VSCode Node debugger already setup.

### [Typescript](https://www.typescriptlang.org/)
Only 2 custom configurations were made in [tsconfig.json](/tsconfig.json):
- `"outDir": "./dist",` para que o código transpilado seja todo salvo na pasta `dist` na raíz do projeto;
- `"rootDir": "./src",` para que a o compilador entenda que código desenvolvido da aplicação começa a partir da pasta `src`.

### [EditorConfig](https://editorconfig.org/)
EditorConfig sets some rules for the editor. Details are available in the [.editorconfig](/.editorconfig)

### [ESLint](https://eslint.org/docs/rules/)
ESLint is configured to follow AirBnB style guide and use import/export statements. More information in [.eslintrc.json](/.eslintrc.json).

Some directories are excluded from this validations. These are found at [.eslintignore](/.eslintignore).

It is recomended that the following configuration is added to VSCode's settings.json, after installing ESLint extension:

```json
"editor.codeActionsOnSave": {
  "source.fixAll.eslint": true
},
```

### [Prettier](https://prettier.io/docs/en/options.html)
[prettier.config.js](/prettier.config.js) is setup to prevent rules conflits between ESLint and Prettier.

### [VSCode Debugger]((https://code.visualstudio.com/docs/nodejs/nodejs-debugging))
Debugger configuration is found at [.vscode/launch.json](/.vscode/launch.json). It basically states that the debugger starts by attaching itself to the current node execution and restarts itself when server is restarted by modifying a file (via  `ts-node-dev`).
