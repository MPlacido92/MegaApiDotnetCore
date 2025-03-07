<table align="center">
    <tr>
        <td align="center" width="25%">
            <img src="https://vignette.wikia.nocookie.net/megaman/images/2/22/Cutman.png" alt="MegaMan Bosses API">
        </td>
        <td align="center" width="75%">
          
# MegaMan Bosses API
          
[![Latest release](https://img.shields.io/github/v/release/felipeAguiarCode/MegaApiDotnetCore)](https://github.com/felipeAguiarCode/MegaApiDotnetCore/releases/latest)
  <br>
        </td>
    </tr>
</table>

<p align="center">
  Este projeto é uma API feita em .NET para listar os dados dos bosses de MegaMan. O objetivo principal é ser um backend que fornece JSONs no formato especificado abaixo.
  <br />
</p>
<p align="center">
  Guides e documentação podem ser encontrados na <a href="https://github.com/seu-usuario/seu-repositorio/wiki">Wiki tab</a>.
</p>

<p align="center">
    <img src="_docs\assets\icon.png">
</p>

## Uso

Para executar esta API, seu PC deve estar equipado com o .NET Core SDK 3.1 ou superior e Visual Studio ou qualquer editor de código de sua preferência.

## Estrutura do JSON

A API fornecerá dados no seguinte formato:

```json
{
  "Id": 1,
  "Code": "DLN/DRN-003",
  "Name": "Cutman",
  "HP": 150,
  "Picture": "https://vignette.wikia.nocookie.net/megaman/images/2/22/Cutman.png"
}
```

## Última versão

Versões estáveis são lançadas periodicamente, com base no branch `master`, para garantir uma experiência mais estável e agradável.

Você pode encontrar a última versão estável [aqui](https://github.com/seu-usuario/seu-repositorio/releases/latest).

Versões Canary são compiladas automaticamente para cada commit no branch `master`. Essas versões podem ser instáveis ou completamente quebradas e são recomendadas apenas para usuários experientes.

Você pode encontrar a última versão canary [aqui](https://github.com/seu-usuario/Canary-Releases/releases/latest).

## Endpoints

| Método | URL                      | Descrição                    | Respostas           |
|--------|--------------------------|------------------------------|---------------------|
| GET    | `/api/v1/robots`         | Listar todos os bosses       | 200 OK              |
| GET    | `/api/v1/robots/{id}`    | Obter boss por ID            | 200 OK, 404 Not Found |
| POST   | `/api/v1/robots`         | Criar um novo boss           | 200 OK              |

## Técnicas Utilizadas

- **ASP.NET Core:** Utilizado para construir a API.
- **Entity Framework Core:** Utilizado para interações com o banco de dados.
- **Newtonsoft.Json:** Utilizado para serialização e desserialização de JSON.
- **Dependency Injection:** Implementado para gerenciar as dependências do projeto.

## Dependências

As dependências do projeto são:

| Dependência                                      | Versão    |
|--------------------------------------------------|-----------|
| [Microsoft.EntityFrameworkCore](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore/)          | 3.1.8     |
| [Microsoft.EntityFrameworkCore.Design](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.Design/)    | 3.1.8     |
| [Microsoft.EntityFrameworkCore.SqlServer](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/) | 3.1.8     |
| [Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json/)                          | 12.0.2    |

## Estrutura do Projeto

A estrutura do projeto é baseada na seguinte árvore de pastas:

```
.vs
.vscode
bin
Controllers
Database
middlewares
Models
obj
Properties
Services
appsettings.Development.json
appsettings.json  
global.json
MegamanApi.csproj  
MegamanApi.sln
Program.cs
Startup.cs
```

## Documentação

Se você está planejando contribuir ou apenas quer aprender mais sobre este projeto, por favor leia nossa [documentação](docs/README.md).

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

⌨️ FelipeAguiar -
[Github](https://github.com/felipeAguiarCode)
