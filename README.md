# Project & Item Templates

A curated set of .NET templates for bootstrapping projects and configs. Built around my workflow, but easy to fork or adapt.

## Prerequisites

- [.NET SDK](https://dotnet.microsoft.com/download)

## Installation

### Manual

1. Clone the repo:
   ```sh
   git clone https://github.com/disgone/bitcrafter-templates.git
   ```

2. Go to the repo directory:
   ```sh
   cd bitcrafter-templates
   ```

3. Install the templates:
   ```sh
   dotnet new install .
   ```

## Usage

Once installed, use the templates with `dotnet new`.

### See Available Templates

```sh
dotnet new list
```

### Create a Project

```sh
dotnet new bitcrafter-buildprops
```

With optional metadata:

```sh
dotnet new bitcrafter-buildprops -au "Janet Doe" -c "Some Company, LLC"
```

## Templates

### `bitcrafter-editorconfig`

Adds a `.editorconfig` file to help keep code style consistent across your projects.

### `bitcrafter-buildprops`

Creates a `Directory.Build.props` file with common project settings, designed to centralize build configurations:

-   **Assembly Metadata**: Configures common assembly information like authors, company, and copyright.
-   **Code Analysis**: Enables .NET analyzers and enforces code style in build. By default, build warnings are treated as errors.
-   **Deterministic Builds**: Ensures reproducible builds by setting the `Deterministic` property to `true`.
-   **Source Link**: Conditionally enables Source Link properties for projects intended to be packed as NuGet packages, improving debugging experience.
-   **Central Package Management (CPM)**: Optionally enables CPM for the solution, promoting consistent package versioning.

**Usage with optional parameters:**

```sh
dotnet new bitcrafter-buildprops -au "Janet Doe" -c "Some Company, LLC" --twae false --cpm false
```

**Parameters:**
-   `-au` or `--authors`: Sets the 'Authors' assembly metadata.
-   `-c` or `--company`: Sets the 'Company' assembly metadata.
-   `--twae` or `--treat-warnings-as-errors`: Set to `true` (default) to treat build warnings as errors, or `false` to allow warnings.
-   `--cpm` or `--enable-cpm`: Set to `true` (default) to enable Central Package Management, or `false` to disable.