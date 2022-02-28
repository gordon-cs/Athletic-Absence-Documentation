# Backend

## API Setup

- Connect to the development VM

  - Make sure you have Multifactor Authentication setup [here](https://cts.gordon.edu/knowledge/setupmfa/)
  - Follow instructions [here](https://cts.gordon.edu/knowledge/how-to-connect-to-a-remote-computer-from-a-non-gordon-managed-windows-computer/) to connect to it
    - `server name: CS-Athletics`
    - `domain: gordon.edu`

- `git clone https://github.com/gordon-cs/athletic-form`
- `cd athletic-form/API`
- Open `AthleticFormAPI.sln` in Visual Studio 2019

---

## Backend with local non-Gordon Database (VS Code)

- First, make sure you have docker-compose installed on your system (follow instructions [here](https://docs.docker.com/compose/install/) (make sure to select the correct operating system)
- `cd clone-path/API/api-core/AthleticFormCore/AthleticSQLServer/ServerConfiguration`
- replace SA_PASSWORD with a password of your choosing (Make sure to use special characters and at least one number)
- Make sure docker is running. If on docker desktop, make sure you are logged in with your docker account
- `sudo docker-compose up`
- in Azure Data Studio, add a new connection
- Server: localhost, username: SA, Password: Password as specified in the docker-compose.yml file
- Once you are connected, open and run the three queries that are included, first the DatabaseCreation.sql, then the CreateTable.SQL and then the InsertData.SQL query
- Be sure to leave the server running to connect with the backend in the next step

- We have since migrated to .NET Core, thus the API can now be run on any OS.
- Steps are exactly the same as above, however instead of opening the solution in Visual Studo, open one of the two projects in VS code:
  - Be sure to have the C# extention (Microsoft) installed
  - Specify the project to load (follow instructions [here](https://code.visualstudio.com/docs/languages/csharp), in particular, the section starting with `Roslyn and OmniSharp`)
  - Make sure you have the secrets.json in your `~/.microsoft/usersecrets/<user_secrets_id>/secrets.json` folder on Unix-like operating systems, and for Windows, `%APPDATA%\Microsoft\UserSecrets\<user_secrets_id>\secrets.json` (for the <user_secrets_id>, check the <UserSecretsId> field in AthleticFormCore.csproj file)
  - In secrets.json, add
    `{ "ConnectionString": "Server=localhost; Database=AthleticDatabase;User Id=sa; Password=your_password }`
  - `cd repoPath/API/api-core/AthleticFormCore`
  - `dotnet run`
