# Fork

Added an option to set a custom `HttpClientHandler` to the underlying gRPC channel used in `OpenTelemetry.Exporter.OpenTelemetryProtocol`.

Forked versions were `1.0.0-rc4` and `core-1.1.0-beta2`

## Building and Packing

This project uses MinVer so you'll want to add tags to define nupkg names

I've used `1.0.0-rc4-fork1` and `core-1.1.0-beta2-fork1`

After git tagging, inside Solution folder run:

```powershell
dotnet build --configuration Release --no-restore -p:Deterministic=true

dotnet pack OpenTelemetry.proj --configuration Release --no-build
```

Packages will be generate.

You can reference them locally in consuming projects for simplicity.