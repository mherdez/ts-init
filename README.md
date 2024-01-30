# Typescript + Vite + Eslint + Prettier

### Instalación

```bash
npm create vite
npm i --save-dev --save-exact eslint @typescript-eslint/eslint-plugin eslint-plugin-prettier prettier eslint-config-prettier
```

## Extensiones utilizadas

Eslint: Para mantener un código limpio y ordenado.
Prettier: Para mantener un código limpio y ordenado.

## Vscode - settings.json

```json
// Prettier
  "prettier.requireConfig": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "[svelte]": {
    "editor.defaultFormatter": "svelte.svelte-vscode"
  },
  "[astro]": {
    "editor.defaultFormatter": "astro-build.astro-vscode"
  },
  "[html]": {
    "editor.defaultFormatter": "vscode.html-language-features"
  },
```

## .eslintrc.json

```json
{
  "parser": "@typescript-eslint/parser",
  "extends": [
    "plugin:@typescript-eslint/recommended",
    "plugin:prettier/recommended"
  ],
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module"
  },
  "rules": {
    "eqeqeq": ["error", "always"],
    "no-empty-function": "error",
    "no-implicit-coercion": "error",
    "@typescript-eslint/no-explicit-any": "error",
    "@typescript-eslint/no-duplicate-enum-values": "error",
    "@typescript-eslint/no-inferrable-types": "warn",
    "@typescript-eslint/no-non-null-assertion": "off",
    "@typescript-eslint/explicit-function-return-type": "warn",
    "@typescript-eslint/comma-dangle": "off",
    "comma-dangle": "off"
  }
}

```

## .prettierrc.json

```json
{
  "tabWidth": 2,
  "useTabs": false,
  "trailingComma": "none",
  "pluginSearchDirs": ["."],
  "overrides": [
    {
      "files": "*.{js*,ts*}",
      "options": {
        "jsxSingleQuote": true,
        "semi": false,
        "singleQuote": true
      }
    }
  ]
}

```

## package.json

```json
{
  "name": "ts-test",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "tsc && vite build",
    "preview": "vite preview",
    "lint": "eslint \"*/**/*.{js,ts,tsx}\" --fix"
  },
  "devDependencies": {
    "@typescript-eslint/eslint-plugin": "6.20.0",
    "eslint": "8.56.0",
    "eslint-config-prettier": "9.1.0",
    "eslint-plugin-prettier": "5.1.3",
    "prettier": "3.2.4",
    "typescript": "5.0.2",
    "vite": "4.4.5"
  }
}
```
