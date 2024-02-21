# create-vue-tsconfigs

TSConfig files for projects created with [create-vue](https://github.com/vuejs/create-vue).

## Available TSConfig files

### [create-vue@3.9.2](https://github.com/vuejs/create-vue/tree/v3.9.2) and [create-vue-templates](https://github.com/vuejs/create-vue-templates/tree/v3.9.2)

| Template                                                                           | TSConfig file                                       |
| ---------------------------------------------------------------------------------- | --------------------------------------------------- |
| [typescript](https://github.com/vuejs/create-vue-templates/tree/v3.9.2/typescript) | [tsconfig.app.json](typescript/tsconfig.app.json)   |
| [typescript](https://github.com/vuejs/create-vue-templates/tree/v3.9.2/typescript) | [tsconfig.node.json](typescript/tsconfig.node.json) |

## Development

Install [fnm](https://github.com/Schniz/fnm) (if necessary).

```bash
fnm install && fnm use && node --version && npm --version
```

```bash
npm install
```

```bash
npm create vue@3.9.2 test-create-vue
```

```bash
cd test-create-vue && npx vue-tsc --project tsconfig.app.json --showConfig
```

```bash
npx vue-tsc --project tsconfig.node.json --showConfig && cd ..
```

Delete the following [top-level options](https://www.typescriptlang.org/tsconfig#extends):

- `"references"`
- `"files"`
- `"include"`
- `"exclude"`

Add the following [`compilerOptions` option](https://www.typescriptlang.org/docs/handbook/project-references.html#composite):

- `"composite": true`

```bash
npm run format
```
