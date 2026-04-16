# Vonage.VerifyV2Only

This project is a **Verify V2-only** class library projection from the main SDK.

## Included source scopes
- `Vonage/VerifyV2/**` (all Verify V2 contracts, models, requests, builders, and the `VerifyV2Client` implementation)
- `Vonage/Common/**` (shared request/client/monad/validation infrastructure used by Verify V2)
- `Vonage/Serialization/**` (JSON converters/helpers used by Verify V2 payloads)

## Why these are required
`IVerifyV2Client` and `VerifyV2Client` depend on:
- Request abstractions (`IVonageRequest`, `VonageRequestBuilder`)
- HTTP client plumbing (`VonageHttpClient`, `VonageHttpClientConfiguration`)
- Monads and validation (`Result<T>`, `Unit`, input validation)
- Serialization helpers/converters (`JsonSerializerBuilder`, custom converters)

All of these live in `Common` and `Serialization`, so they are included with `VerifyV2`.

## Build
```bash
dotnet build Vonage.VerifyV2Only/Vonage.VerifyV2Only.csproj
```
