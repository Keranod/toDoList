# toDoList-frontend

-   Frontend part of the `toDoList` project

### Initalized using Vite + TypeScript:

```
npm create vite@latest
√ Project name: toDoList
√ Package name: todolist
√ Select a framework: » React
√ Select a variant: » TypeScript
```

### Formatting:

-   create `.prettierrc.json` in root directory of the codebase
-   paste and save this code:

```json
{
    "trailingComma": "none",
    "tabWidth": 4,
    "semi": true,
    "singleQuote": true,
    "printWidth": 120
}
```

### TS Config:

-   add in `tsconfig.json` in `"compilerOptions"`:

```json
"noImplicitAny": true,
"strictNullChecks": true,
"strictFunctionTypes": true,
"strictPropertyInitialization": true,
```

### Json-server (full fake REST API):

-   npm install json-server --save-dev
-   Add in `package.json` in `"scripts"` section:

```json
"server": "json-server -p3001 --watch db.json"
```

-   It is run by using `npm run server`
-   Looks at `db.json` file in project root directory

### Using relative URLs:

-   Edit `vite.config.ts` adding in `defineConfig`:

```
server: {
    proxy: {
      '/api': {
        target: 'http://localhost:3001',
        changeOrigin: true,
      },
    }
  },
```

### Axios for HTTP request from React components:

-   npm install axios @types/axios

### Cleanup:

-   Delete assets/react.svg file
