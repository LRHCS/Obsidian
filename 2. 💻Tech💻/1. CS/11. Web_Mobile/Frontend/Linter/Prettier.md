#Tools #Linter #javascript 
install `npm install --save-dev --save-exact prettier, echo {}> .prettierrc.json`

```json
// goes to .prettierrc.json
{
  "arrowParens": "always",
  "bracketSameLine": false,
  "bracketSpacing": true,
  "embeddedLanguageFormatting": "auto",
  "htmlWhitespaceSensitivity": "css",
  "insertPragma": false,
  "jsxSingleQuote": false,
  "printWidth": 80,
  "proseWrap": "preserve",
  "quoteProps": "as-needed",
  "requirePragma": false,
  "semi": true,
  "singleAttributePerLine": false,
  "singleQuote": false,
  "tabWidth": 4,
  "trailingComma": "es5",
  "useTabs": false,
  "vueIndentScriptAndStyle": false,
  "rangeStart": 0
}
```

```txt
# Ignore artifacts: (goes to .prettierignore) 
build 
coverage
```

format all - >
```
npx prettier --write .
```

check ->
```
npx prettier --check .
```