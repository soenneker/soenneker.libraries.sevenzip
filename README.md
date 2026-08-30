[![](https://img.shields.io/nuget/v/soenneker.libraries.sevenzip.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.libraries.sevenzip/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.libraries.sevenzip/build-and-test.yml?style=for-the-badge)](https://github.com/soenneker/soenneker.libraries.sevenzip/actions/workflows/build-and-test.yml)
[![](https://img.shields.io/nuget/dt/soenneker.libraries.sevenzip.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.libraries.sevenzip/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.libraries.sevenzip/codeql.yml?label=CodeQL&style=for-the-badge)](https://github.com/soenneker/soenneker.libraries.sevenzip/actions/workflows/codeql.yml)

# Soenneker.Libraries.SevenZip

The standalone 7-Zip command-line executable packaged for Windows .NET applications.

## Install

```bash
dotnet add package Soenneker.Libraries.SevenZip
```

The package copies `7za.exe` beneath the application output directory:

```csharp
string sevenZip = Path.Combine(AppContext.BaseDirectory, "Resources", "7za.exe");
```

This package supplies the executable but does not run it or provide a managed archive API. Pass archive names, passwords, and output paths through `ProcessStartInfo.ArgumentList`; do not construct a shell command by concatenating them.

Always check the process exit code. When extracting untrusted archives, use a dedicated empty directory and enforce limits on archive size, extracted size, file count, and processing time before moving files into their final location.
