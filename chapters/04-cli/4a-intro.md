# Ionic CLI

Ionic CLI é a principal ferramenta que você usará durante o desenvolvimento do seu aplicativo Ionic. É como um canivete suiço: Ele agrupa várias ferramentas em uma única interface. O CLI contém um número de comandos crucial para o desenvolvimento com Ionic, tais como **start**, **build**, **serve** e **run**. Também contém os comandos **emulate** e **info**, que podem ser uteis em determinadas situações.


# Instalando o CLI

Antes de instalar o CLI, você vai precisar instalar primeiro [node](http://ionicframework.com/docs/v2/resources/what-is#node) e [npm](http://ionicframework.com/docs/v2/resources/what-is#npm). OBS: O CLI requer Node 4.X (Node 5.X é conhecida por ocasionar problemas) Após a instalação, você pode executar o seguinte comando para obter a ultima versão do Ionic CLI.

```shell
$ npm install -g ionic@beta
```
No Mac ou Linux, você irá precisar usar o comando **sudo** para instalar Ionic Globalmente.

```shell
$ sudo npm install -g ionic@beta
```

# Uso básico

**start** é um dos comandos mais importante, usado para criar um novo projeto Ionic. Vamos testar:

```shell
$ ionic start myAwesomeApp --v2
```
Isso irá criar um novo aplicativo chamado **myAwesomeApp**. Agora vamos abrir o directorio  - **cd** - e executar outro comando no Ionic CLI.

```shell
$ ionic info
```
Isso irá mostrar detalhes do seu ambiente Ionic de desenvolvimento, ideal para depuração (debug). Finalmente, para ver o seu aplicativo no browser, você pode usar o comando **serve**.

```shell
$ ionic serve
```

# Proximos Passos

Agora você já sabe o básico, cheque o sumario para poder ver a lista completa de comandos. Se você preferir, você pode ver a lista completa de comandos e suas opções, simplesmente digitando **ionic**.
