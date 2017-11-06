# dotnet-mono

## For what?

Can be used for multi-targeting build, like

    <PropertyGroup>
        <TargetFrameworks>netstandard2.0;net461</TargetFrameworks>
    </PropertyGroup>

especially fot `dotnet pack` to produce multi-targeting packages.

## Versions

* .net Core SDK 2.0  
* mono 5.4.0.201