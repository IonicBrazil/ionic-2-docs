# Glossário do Desenvolvedor Ionic

## Android SDK  

O [Android SDK](http://developer.android.com/sdk/index.html) é um kit de desenvolvimento de softwares para desenvolvedores construam aplicações para a plataforma Google's Android. Ele inclui ferramentas para  construção (*building*), testes e depuração (*debugging*) de aplicativos Android.


## Anotações  

Anotações são usadas para adicionar metadados em uma classe. TypeScript extende ES6 através de anotações. Enquanto você pode definir sua própria anotação, a comunidade Ionic referem-se a duas anotações fornecidas pelo Angular 2: `@Component` e `@View`.


## Autoprefixo  

Autoprefixo é uma ferramenta que adiciona prefixos específicos nos códigos CSS/Sass manuscritos. Isso garante que as regras CSS escritas por você sejam padronizadas e aplicada em todos os navegadores que a suportam. Por exemplo, ao invés de você conhecer cada sintaxe do *flexbox* usado para vários navegadores, o autoprefixo permite que você escreva apenas `display: flex;`; e automaticamente ele vai ser linkado no CSS correto.


## Babel  

[Babel](http://babeljs.io/) é um compilador JavaScript na nova geração. Atualmente, os navegadores não suportam todos os recursos da próxima geração do JavaScript (ES6). Babel resolve esse problema compilando seu código ES6 em ES5, que é a versão JavaScript suportada em todos os navegadores.


## Browserify  

[Browserify](http://browserify.org/) é um agrupador (*bundler*) de códigos, semelhante ao *webpack*, que vai analisar todo o código do seu projeto, e vai gerar (bundle) um único arquivo.


## Agrupamento (Bundling)  

Agrupamento é o processo de pegar as dependências do aplicativo (seus códigos escritos mais quaisquer módulos NPM instalados) e compilar isso tudo em um único arquivo.


## CLI  

A CLI, ou interface de linha de comando, é uma interface baseada em texto para interagir com um programa. O terminal de linha de comando é comum para um usuário Mac/Linux, e os usuários Windows utilizam o Prompt de Comando. Muitas vezes a comunidade Ionic utiliza esse termo para se referir ao Ionic CLI. O Ionic CLI pode ser usado para inúmeras coisas, como criar *builds* de aplicativos em produção, executar o servidor de desenvolvimento, e acessar serviços do Ionic.


## CommonJS  

[CommonJS](https://webpack.github.io/docs/commonjs.html) é um grupo de formatos e padrões para API's JavaScript. Eles definem padrões para módulos e pacotes JavaScript.


## Cordova  

[Cordova](https://cordova.apache.org/) é uma saída para transformar códigos HTML/CSS/JS em um aplicativo nativo. Ele fornece a API do JavaScript para acessar recursos e funcionalidades nativas do dispositivo, como a camera ou acelerômetro. Cordova contém ferramentas necessárias de compilação para o empacotamento de aplicativos web para iOS, Android, e Windows Phone.


## Decorators  

*Decorators* são expressões que retornam uma função. Elas basicamente permitem que você pegue uma função ja existente e altere o seu comportamento. Com TypeScript, você também pode decorar classes e parâmetros. Quando você decorar uma classe, você estará enrolando e estendendo o comportamento de seu construtor. Em outras palavras, o *decorator* irá adicionar alguma funcionalidade quando o construtor for chamado, e irá retornar o construtor original. Quando você decorar um parâmetro, você estará enrolando o argumento que foi passado para esse parâmetro. Em outras palavras, o *decorator* irá adicionar funcionalidades quando um argumento é passado para o método, e em seguida, retornar o argumento original.


## ES5  

ES5 refere-se ao EcmaScript 5ª Edição. Uma maneira simples de colocá-lo é que o ES5 é a versão do JavaScript que os desenvolvedores estão familizariados atualmente.


## ES2015/ES6  

ES2015/ES6 são dois nomes geralmente usados para a versão mais recente do JavaScript. Uma vasta gama de novas funcionalidades foram introduzidas nessa versão, incluindo classes, módulos, iteradores e *promises*. O projeto final da ES6 já foi aproviado, o que significa que os códigos ES6 podem ser interpretados diretamente pelo navegador. Para usas as funcionalidades ES6 atualmente, ferramentas como Babel e TypeScript tem que converter codes ES6 em ES5.


## ES2016/ES7  

ES2016/ES7 são dois nomes geralmente usados para a versão experimental do JavaScript. A futura versão do JavaScript vai adicionar um número de novas funcionalidades à linguagem, incluindo funções assíncronas e *typed objects*. Ela está em constante revisão, e atualmente não é adequada para produção de aplicativos.


## Genymotion  

Genymotion é um emulador Android de terceiros. É extremamente rápido, e é útil para testar rapidamente seus aplicativos no Android. Confira a nossa sessão de [recursos](http://ionicframework.com/docs/v2/resources/developer-tips/#using-genymotion-android) na sessão Genymotion para maiores informaçõe.


## Git  

[Git](https://git-scm.com/) é um sistema de controle de versão para o gerenciamento de código. Ele permite que equipes de desenvolvimento possam contribuir com códigos para o mesmo projeto sem causar conflitos no código.


## Gulp  

[Gulp](http://gulpjs.com/) é uma ferramenta para execução de tarefas automatizadas que podem ser usadas para compilar seu aplicativo. Comumente execução de tarefas automatizadas inclui converter ES6 para ES5, transformar Sass em CSS, minificar códigos e concatenar arquivos.


## Importação  

ES6 traz o conceito de módulos para o javascript. Com módulos, as coisas não estão mais no escopo global e devem ser importados para serem utilizadas. Isso torna muito mais fácil para entender de onde seu código está vindo.  

[Importação](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import)


## Ionicons  

[Ionicons](http://ionicons.com/) é um conjunto de ícones de código aberto criados para serem usados com Ionic. Ele inclui iOS, Material Design, e ícones de redes sociais, bem como uma vasta coleção de ícones comumente usados. Ionicons é incluído por padrão em distribuições Ionic, mas eles podem ser usados em qualquer projeto.


## Karma  

[Karma](https://karma-runner.github.io/0.13/index.html) é um automatizador de testes que podem executar testes no seu aplicativo dentro de um navegador em tempo real. O tete é preciso, pode ser escrito sob qualquer framework, e apenas executá-los no navegador. Foi originalmente escrito para Angular 1.


## Module  

Módulos em JavaScript são pequenos, independentes, e reutilizáveis, pedaços de códigos podem ser isolados uns dos outros e do escopo global.


## Recarregamento Automático (Live Reload)  

Recarregamento Automático é uma ferramenta que recarrega seu navegador automaticamente quando detecta mudanças em seu código. Ele assite um diretório especifico e toda vez que um arquivo ou diretório é atualizado, ele envia um sinal para o navegador recarregar. Em casos de mudanças no CSS, ele vai injetar as mudanças CSS instantaneamente e recarregar a página inteira.


## Node  

[Node](https://nodejs.org/en/) é um ambiente de execução em tempo real que permite você escrever JavaScript do lado do servidor. Além de ser usado para serviços web, node também pode ser usado para desenvolver ferramentas, assim como o [Ionic CLI](http://ionicframework.com/docs/v2/resources/what-is/#cli).


## NPM  

[NPM](https://www.npmjs.com/) é o gerenciador de pacotes para Node. Com ele é possível instalar, compartilhar e adicionar pacotes aos módulos do Node. Ionic pode ser instalado com npm, juntamente com suas dependências.


## Observável (Observable)  

Um observável é um objeto que emite eventos (ou notificações). Um observador é um objeto que escuta esses eventos e faz alguma coisa quando um novo evento é recebido. Juntos, eles criam um padrão que pode ser utilizado para programar de forma assíncrona.


## Polyfill  

Um polyfill é um pedaço de código que vai adicionar uma funcionalidade ao navegador e normalizar suas diferenças. É similar ao shim, mas como o shim possui sua própria API, um polyfill vai usar uma API esperada pelo navegador.  

[O que é um polyfill?](https://remysharp.com/2010/10/08/what-is-a-polyfill)


## Protractor  

[Protractor](https://angular.github.io/protractor/#/) é um framework de testes escrito pela equipe do Angular para usar com o Angular. Ele pode ser usado juntamente com automatizadores de testes, como o Karma, para testes de front-end. Basicamente irá descobrir se seu aplicativo vai se comportar da maneira esperada.


## Sass  

Sass é uma linguagem de estilos que compila CSS e é usado pelo Ionic. Sass é como o CSS, porém com funcionalidades e características adicionais, tais como [variáveis](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#variables_), [mixins](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#mixins) e [laços de repetição](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#_10).


## Shim  

Um *shim* é um pedaço de código que normaliza diferentes APIs entre os navegadores. Um *shim* muitas vezes possui sua própria API que irá lidar com os diferentes navegadores.


## SystemJS  

SystemJS é um carregador de módulos (assim com o RequireJS) que carrega módulos de diferentes formatos - AMD, CommonJS e ES6, e é construído em cima do [polyfill do módulo de carregamento do ES6](https://github.com/ModuleLoader/es6-module-loader) (um polyfill implementa um caminho para o JavaScript carregar módulos nativos futuramente).


## Transpiler  

*Transpile* significa converter o código de uma linguagem para outra linguagem. Tipicamento um *transpiler* convertem códigos de linguagens de alto nível para outra linguagem de alto nível. Muitas vezes a comunidade Ionic vai falar sobre *transpiling* ES2015/ES6 ou TypeScript para ES5.


## TypeScript  

TypeScript é um super conjunto do JavaScript, o que siginifica que fornece um grande número de funcionalidades adicionais ao seu JavaScript, como declarações de tipo e interfaces. Embora o Ionic seja construído com TypeScript, usá-lo para criar um aplicativo Ionic é completamente opcional.


## Testes Unitários  

Testes unitários são uma maneira de testar pequenos pedaços de código para ver se eles se comportam conforme o esperado. Alguns frameworks de testes unitários são Jasmine, Mocha, QUnit, e muitos outros.


## Webpack  

[Webpack](https://webpack.github.io/) agrupa módulos e outros ativos JavaScript. Ele pode ser usado para criar pedaços simples ou múltiplos que são carregados apenas quando necessário. Basicamente você pode usar Webpack para levar seus inúmeros arquivos e dependências e empacotá-los em um único arquivo, ou conforme seu ajuste.


## XCode  

[XCode]() é uma IDE que permite desenvolver aplicativos para iOS. XCode inclui ferramentas que te ajudam com o *building*, testes e *debugging* do seu aplicativo. Embora muitos desenvolvedores Ionic não o usem como editor de código favorito, é muitas vezes usado para construir e assinar uma versão de produção de um aplicativo.
