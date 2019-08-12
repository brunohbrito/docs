>[!IMPORTANT]
>If you're testing an ASP.NET Core application, and you're targeting a framework _other_ than `netcoreapp3.0`, you must add an additional package reference: `Microsoft.AspNetCore.App`.
>
>```
>dotnet add package Microsoft.AspNetCore.App
>```
>
>This command adds a _versioned_ package reference to your project. You will need to open the project file and remove the `Version` attribute. The reference should look like the following.
>
>```xml
><ItemGroup>
>  <PackageReference Include="Microsoft.AspNetCore.App" />
></ItemGroup>
>
>Also, if you're using the **.NET Core 2.1 SDK** or earlier, set the SDK type in the testing project file to the web SDK:
>
>```xml
><Project Sdk="Microsoft.NET.Sdk.Web">
>```
