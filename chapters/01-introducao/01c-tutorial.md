# 1.3 Ionic 2 Tutorial

Agora que você tem [instalado Ionic e suas dependências](chapters/01-introducao/01b-instalation.md), você pode construir seu primeiro aplicativo! Esta seção irá guiá-lo através do processo de iniciar uma nova aplicação, adicionando páginas, navegação entre as páginas, e muito mais. Vamos começar!

## Iniciano um Novo aplicativo Ionic 2

Vanos criar um aplicativo! Use o comando **start** para inicializar um novo aplicativo Ionic. Especifique que você quer que ele seja um aplicativo Ionic 2 passando a opção **--v2**.  Nós também especificamos que o modelo do **tutorial** poderia ser usado.
```
$ ionic start MyIonic2Project tutorial --v2
```
    
Isso vai baixar o Ionic 2, instalar o [módulos npm](ionic2-docs/glossario.md) para a aplicação, e obter o [Cordova](ionic2-docs/glossario.md) configurado e pronto para utilizar.

Quer usar o TypeScript em vez disso? Passe o sinalizador **--ts** e obtenha uma configuração de projeto de TypeScript em seu lugar.

Você pode ter notado que nós passamos **tutorial** para o comando **start iônica**. Isto diz para o Ionic inicializar seu aplicativo usando o [modelo tutorial](https://github.com/driftyco/ionic2-starter-tutorial). Se você não especificar um modelo executando **ionic start MyIonic2Project --v2**, o [tab starter](https://github.com/driftyco/ionic2-starter-tabs) será utilizado.

## Visualizando o aplicativo em um navegador

Agora, você pode **cd** para entrar na pasta que foi criada. Para obter uma visualização rápida do seu aplicativo no navegador, use o comando **serve**.
```
$ cd MyIonic2Project/
$ ionic serve
```

[tutorial-screen](tutorial-screen.png)

Você deverá ver a mensagem de boas vindas mostrada acima, se tudo foi instalado com sucesso.

Na próxima seção, vamos falar sobre a estrutura do projeto criado pelo comando **ionic**.
