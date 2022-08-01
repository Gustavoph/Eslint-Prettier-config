# Step 1: Installation

- Install eslint dependencies

```
  npm install --save-dev @typescript-eslint/parser @typescript-eslint/eslint-plugin eslint typescript

  yarn add --dev @typescript-eslint/parser @typescript-eslint/eslint-plugin eslint typescript
```

# Step 2: Configuration

- Create a .eslintrc.json config file in the root of your project, and populate it with the code

```json
{
  "root": true,
  "parser": "@typescript-eslint/parser",
  "plugins": ["@typescript-eslint"],
  "extends": [
    "eslint:recommended",
    "plugin:@typescript-eslint/eslint-recommended",
    "plugin:@typescript-eslint/recommended"
  ],
  "rules": {
    "indent": ["error", 2],
    "no-empty": "warn",
    "no-cond-assign": ["error", "always"],
    "no-mixed-spaces-and-tabs": "error",
    "array-callback-return": ["error", { "allowImplicit": true }],
    "linebreak-style": ["error", "unix"],
    "max-depth": ["error", 4],
    "key-spacing": ["error", { "afterColon": true }],
    "dot-location": ["error", "property"],
    "max-len": ["error", { "code": 80, "tabWidth": 2 }],
    "quotes": ["error", "single"],
    "new-cap": ["error", { "newIsCap": true }],
    "line-comment-position": ["error", { "position": "above" }],
    "semi": ["error", "never"],
    "no-multiple-empty-lines": ["error", { "max": 1 }],
    "no-trailing-spaces": [
      "error",
      { "skipBlankLines": true, "ignoreComments": true }
    ],
    "arrow-body-style": [
      "error",
      "as-needed",
      { "requireReturnForObjectLiteral": false }
    ],
    "no-duplicate-imports": ["error", { "includeExports": true }]
  }
}
```

# Step 3: Configuration Prettier

- Create a .prettierrc.json config file in the root of your project, and populate it with the code

```json
{
  "printWidth": 80,
  "tabWidth": 2,
  "singleQuote": true,
  "trailingComma": "all",
  "arrowParens": "always",
  "semi": false,
  "arraySeparator": true
}
```

# Step 4: Configuration script

- Configure lint in your package.json and lint your code

```json
"scripts": {
  "lint": "eslint . --ext .ts"
}

```

- You can use npm run lint for find errors in your code
- And you can use npm run lint --fix for find and fix erros in your code

### OBS: you must install eslint and prettier extension in your vscode
