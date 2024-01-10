# Test package

For testing github's nuget packages repo

## Uploading package

1. In `TestPackage.csproj`, update the version number
2. Create a new tag at the commit of release
3. Create a new github release on that tag
4. Github Actions automatically generates and pushes the package

## Restoring package locally

Run the following inside a console:

- Replace NAME with your github username
- Replace PAT with your Personal Access Token (with `read:packages`)

```sh
nuget add source "https://nuget.pkg.github.com/merijnhendriks/index.json" --name "github-merijnhendriks" --username "NAME" --password "PAT"
```