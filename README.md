# RED ADP eslint config
.eslintrc.json file for RED ADP

#### What is this?
This is the standard eslint config for ADP projects.

#### How to use this file:

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
