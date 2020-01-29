# Steps to reproduce

1. Create a new blazor wasm project using the latest template.

> Note: Make sure to run
>```
>dotnet new -i Microsoft.AspNetCore.Blazor.Templates::3.2.0-preview1.20073.1
>```
> to get the template

2. Deploy the app to IIS using the following command
```
dotnet clean --configuration Release && dotnet publish --configuration Release -o <PATH_TO_IIS_FOLDER>
```
Suppose that the app is exposed from IIS on http://localhost/blazorwasm32

3. Open http://localhost/blazorwasm32

4. Open the Network tab in DevTools and look for the failed request for `blazorwasm32.Shared.pdb`

Screenshot of the result:

![blazor-wasm](https://user-images.githubusercontent.com/1857705/73352302-7cd53b00-4299-11ea-9179-7edc79d5cc7e.png)

