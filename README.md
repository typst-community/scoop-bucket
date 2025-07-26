# typst-community/scoop-bucket

[![Tests](https://github.com/typst-community/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/typst-community/scoop-bucket/actions/workflows/ci.yml)
[![Excavator](https://github.com/typst-community/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/typst-community/scoop-bucket/actions/workflows/excavator.yml)

This is a bucket for [Scoop](https://scoop.sh), the Windows command-line installer.

This bucket contains various unofficial [Typst](https://typst.app/) tools:

- **Writing**

  - [tinymist](https://myriad-dreamin.github.io/tinymist/), an integrated language service
  - [typstyle](https://typstyle-rs.github.io/typstyle/), a code formatter
  - [shiroa](https://myriad-dreamin.github.io/shiroa/), for creating online books

- **Conversion**

   - [typlite](https://crates.io/crates/typlite), for converting to markdown

- **Package development**

   - [tytanic](https://typst-community.github.io/tytanic/), a test runner
   - [typship](https://github.com/sjfhsjfh/typship), for sending packages to the [universe](https://typst.app/universe/)

## How do I install these tools?

Run the following:

```pwsh
scoop bucket add typst-community https://github.com/typst-community/scoop-bucket

scoop install typst-community/⟨tool-name⟩
# For example:
# scoop install typst-community/tinymist
```

> [!NOTE]
>
> The [official Typst compiler](https://github.com/typst/typst/) is not included in this bucket. You can install it from the [Main bucket](https://github.com/ScoopInstaller/Main/) instead:
>
> ```pwsh
> scoop bucket add main
> scoop install main/typst
> ```

## How do I contribute new manifests?

To make a new manifest contribution, please read the [Contributing
Guide](https://github.com/ScoopInstaller/.github/blob/main/.github/CONTRIBUTING.md)
and [App Manifests](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests)
wiki page.
