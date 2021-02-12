# IdentityServer4Complete
Complete Identity Server 4 Asp.net Identity Role Based Solution with both Client Credential and Resource Owner Password Grany Type. 

## Features
- IdentityServer4 Full STS Implementation. (STS here refers to IdentityServer Project)
- Asp.net Core Identity Users and Roles Fully implemented
- .NET 5 and Entity Framework Core 5
- Custom profile and Custom Tokens implementations
- Full Client App Accessing secure API Endpoint
- Database Seeding with Configuration and Identity Users (with roles) examples
- Registration and Login API Endpoints in STS
- Headless/Cookieless No UI Implementation and API call and token exchange for Both Native and SPA apps


## How to Use?
1. Modify ConnectionString on IdentityServer configuration (Use Sqlite or any other ef core provider for database)
2. For Relation data stores, Run Migration Database update and for non-relational data store add the proper encore nuget extension, remove Migration Files and make code modifications to run **EnsureDatabaseCreate** command is executed
3. Run both IdentityServer project (STS) and API by the command `dotnet run`
4. Run the client console app by the command `dotnet run`

## Todo

- Modify Db Provider (you can use any EFCore Database providers by making correct modifications)
- Replace `AddDeveloperSigningCredential` with `AddSigningCredential` method in STS statup class using proper Signing credentials It is so critical for production apps to use proper signing certificare since we are passing both users and roles information across services and singnature is the only binding contract for the claims integirity.
- Add more Clients, APIs and Scopes by modifying the Config.CS file in STS Note: After initial run, you need to update database directly.