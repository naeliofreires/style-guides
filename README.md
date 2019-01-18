@naeliofreires
# Setup: 

Este _Style Guide_ pode ser utilizado para varias projetos em JS,

*Os seguintes passo foram feito após a criação do projeto!*
### I Step

```sh
$ yarn add eslint -D || npm install -g eslint
$ yarn run eslint --init || eslint --init
```
### II Step
Após você executar os seguintes códido acima, ira aparecer  algumas opções, você deve selecionar as seguintes:
-  Use a popular style guide 
-  Airbnb (https://github.com/airbnb/javascript)

### III Step
> Você deve em seguida adicionar o plugin **ESLint** no seu edito de texto e
> depois no arquivo **.eslintrc.json** adicione o seguinte texto.
```json
 {
    "parser": "babel-eslint",
    "env": {
      "browser": true,
      "jest": true
    },
    "plugins": ["react", "jsx-a11y", "import"],
    "extends": "airbnb",
    "rules": {
      "react/jsx-filename-extension": [
        "error",
        {
          "extensions": [".js", ".jsx"]
        }
      ],
      "global-require": "off",
      "import/prefer-default-export": "off",
      "no-unused-expressions": ["error", { "allowTaggedTemplates": true }]
    }
  }
```
### IV Step
> Logo depois adicione o plugin **Prettier - Code formatter** e siga os seguintes passos (VSCODE):

-   Ctrl + Shit + P
-   Digite 'settings:' e selecione 'Open Settings JSON'
-   E adicione as seguintes config:
```json
{
    "editor.tabSize": 2,
    "editor.formatOnSave": true,
    "prettier.eslintIntegration": true,
}
```

### V Step
> Agora vamos para o passo final, adicione o plugin **EditorConfig for Visual Code** e em seguidad criar o arquivo **.editorconfig** e adicionar o seguinte codigo:

```env
root = true

[*]
indent_style = space
indent_size = 2
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = false
insert_final_newline = false
```

Fonte: [Blog da Rockseat](https://blog.rocketseat.com.br/)
