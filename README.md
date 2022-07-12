# ComandosDotNetCLI
Guia de comando mais utilizado em dotnet

# Criando aplicações em .NET
 
Para criar uma Solution utilizamos o sln
 *dotnet new sln --name <Nome da solution>

Para criar um projeto WEBAPI 
 *dotnet new webapi --name <Nome do projeto> -- output <Pasta onde serar criado>

Para adicionar a referencia do projeto a solution
 *dotnet sln add <Caminho do arquivo csproj (.\APP\APP.csproj)>


# Criando executáveis e pacotes das aplicações .NET

Para compilar a aplicação em release, podemos utilizar a flag "--configuration" no comando build.

 *dotnet build -- configuration Release

Para gerar os arquivos de publicação dessa aplicaçõa podemos utilizar o  comando "Publish" com a flag -- configuration.

 *dotnet publish --configuration Release

E para gerar m pacote da sua biblioteca ao invés de um executavel caso queira utilizamos o comando "pack".

 *dotnetpack --configuration Release


# Criando Migrations

Para gerar as migrations o comando é composto por: dotnet ef migrations add <nome que identifique a migration> -s <Porjetos que contem as configurações do projeto> -o <Caminho aonde será geradas as migrations>


 *dotnet ef migrations add UpdateNameTabeleProject -s ..\DevFreela.API\DevFrella.API.csproj -o .\Persistence\Migrations

Agora para aplicar as migrations basta usar comando: dotnet ef database update -s <Cominho que contem as configurações do projeto>


 *dotnet ef database update -s ..\DevFreela.API\DevFrella.API.csproj
