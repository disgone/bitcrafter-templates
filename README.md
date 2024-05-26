# Project & Item Templates

An opinionated set of pre-configured file templates aimed to speed up .NET project initialization and configuration. This collection is tailored to my personal workflow and preferences, but feel free to fork or adapt it to your needs.

## Prerequisites

- [.NET SDK](https://dotnet.microsoft.com/download) installed on your machine.

## Getting Started

To start using these templates, you'll need to install them. There are a couple of options:

### Manual Install

1. Clone the repository to your local machine:
   ```sh
   git clone https://github.com/disgone/bitcrafter-templates.git
   ```

2. Navigate to the repository directory:
   ```sh
   cd bitcrafter-templates
   ```

3. Install the templates:
   ```sh
   dotnet new install .
   ```

## Usage

Once the templates are installed, you can create new projects or items using them. You can view a list of the available templates using the `dotnet new list` command.

### Usage Example

To create a new project using the `bitcrafter-buildprops` template, run:
```sh
dotnet new bitcrafter-buildprops
```

You can also specify additional options, for example:
```sh
dotnet new bitcrafter-buildprops -au "Janet Doe" -c "Some Company, LLC"
```

## Templates

Here's a small overview of the templates currently available (and documented).

- `bitcrafter-editorconfig` - Generates and adds an `.editorconfig` pre-setup for usage at U.S. Bank to help guide and follow good coding practices.

- `bitcrafter-buildprops` - Generates and adds a `Directory.Build.props` configuration file to set generic assembly information, enable .NET analyzers, and configure unit test projects. Author and company information can be overridden on creation:
  ```sh
  dotnet new bitcrafter-buildprops -au "Janet Doe" -c "Some Company, LLC"
  ```
