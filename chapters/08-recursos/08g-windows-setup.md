# Windows

Existem duas maneiras de configurar o Ionic em uma máquina windows. Uma delas é instalar todas ass dependências uma por uma, e 
a outra é instalar o plugin Tools for Cordova para o Visual Studio 2015. Nós explicamos o segundo modo, para usar o Visual Studio em
[nosso blog](http://blog.ionic.io/visual-studio-tools-for-apache-cordova/).

## Ferramentas comuns

Na maior parte, o Node.js e NPM serão extensivamente usados tanto para o Ionic quanto para o Cordova. Você pode usar o instalador 
do [próprio site do Node.js](https://nodejs.org/) para instala-lo ou o gerenciador de pacotes chamado [Chocolatey](https://chocolatey.org/).

Uma vez instalado, você deve ter acesso tanto aos comandos `node` e `npm` da sua linha de comando.

## iOS

O SDK para iOS não roda em ambientes Windows, então não temos o que fazer aqui... Mas se você ainda quiser criar aplicações para iOS mesmo assim, veja o [Package](http://ionic.io/platform#packaging), uma parte da plataforma Ionic.

## Java

Vamos precisar instalar o Java direto do [website deles](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html). O instalador coloca o Java na sua pasta `C:\Program Files\Java`, então navegue até lá e escolha a versão java que você instalou. Copie essa localização (incluindo o número da versão) porque você irá precisar disso depois.

## Android

Faça o download do Android Studio e instale-o na máquina seguindo os passos para configurar o IDE completamente. Ele deve exibir uma localização para perguntar aonde você deseja instalar o Android `SDK`; copie essa localização também para uso futuro.

Depois disso, dentro da pasta do novo `SDK`, vamos rodar o arquivo `android`, presente na pasta `tools` (`tools/android`) para abrir o gerenciador de downloads do Android SDK Manager. Uma vez aberto vamos instalar os seguintes componentes:

- Android Platform SDK para a sua versão alvo do android
- Android Platform-Tools
- Android SDK build-tools version 19.1.0 ou superior
- Android Support Repository (pode ser encontrado dentro da pasta "Extras")

Aceite as declarações de licença de deixe os pacotes serem instalados.

## Variáveis de ambiente

Agora que tudo está instalado, vamos precisar setar algumas variáveis de ambiente para a nossa linha de comando. No menu iniciar, procure por "Variáveis de ambiente do sistema" (ou "System Environment Variables"). Daqui vamos poder atualizar a variável de usuário chamada `PATH` e criar uma nova variável chamada `JAVA_HOME`

- `JAVA_HOME`: O caminho que o Java foi instalado (copiado dois passos acima)
- `PATH`: Vamos adicionar duas novas entradas, uma será o caminho onde o `Tools` está instalado para o Android SDK, o outro para o `Platform Tools`

A partir daqui, então, poderemos rodar:

```bat
# Checa a versão do java
java -version

# inicia o Android SDK Manager
android
```

Agora poderemos criar e construir um projeto Android a partir da linha de comando.

## Aplicativos Windows Universal

Para criar aplicativos compatíveis com o Windows Universal, baixe e instale o Visual Studio 2015 Community Edition. Durante a instalação, selecione opção "Tools for Cross Platform Development" juntamente com os SDK's para Windows Universal Apps.

Com tudo isso instalado, você será capaz de adicionar uma plataforma windows a partir da linha de comando, com este comando:

`ionic platform add windows`

Por padrão, o comando `build` produz dois pacotes: Windows 8.1 e Windows Phone 8.1, o qual o Ionic não suporta. Para atualizar um pacote Windows para a versão 10, a seguinte linha de configuração deve ser adicionada no arquivo `config.xml`:

`<preference name="windows-target-version" value="10.0">`
