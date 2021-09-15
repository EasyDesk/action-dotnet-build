# action-dotnet-build
An action that can be used to run the `dotnet build` command on a project, after restoring the projects and their dependencies.

## Usage

### Usage example
```yaml
    steps:
      - uses: EasyDesk/action-dotnet-build@v1
        with:
          # (Optional) Additional arguments for dotnet build.
          build-args: -v normal

          # (Optional) Build configuration, defaults to 'Release'
          # If the version starts with the 'v' prefix, it will be removed to conform to the requirements of dotnet pack.
          build-configuration: Release

          # (Optional) The path of the project to build; if omitted, the whole solution is built
          path: ./<project-name>/
```
