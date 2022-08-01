# Step 1: Installation

- Install eslint dependencies

```
  npm install --save-dev eslint

  yarn add --dev eslint
```

# Step 2: Configuration

- Create a .eslintrc.json config file in the root of your project, and populate it with the code

```json
{
  "env": {
    "commonjs": true,
    "es2021": true,
    "node": true
  },
  "extends": "eslint:recommended",
  "parserOptions": {
    "ecmaVersion": "latest"
  },
  "rules": {
    "no-empty": "warn",
    "no-mixed-spaces-and-tabs": "error",
    "no-cond-assign": ["error", "always"],
    "array-callback-return": ["error", { "allowImplicit": true }],
    "linebreak-style": ["error", "unix"],
    "max-depth": ["error", 4],
    "key-spacing": ["error", { "afterColon": true }],
    "dot-location": ["error", "property"],
    "max-len": ["error", { "code": 80, "tabWidth": 2 }],
    "quotes": ["error", "single"],
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
