# typst-community/scoop-bucket

[![Tests](https://github.com/typst-community/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/typst-community/scoop-bucket/actions/workflows/ci.yml)
[![Excavator](https://github.com/typst-community/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/typst-community/scoop-bucket/actions/workflows/excavator.yml)

A bucket containing various unofficial [typst](https://typst.app/) tools, for [scoop](https://scoop.sh), the Windows command-line installer.

## How do I use this template?

3. Allow writing to the repository from within GitHub Actions:
   - Navigate to `Settings` - `Actions` - `General` - `Workflow permissions`.
   - Select `Read and write permissions`.
   - Then `Save`.
6. Create new manifests by copying `bucket/app-name.json.template` to
   `bucket/<app-name>.json`.
8. If you'd like your bucket to be indexed on `https://scoop.sh`, add the
   topic `scoop-bucket` to your repository.

## How do I install these manifests?

After manifests have been committed and pushed, run the following:

```pwsh
scoop bucket add typst-community https://github.com/typst-community/scoop-bucket
scoop install typst-community/⟨app-name⟩
```

## How do I contribute new manifests?

To make a new manifest contribution, please read the [Contributing
Guide](https://github.com/ScoopInstaller/.github/blob/main/.github/CONTRIBUTING.md)
and [App Manifests](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests)
wiki page.
