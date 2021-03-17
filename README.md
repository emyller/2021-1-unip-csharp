# Experimento com .NET

Este projeto foi criado para fins de aprendizado durante a extensão do curso de
Análise e Desenvolvimento de Sistemas da UNIP.


## O que está incluso

- _Software Development Kit_ do framework Microsoft .NET.
- Compilador C#.


## Requerimentos

- É necessário instalar e executar o [Docker][].
- Para contribuir ao código, é necessário usar [Git][].
- Linux. Mas com Docker, também é possível rodar no Windows (versão Pro).


[Docker]: https://docs.docker.com/get-docker/
[Git]: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git


## Como rodar

Para facilitar a instalação e uso das ferramentas, usamos Docker. Vide os
requerimentos acima.

Para executar a aplicação:

```
$ ./bin/run
Hello World!
The current time is 03/09/2021 23:53:17
```

O script `./bin/run` também é capaz de executar qualquer outro programa
disponível na imagem Docker sendo usada, bastando passar o comando como parâmetro:

```
$ ./bin/run dotnet --info
.NET SDK (reflecting any global.json):
 Version:   5.0.201
 Commit:    a09bd5c86c

Runtime Environment:
 OS Name:     debian
 OS Version:  10
 OS Platform: Linux
...
```
