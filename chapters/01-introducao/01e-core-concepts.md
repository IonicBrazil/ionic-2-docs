# 1.5 Conceitos Básicos

Se você é completamente novo para Ionic e/ou desenvolvimento de aplicativos híbrids para celular, ele pode ser útil para obter uma compreensão de alto nível do núcleo da filosofia, conceitos e ferramentas por trás do Ionic. As informações a seguir podem ajudá-lo a se familiarizar com o Ionic e como ele funciona.

## O que é Ionic?

Ionic é um SDK de código aberto que permite aos desenvolvedores criar, aplicativos móveis de desenpeho de alta qualidade utilizando tecnologias web familiares (HTML, CSS e JavaScript).

Ionic está voltada principalmente para a aparência, ou a interação UI, de um aplicativo. Isto significa que não é um substituto para o PhoneGap ou o seu framework JavaScript favorito. Em vez disso, Ionic se encaixa bem com esses projetos, a fim de simplificar uma grande parte do seu processo de desenvolvimento de aplicativos: o front-end. Confira [“Where does the Ionic Framework fit in?”](http://blog.ionic.io/where-does-the-ionic-framework-fit-in/) para obter uma boa compreensão da filosofia de base do Ionic e objetivos.

**Ionic exige actualmente AngularJS a fim de trabalhar em seu pleno potencial.** Enquanto você ainda pode usar a parte CSS do frameworks, você vai perder interações poderosas de interface do usuário, gestos, animações e outras coisas. No futuro, Ionic pretende tornar-se mais agnóstico, a fim de apoiar uma ampla variedade de frameworks JavaScript.

## Como Ionic é licenciado?

Ionic é completamente livre e de código aberto, lançado sob a licença permissiva [MIT](http://opensource.org/licenses/MIT), o que significa que você pode usar Ionic em projetos pessoais ou comerciais livremente. Por exemplo, o MIT é a mesma licença usada por tais projetos populares como jQuery e Ruby on Rails.

Este conteúdo do site e documentação (encontrado no repo [ionic-site](https://github.com/driftyco/ionic-site)) é licenciado sob a licença Apache 2.

## O que é Ionic CLI?

O [CLI](ionic2-docs/glossario.md), ou interface de linha de comando, é uma ferramenta que fornece uma série de comandos úteis para desenvolvedores Ionic. Além de instalar e atualizar Ionic, o CLI vem com um  servidor de desenvolvimento, construção e ferramentas de depuração, e muito mais. Se você estiver usando a Plataforma Ionic, o CLI pode ser usado para exportar o código e até mesmo interagir com a sua conta por meio de programação.

## O que são componentes?

Componentes em Ionic são elementos de interface do usuário reutilizáveis que servem como blocos de construção para seu aplicativo móvel. Componentes são feitos de HTML, CSS, e as vezes JavaScript. Cada componente Ionic se adapta a plataforma na qual seu aplicativo está sendo executado. Chamamos isso de **Platform Continuity** e vai mais a fundo sobre como ele funciona em Theming.

## O que é theming?

Os temas são conjuntos de estilos que são aplicados a um aplicativo. Ionic utiliza um tema claro por padrão, mas ele também vem com um tema escuro. Além de theming, **Platform Continuity** do Ionic permite os componentes terem estilos específicos da plataforma. Isto significa que estilos do aplicativo será alterada com base na plataforma (iOS, Android, etc.) em que está sendo executado, oferecendo a seus usuários uma experiência com a qual está familiarizado.

## Como funciona a navegação?

Navegação funciona como uma pilha - **push** uma página para a pilha para navegar até ele, e **pop** para voltar. Modais e alertas também podem ser exibidos, empurrando-os para a pilha de navegação.

## Quem está por trás do Ionic?

Ionic foi originalmente construído por [@benjsperry](https://twitter.com/benjsperry), [@adamdbradley](https://twitter.com/adamdbradley) e [@maxlynch](https://twitter.com/maxlynch). Depois de lançar uma versão alfa do Ionic em Novembro de 2013, lançou uma versão 1.0 beta em Março de 2014 e uma 1.0 final em Maio 2015.

Agora, Ionic tem uma comunidade internacional maciça de desenvolvedores e colaboradores que impulsionam seu crescimento e adoção. As empresas pequenas e grandes estão usando Ionic para criar aplicativos melhores, mais rápido. Em 2015 os desenvolvedores Ionic teria criado mais de 1.3M aplicativos com o Ionic, um número que continua a crescer a cada dia.
