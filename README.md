# C# OAuth [Asp.Net Core](https://asp.net) API
Esse projeto � a implementa��o de um servi�o OAuth usando .NET Core 6 baseado no [RFC 6749](https://datatracker.ietf.org/doc/html/rfc6749) 
que regulamenta o protocolo de autentica��o � autoriza��o usando o mecanismo OAuth. 

## Estrutura do projeto 
A solu��o do projeto est� divida em duas pastas 
- Api
	Cont�m �s implementa��es do sistema OAuth para o servidor de autoriza��o.
- Client	
	Cont�m os clientes para plataformas como: 
	- Android 
	- Linux 
	- Windows 
	- Cliente de Teste
## Inciando API
Para inicar a API pela primeira vez � necess�rio:
- Adicionar a chave de conex�o corresponde ao seu banco de dados no arquivo 'appsettings.json' dentro do projeto 'Nexus.OAuth.Api'.
- Rodar a migration dentro do seu servidor com a mesma conex�o, para isso rode o seguinte comando no root do projeto:
	 ``` 
      dotnet ef database update "{connectionString}"
- Caso n�o tenha o EntityFramework instalado em sua m�quina execute esse comando antes do anterior:
   ```
      dotnet tool install dotnet-ef -g
- Caso precise o projeto conta com uma cole��o pronta para testar o projeto no **Postman**.

  [![Rodar no Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/10567804-e51adde7-b8e9-40b2-9e0a-e236f839c5d4?action=collection%2Ffork&collection-url=entityId%3D10567804-e51adde7-b8e9-40b2-9e0a-e236f839c5d4%26entityType%3Dcollection%26workspaceId%3D7eeb276b-b89e-4ae3-af25-94e668ad861e)

> O projeto esta configurado para n�o iniciar o navegador ao depurar, utilize a **porta 4196** do seu localhost para se conectar ao servidor