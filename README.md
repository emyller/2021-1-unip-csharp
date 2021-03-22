# Experimento com .NET

Este projeto foi criado para fins de aprendizado durante a extensão do curso de
Análise e Desenvolvimento de Sistemas da UNIP.


## O que está incluso

- _Software Development Kit_ (SDK) do framework Microsoft .NET, que inclui o compilador C# oficial.
- Microsoft SQL Server 2019 (licença para desenvolvedores).


## Requerimentos

- É necessário instalar e executar o [Docker][].
- Para contribuir ao código, é necessário usar [Git][].
- Linux. Mas com Docker, também é possível rodar no Windows (versão Pro).


[Docker]: https://docs.docker.com/get-docker/
[Git]: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git


## Como rodar o código C#

Este projeto inclui, no diretório `src` (abreviação para "source", ou _fonte_),
um projeto C# simples. Você pode modificá-lo para seus exercícios ou qualquer
outra finalidade não comercial.

Para executar a aplicação:

```
$ ./bin/dotnet run
Hello World!
The current time is 03/09/2021 23:53:17
```

O script `./bin/dotnet` é um "atalho" para o programa "dotnet" incluído na
imagem Docker [oficial](https://hub.docker.com/_/microsoft-dotnet-sdk) da
Microsoft, e pode ser usada também com outros parâmetros, quando necessário:

```
$ ./bin/dotnet --info
.NET SDK (reflecting any global.json):
 Version:   5.0.201
 Commit:    a09bd5c86c

Runtime Environment:
 OS Name:     debian
 OS Version:  10
 OS Platform: Linux
...
```


## Acesso ao banco de dados

Este projeto também inclui o Microsoft SQL Server, através da imagem Docker
[oficial](https://hub.docker.com/_/microsoft-mssql-server). Por padrão, ao
executar o programa `dotnet` descrito acima, o sistema de banco de dados já será
executado e deverá estar pronto para uso.

Alternativamente, você poderá executá-lo isoladamente com o seguinte comando:

```
$ ./bin/mssql
```

Note que o comando acima somente funcionará se a porta 1433 não estiver sendo
usada por outro processo.

A conexão ao banco de dados pode ser feita com os seguintes parâmetros:

- Usuário: `sa`.
- Senha: `#Secret0#`.
- Porta: `1433`.
- Banco de dados: `master`.
- Hostname: `database`, quando dentro do projeto.

Você também pode utilizar uma ferramenta externa para conexão ao banco de dados,
como o [DBeaver](https://dbeaver.io/), que oferece uma interface gráfica para
manipulação de dados. Para isso, substitua o _hostname_ acima por `localhost`.
