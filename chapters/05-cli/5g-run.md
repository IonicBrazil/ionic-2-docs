# Run #


| Comando | Descrição |
|---------|-----------|
| ionic run | Executar projeto ionic em um dispositivel conectado |
| **Flags** | |
| --livereload&#124; | |
| --address | |
| --port&#124;-p | |
| --livereload-port&#124;-r | |
| --consolelogs&#124;-c | Imprimir logs do console do aplicativo no Ionic CLI (livereload requirido) |
| --serverlogs&#124;-s | Imprimir logs do servidor de desenvolviment no Ionic CLI (livereload requirido) |
| --debug&#124;--release | |
| --device&#124;--emulator&#124;--target=FOO | |

# Descrição #

O comando *run* irá fazer um deploy do aplicativo para a plataforma de um dispositivo específicado. Você também pode executar *live reload* (atualização dos arquivos em tempo real), adicionando a opção *--livereload*. A funcionalidade do *live reload* é similiar ao que contém no comando *ionic serve*, porém ao invés de desenvolver e debugar seu aplicativo utilizando um navegador pardão, o proprio compilador hibrido irá observar todas as mudanças dos arquivos, e recarregar o aplicativo quando necessário. Isto reduz a necessidade de fazer *rebuild* constantemente a cada pequena mudanças. Entretanto, todas as alterções realizadas nos plugins, vai ser necessario realizar um *rebuild* completo. Para o live reload funcionar, é necessario que a maquina de desenvolvimento e o dispositivel esteja na mesma rede local e o dispositivel deve ter suporte a [web socktes](http://caniuse.com/websockets).
