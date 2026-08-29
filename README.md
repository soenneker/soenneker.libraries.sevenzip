[![](https://img.shields.io/nuget/v/soenneker.libraries.sevenzip.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.libraries.sevenzip/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.libraries.sevenzip/build-and-test.yml?style=for-the-badge)](https://github.com/soenneker/soenneker.libraries.sevenzip/actions/workflows/build-and-test.yml)
[![](https://img.shields.io/nuget/dt/soenneker.libraries.sevenzip.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.libraries.sevenzip/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.libraries.sevenzip/codeql.yml?label=CodeQL&style=for-the-badge)](https://github.com/soenneker/soenneker.libraries.sevenzip/actions/workflows/codeql.yml)

# Soenneker.Libraries.SevenZip

Adds the 7zip Windows executable, updated daily (if available).

## Install

```bash
dotnet add package Soenneker.Libraries.SevenZip
```

## What it provides

- Adds the 7zip Windows executable, updated daily (if available).
- The file is copied to the output directory, and located at the relative path: `Resources\`.

## How to use it

After installation, resolve the packaged file from the output-relative path above. The package deploys the asset but does not invoke it for you.
