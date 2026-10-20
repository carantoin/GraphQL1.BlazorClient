# GraphQL1 — Blazor Client

Standalone Blazor WebAssembly client for sending GraphQL `query` and `mutation` operations to an existing GraphQL endpoint.

## Requirements
- .NET 8 SDK
- Your GraphQL API running and its endpoint URL (often `/graphql`)

## Run
From this folder:

```bash
dotnet restore
dotnet run --project GraphQL1.BlazorClient
```

Open the HTTPS URL printed in the terminal (the default launch profile uses `https://localhost:7194`). Enter your API's actual GraphQL endpoint in the endpoint field.

## Features
- GraphQL query and mutation editor
- JSON variables editor and validation
- Sends POST requests with `application/json`
- Pretty-prints JSON responses and GraphQL errors
- Shows HTTP errors and request duration
- Responsive dark UI

## Connect it to the coursework API
The client is intentionally schema-neutral because the GraphQL schema and endpoint of the existing repository could not be verified from the repository page alone. Replace the sample `query { __typename }` with fields and mutations that exist in your schema.

If the browser reports a CORS error, configure CORS in the API project to allow the client origin, e.g. `https://localhost:7194`. CORS must be configured on the API server; it cannot be fixed in this client.

## Notes
This client does not invent CRUD operations or model fields. To wire dedicated pages (list/create/edit/delete) to the coursework domain, the exact GraphQL schema or the source archive is needed.
