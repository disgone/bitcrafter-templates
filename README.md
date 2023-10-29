# Project & Item Templates

An opinionated set of pre-configured file templates aimed to speed up dotnet
project initialization and configuration.
This collection is tailored to my personal workflow and preferences but feel
free to fork or adapt to your needs.

## Getting Started

To start using these templates, you'll need to install them and there are a
couple of options:

### Manual install

Clone the repository to your local machine:
`git clone https://github.com/disgone/bitcrafter-templates.git`

Navigate to the repository directory
`cd bitcrafter-templates`

Install the templates
`dotnet new install .`

## Usage

Once the templates are installed, you can create new projects or items using
them. You can view a list of the
available templates using the `dotnet new list` command.

```
dotnet new bitcrafter-buildprops
```

## Templates

Here's a small overview of the templates currently available (and documented).

- `bitcrafter-editorconfig` - Generates and adds an `.editorconfig` pre-setup
  for usage at U.S. Bank to help guide and follow good coding practices.

- `bitcrafter-buildprops` - Generates and adds a `Directory.Build.props`
  configuration file to set generic assembly information, enables .NET
  analyzers, and configures unit test projects. Author and company information
  can be overriden on
  creation `dotnet new bitcrafter-buildprops -au "Janet Doe" -c "Some Company, LLC"`