# DiagramaClasseIphone-BancoSantander
## Modelagem e Diagramação de um Componente iPhone

### Reprodutor Musical
* Métodos: tocar(), pausar(), selecionarMusica(String musica)
### Realizar Chamada
* Métodos: ligar(String numero), atender(), iniciarCorreioVoz()
### Navegador na Internet
* Métodos: exibirPagina(String url), adicionarNovaAba(), atualizarPagina()

```mermaid
classDiagram
    class Usuario {
        - nome: String
        - email: String
        - Musica: musicas
        - NavegadorInternet: navegador
        -Chamada: chamada
    }

    class Música {
        - título: String
        - artista: String
        - álbum: String
        - duração: Int
        + reproduzir()
        + pausar()
        + selecionar()
    }

    class Chamada {
        - númeroTelefone: String
        - tipoChamada: String
        - duração: Int
        + fazerChamada()
        + receberChamada()
        + encerrarChamada()
    }

    class NavegadorInternet {
        - urlAtual: String
        - histórico: String
        + navegar()
        + baixarConteúdo()
    }
    Usuario "1" *-- "N" Música
    Usuario "1" *-- "N" Chamada 
    Usuario "1" *-- "N" NavegadorInternet
```
