# csharp_asset_sdk

Kiota-generated C# client for the **Asset** OpenAPI contract.

| Item | Value |
|------|--------|
| Package | `ExploraProp.Asset.ApiClient` |
| Repo | [`ExploraProp/csharp_asset_sdk`](https://github.com/ExploraProp/csharp_asset_sdk) |
| Contracts | `ExploraProp/OpenAPI-contracts` → newest `apis/asset/openapi.<YYYY.MM.DD.HH.MM>.json` |
| Notify | `openapi-spec-updated` (`spec_path` in payload) |
| Generate | **API.Scripts** only (`generate-client`) — no `generate.ps1` |

## Local regenerate

```powershell
dotnet tool restore
dotnet tool run api-scripts -- generate-client --spec openapi/openapi.v1.json --bc asset --out src/Generated
dotnet pack src/ExploraProp.Asset.ApiClient.csproj -c Release -p:PackageVersion=2026.9.13.241
```

## CI

[`.github/workflows/openapi-spec-updated.yml`](.github/workflows/openapi-spec-updated.yml) on `repository_dispatch`.
