# Canary - ABA Cemtext Bank File Validator
[![Unit Test Action status](https://github.com/sbartholomeusz/canary/workflows/dotnet-unit-tests/badge.svg)](https://github.com/sbartholomeusz/canary/actions)

## Overview
Canary is a utility for validating bank files in the Australian Bankers Association (ABA) format (aka Cemtext).

The application is accessible using either of the following clients:
* <b>Windows WPF desktop application</b>: WPF C# .NET Core 3.1.
* <b>Web application</b>: Blazor WebAssembly ASP.NET Core 3.1.

![WPF App Screenshot](/docs/wpf-screenshot.png?raw=true "")

![WASM App Screenshot](/docs/blazor-web-screenshot.png?raw=true "")

## Solution Structure
* <u>Canary.Core</u> - Contains the core bank file validation logic.
* <u>Canary.Form</u> - User interface layer consisting of a WPF form.
* <u>Canary.Logging</u> - Application logging layer leveraging Log4Net.
* <u>Canary.Web</u> - Contains the Blazor WebAssembly web application.
* <u>Canary.Tests</u> - Unit and integration tests

![Solution Dependency Map](/docs/high-level-overview.png?raw=true "Solution Structure")

## Getting Started - Desktop Application
1. Clone the repo
```console
git clone https://github.com/sbartholomeusz/canary
```
<br />

2. Build the solution
```console
cd canary\src\
dotnet build --configuration Release
```
<br />

3. Launch the WPF form
```console
Canary.Form\bin\Debug\netcoreapp3.1\Canary.exe
```
<br />

## Getting Started - Web Application
1. Clone the repo
```console
git clone https://github.com/sbartholomeusz/canary
cd canary\src\Canary.Web
```
<br />

2. Install the self-signed certificate
```console
dotnet dev-certs https --trust
```
<br />

3. Start the web application (https://localhost:5001)
```console
dotnet run
```
<br />

## Dependencies
* [MahApps](https://mahapps.com/docs/guides/quick-start) - WPF application theming
* [Log4Net](https://logging.apache.org/log4net/release/manual/introduction.html) - Application logging
<br />

## License
[MIT Licence](http://en.wikipedia.org/wiki/MIT_License)
<br />

## References
* https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details
* http://www.anz.com/Documents/AU/corporate/clientfileformats.pdf
