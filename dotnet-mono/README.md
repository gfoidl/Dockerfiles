# dotnet-mono

## For what?

Can be used for multi-targeting build, like

    <PropertyGroup>
        <TargetFrameworks>netstandard2.0;netcoreapp2.1;netcoreapp2.0;net471;net47;net461;net46;net45</TargetFrameworks>
    </PropertyGroup>

especially for `dotnet pack` to produce multi-targeting packages.

## Versions

* .net Core SDK 2.2   
* mono 5.18.1.0
