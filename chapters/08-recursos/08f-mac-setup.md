# OSX

## Ferramentas comuns

Node e NPM vão ser usados extensivamente para o Ionic e Cordova na maioria dos casos. Voê pode usar o instalador diretamente
[do site do Node.js](https://nodejs.org/) ou então vários outros gerenciadores de pacotes:

- [n](https://github.com/tj/n)
- [nvm](https://github.com/creationix/nvm)
- [homebrew](http://brew.sh/)

Uma vez instalados, você deverá ter acesso tanto ao comando `node` e ao `npm` diretamente da linha de comando.

## iOS

Você irá precisar instalar o Xcode da Apple. Você pode fazer isso ou pela Mac App Store ou então pelo Portal de desenvolvimento da
Apple. A Mac App Store é o jeito mais fácil. Uma vez que o XCode esteja instalado, você terá o próprio XCode, o SDK do iOS, 
as ferramentas de linha de comando do IDE e todas as ferramentas de build para criar um app nativo.

## Java

Você precisará baixar o Java diretamente do [site oficial](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).
A instalação vai colocar o Java na sua pasta `/Library/Java/JavaVirtualMachines`, então navegue até lá e escolha a versão que
você acabou de instalar. Copie essa localização (incluindo o número da versão) porque ela será necessária mais tarde.

## Android

Baixe o Android Studio e siga os passos do instalador para configurar a IDE. Ela deverá pedir uma localização para aonde o
SDK será instalado; copie essa localização, porque ela também será usada mais tarde.

Depois, dentro da pasta `SDK` que foi criada, vamos rodar o comando `tools/android` para abrir o gerenciador de versões
do Android SDK. Vamos instalar:

- Android Platform SDK para a sua versão escolhida do Android
- Android Platform-Tools
- Android SDK build-tools versão 19.1.0 ou superior
- Android Support Repository (encontrado na pasta “Extras”)

Aceite os termos de licença e deixe os pacotes instalando.

## Variáveis de ambiente

Agora que tudo está instalado, vamos precisa setar algumas variáveis de ambiente para a nossa linha de comando. 
Abra o terminal e digite `touch .bash_profile`, então abra esse arquivo no seu editor de preferência.

Daqui, teremos que adicionar algumas linhas. Essas serão as referências para o Java, a localização do Android SDK que 
copiamos anteriormente.

Se você usou os caminhos que foram sugeridos, você deverá ter algo assim no final:

```
# Create a JAVA_HOME Variable, use, the name of the JDK folder
export JAVA_HOME=/Library/Java/JavaVirtualMachines/{replaceWithYourJavaVersion}/Contents/Home
# Add that to the global PATH variable
export PATH=${JAVA_HOME}/bin:$PATH
# Add the Android SDK to the PATH variable
export PATH=${PATH}:~/Library/Android/sdk/tools:~/Library/Android/sdk/platform-tools
```

Agora feche o terminal e abra-o novamente. Se não houve nenhum erro você poderá rodar os seguintes comandos:

```
# checa a versão do java
java -version

# inicia o gerenciador de SDK
android
```

A partir de agora você poderá criar e compilar aplicações para android pela linha de comando.
