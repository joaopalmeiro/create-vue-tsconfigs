# create-vue-tsconfigs

TSConfig files for projects created with [create-vue](https://github.com/vuejs/create-vue).

- [Source code](https://github.com/joaopalmeiro/create-vue-tsconfigs)
- [npm package](https://www.npmjs.com/package/create-vue-tsconfigs)
- [Licenses](https://licenses.dev/npm/create-vue-tsconfigs/0.1.0)

## Available TSConfig files

### [create-vue@3.9.2](https://github.com/vuejs/create-vue/tree/v3.9.2) and [create-vue-templates@3.9.2](https://github.com/vuejs/create-vue-templates/tree/v3.9.2)

| Template                                                                           | Package TSConfig file                               | Source TSConfig file                                                                                          |
| ---------------------------------------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| [typescript](https://github.com/vuejs/create-vue-templates/tree/v3.9.2/typescript) | [tsconfig.app.json](typescript/tsconfig.app.json)   | [tsconfig.app.json](https://github.com/vuejs/create-vue-templates/blob/v3.9.2/typescript/tsconfig.app.json)   |
| [typescript](https://github.com/vuejs/create-vue-templates/tree/v3.9.2/typescript) | [tsconfig.node.json](typescript/tsconfig.node.json) | [tsconfig.node.json](https://github.com/vuejs/create-vue-templates/blob/v3.9.2/typescript/tsconfig.node.json) |

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
cd test-create-vue && npm install
```

```bash
npx vue-tsc --project tsconfig.app.json --showConfig
```

```bash
npx vue-tsc --project tsconfig.node.json --showConfig
```

```bash
cd ..
```

Delete the following [top-level options](https://www.typescriptlang.org/tsconfig#extends) (if necessary):

- `"references"`
- `"files"`
- `"include"`
- `"exclude"`

Remove the following [`compilerOptions` options](https://www.typescriptlang.org/tsconfig) (if necessary):

- `"types"`
- `"tsBuildInfoFile"`
- `"baseUrl"`
- `"paths"`

Add the following [`compilerOptions` option](https://www.typescriptlang.org/docs/handbook/project-references.html#composite) (if necessary):

- `"composite": true`

```bash
npm run format
```

## Deployment

```bash
npm pack --dry-run
```

```bash
npm version patch
```

```bash
npm version minor
```

```bash
npm version major
```

- Update the version in the `Licenses` link at the top.
- Commit and push changes.
- Create a tag on [GitHub Desktop](https://github.blog/2020-05-12-create-and-push-tags-in-the-latest-github-desktop-2-5-release/).
- Check [GitHub](https://github.com/joaopalmeiro/create-vue-tsconfigs/tags).

```bash
npm login
```

```bash
npm publish
```

- Check [npm](https://www.npmjs.com/package/create-vue-tsconfigs).
