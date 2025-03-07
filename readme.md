# MegaMan Bosses API

## Contexto

Este projeto é uma API feita em .NET para listar os dados dos bosses de MegaMan. O objetivo principal é ser um backend que fornece JSONs no formato especificado abaixo.

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

## Especificações do Projeto

```xml
<Project Sdk="Microsoft.NET.Sdk.Web">

  <PropertyGroup>
    <TargetFramework>netcoreapp3.1</TargetFramework>
  </PropertyGroup>

  <ItemGroup>
    <PackageReference Include="Microsoft.EntityFrameworkCore" Version="3.1.8" />
    <PackageReference Include="Microsoft.EntityFrameworkCore.Design" Version="3.1.8">
      <IncludeAssets>runtime; build; native; contentfiles; analyzers; buildtransitive</IncludeAssets>
      <PrivateAssets>all</PrivateAssets>
    </PackageReference>
    <PackageReference Include="Microsoft.EntityFrameworkCore.SqlServer" Version="3.1.8" />
    <PackageReference Include="Newtonsoft.Json" Version="12.0.2" />
  </ItemGroup>

</Project>
```

## Endpoints do Projeto

### Listar todos os bosses

- **URL:** `/api/v1/robots`
- **Método:** `GET`
- **Resposta de Sucesso:** `200 OK`

```json
[
  {
    "Id": 1,
    "Code": "DLN/DRN-003",
    "Name": "Cutman",
    "HP": 150,
    "Picture": "https://vignette.wikia.nocookie.net/megaman/images/2/22/Cutman.png"
  },
  ...
]
```

### Obter boss por ID

- **URL:** `/api/v1/robots/{id}`
- **Método:** `GET`
- **Resposta de Sucesso:** `200 OK`
- **Resposta de Erro:** `404 Not Found`

```json
{
  "Id": 1,
  "Code": "DLN/DRN-003",
  "Name": "Cutman",
  "HP": 150,
  "Picture": "https://vignette.wikia.nocookie.net/megaman/images/2/22/Cutman.png"
}
```

### Criar um novo boss

- **URL:** `/api/v1/robots`
- **Método:** `POST`
- **Resposta de Sucesso:** `200 OK`

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

## Técnicas Utilizadas

- **ASP.NET Core:** Utilizado para construir a API.
- **Entity Framework Core:** Utilizado para interações com o banco de dados.
- **Newtonsoft.Json:** Utilizado para serialização e desserialização de JSON.
- **Dependency Injection:** Implementado para gerenciar as dependências do projeto.

## Como utilizar

### Pré-requisitos

- .NET Core SDK 3.1 ou superior
- Visual Studio ou qualquer editor de código de sua preferência

### Passos para execução

1. Clone este repositório:
   ```sh
   git clone https://github.com/seu-usuario/seu-repositorio.git
   ```

2. Navegue até o diretório do projeto:
   ```sh
   cd seu-repositorio
   ```

3. Restaure as dependências do projeto:
   ```sh
   dotnet restore
   ```

4. Execute a aplicação:
   ```sh
   dotnet run
   ```

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
