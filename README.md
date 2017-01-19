#### What is this?
This is the standard eslint config for ADP projects.

#### What should I do now?

1) Run these commands:

```bash
npm i -D eslint
npm i -D babel-eslint
npm i -D eslint-loader
```

2) Then install the airbnb eslint and peer dependencies

```bash
(
  export PKG=eslint-config-airbnb;
  npm info "$PKG@latest" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG@latest"
)
```

3) Include the following in your `package.json`

## For Browser-based React Apps

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
    "no-param-reassign": 1,
    "react/prefer-stateless-function": 0,
    "react/jsx-no-bind": 0
  }
}
```

## For NodeJS Projects

```json
 "eslintConfig": {
  "extends": "airbnb",
  "env": {
    "node": true
  },
  "rules": {
    "max-len": 0,
    "global-require": 0,
    "no-case-declarations": 0,
    "no-param-reassign": 1
  }
}
```
