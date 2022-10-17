# monorepo-next-storybook

Basaremos nuetro monorepo en Yarn Workspaces ([https://classic.yarnpkg.com/en/docs/workspaces/](:https://classic.yarnpkg.com/en/docs/workspaces/)) que es bastante simple y no necesitamos publicar módulos individuales dentro del monorepo.

El primer paso que voy a crear en el monorepo es crear la carpeta de repositorio y crearemos _package.json_ con el comando:

```properties
yarn init
```

agreagamos workspaces:

```json
{
    "name":"@elboqueronpaco/monorepo",
    "private": true,
    ...
    "workspaces":[
        "packages/app/*",
        "packages/shared/*"
    ]
    ...
}
```

instalamos todas las dependecias de desarrollo:

```properties
yarn add -W -D @babel/core @babel/preset-env @babel/preset-react @babel/preset-typescript @next/bundle-analyzer @storybook/addon-actions @storybook/addon-docs @storybook/addon-essentials @storybook/addon-links @storybook/addon-storyshots @storybook/react @testing-library/jest-dom @testing-library/react @types/jest @types/node @types/react @typescript-eslint/eslint-plugin @typescript-eslint/parser arg babel-jest babel-loader babel-plugin-module-resolver dev-kong eslint eslint-config-standard-with-typescript eslint-plugin-import eslint-plugin-jest eslint-plugin-jest-dom eslint-plugin-node eslint-plugin-prettier eslint-plugin-promise eslint-plugin-react eslint-plugin-react-hooks eslint-plugin-standard fs-extra globby identity-obj-proxy internal-ip jest jest-runtime next-transpile-modules plop pm2 prettier react-is react-test-renderer replace-in-files rimraf sass sass-loader ts-jest ts-node typescript
```