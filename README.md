#### What is this?
This is the standard eslint config for ADP projects.

#### What should I do now?

1) Run this command:

```bash

npm i -D eslint && \
         babel-eslint && \
         eslint-config-airbnb && \
         eslint-loader && \
         eslint-plugin-import && \
         eslint-plugin-jsx-a11y && \
         eslint-plugin-react
         
```

2) Include the following in your `package.json`

```json
"eslintConfig": {
    "parser": "babel-eslint",
    "extends": "airbnb",
    "env": {
      "browser": true,
      "node": true
    },
     "plugins" : [
      "import",
      "react",
      "jsx-a11y"
    ],
    "rules": {
      "max-len": 0,
      "global-require": 0,
      "no-case-declarations": 0,
      "no-param-reassign": 0,
      "react/prefer-stateless-function": 0,
      "react/jsx-no-bind": 0
    }
  }
```
