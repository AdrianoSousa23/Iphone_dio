# Iphone_dio
criando uma interação de um iphone

## Diagrama de Classes

```mermaid
classDiagram
    class Iphone {
        +ligar(numero: String)
        +atender()
        +iniciarCorreioVoz()
        +exibirPaginas()
        +adicionarPagina()
        +atualizarPagina()
        +tocar(musica: String)
        +pausarMusica()
        +selecionarMusica()
    }
    interface AparelhoTelefonico {
        +ligar(numero: String)
        +atender()
        +iniciarCorreioVoz()
    }
    interface NavegadorInternet {
        +exibirPaginas()
        +adicionarPagina()
        +atualizarPagina()
    }
    interface ReprodutorMusica {
        +tocar(musica: String)
        +pausarMusica()
        +selecionarMusica()
    }
    class ExecutandoIphone {
        +main(args: String[])
        -realizarAcao(iphone: Iphone, escolha: String)
    }
    Iphone --|> AparelhoTelefonico
    Iphone --|> NavegadorInternet
    Iphone --|> ReprodutorMusica


```
