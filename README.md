# Octoshift

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/gh-migration-tools/Octoshift/blob/main/LICENSE)
[![CI](https://github.com/gh-migration-tools/Octoshift/actions/workflows/CI.yml/badge.svg)](https://github.com/gh-migration-tools/Octoshift/actions/workflows/CI.yml)

This repository extracts the code of the **Octoshift** library from the [gh-gei](https://github.com/github/gh-gei) **GitHub Enterprise Importer CLI** project and provides it as a NuGet package. Thereby the base code can be reused while creating custom migration extensions for the [GitHub CLI](https://github.com/cli/cli#installation).

> [!NOTE]
> Regarding **Octoshift** library development or issues please visit to the [gh-gei](https://github.com/github/gh-gei) project.

## Usage

### Add NuGet source

As GitHub Packages does not support anonymous access for NuGet feeds you need to create a NuGet source using a GitHub personal access token (PAT) with the scope `read:packages`.

```
dotnet nuget add source https://nuget.pkg.github.com/gh-migration-tools/index.json
  --name gh-migration-tools
  --username USERNAME
  --password PAT
```

> [!TIP]
> Keep the `--username USERNAME` option as it is, just set the `PAT` in the `--password` option.

### Add NuGet package

```
dotnet add package Octoshift --source gh-migration-tools
```
