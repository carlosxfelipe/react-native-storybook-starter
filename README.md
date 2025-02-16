# React Native Storybook starter

O projeto foi inicialmente criado a partir das instruções do tutorial oficial do Storybook para React Native. O tutorial pode ser encontrado no seguinte link:  
[https://storybook.js.org/tutorials/intro-to-storybook/react-native/pt/get-started/](https://storybook.js.org/tutorials/intro-to-storybook/react-native/pt/get-started/)

Após isso, fiz algumas configurações para conseguir gerar uma pasta _dist_ e em seguida criar um pacote .tgz (tarball).

## Instruções para Rodar o Projeto

### Configuração Inicial

Após clonar o repositório, execute o seguinte comando para instalar as dependências:

```bash
yarn
```

### Comandos

- **Navegador:**  
  Para rodar o Storybook no navegador, use o comando:

  ```bash
  yarn storybook
  ```

- **iOS:**  
  Para rodar o Storybook no emulador do iOS, use o comando:

  ```bash
  yarn storybook:ios
  ```

- **Android:**  
  Para rodar o Storybook no emulador Android, use o comando:

  ```bash
  yarn storybook:android
  ```

### Build e instalação

- **npm pack:**  
   Para realizar o build, use o comando:

  ```bash
  yarn build && npm pack
  ```

  Após isso, um arquivo **react-native-storybook-starter-1.0.0.tgz** será criado. Esse nome é originado a partir do _name_ e do _version_ do **package.json**. Se for alterar o _name_, é importante apagar node_modules e rodar yarn novamente para reinstalar as dependências.

  Copie esse arquivo gerado para a raiz do projeto alvo e para instalá-lo use o comando:

  ```bash
  yarn add file:./react-native-storybook-starter-1.0.0.tgz
  ```

  A partir do Yarn v2+, a instalação de pacotes locais a partir de um arquivo .tgz pode ser feita utilizando um alias.

  ```bash
  yarn add qualquercoisa@file:./react-native-storybook-starter-1.0.0.tgz
  ```

### Uso

Se instalado normalmente:

```
import { Carousel } from "react-native-storybook-starter";
```

Se instalado com um alias no Yarn v2+:

```
import { Carousel } from "qualquercoisa";
```
