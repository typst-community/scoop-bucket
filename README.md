# typst-community/scoop-bucket

[![Tests](https://github.com/typst-community/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/typst-community/scoop-bucket/actions/workflows/ci.yml)
[![Excavator](https://github.com/typst-community/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/typst-community/scoop-bucket/actions/workflows/excavator.yml)

This is a bucket for [Scoop](https://scoop.sh), the Windows command-line installer.

This bucket contains various unofficial [Typst](https://typst.app/) tools, and [unofficial builds of official tools][dev-builds]:

- **Writing**

  - [tinymist](https://myriad-dreamin.github.io/tinymist/), an integrated language service
  - [typstyle](https://typstyle-rs.github.io/typstyle/), a code formatter
  - [katvan](https://katvan.app), an editor with a bias for right-to-left editing
  - [tyx](https://tyx-editor.com), a LyX-like editor

- **Conversion and generation**

   - [hayagriva](https://github.com/typst/hayagriva), for testing bibliography files and converting from BibTeX `.bib` format to YAML format. ([unofficial build][dev-builds])
   - [shiroa](https://myriad-dreamin.github.io/shiroa/), for creating online books
   - [typlite](https://crates.io/crates/typlite), for converting to markdown
   - [typsite](https://typ.rowlib.com/en/), for generating static sites

- **Package development**

   - [typst-package-check](https://github.com/typst/package-check), the official tool to check Typst packages. ([unofficial build][dev-builds])
   - [tytanic](https://typst-community.github.io/tytanic/), a test runner
   - [utpm](https://github.com/typst-community/utpm), an unofficial Typst package manager
   - [typship](https://github.com/sjfhsjfh/typship), for sending packages to the [universe](https://typst.app/universe/)
   - [wasi-stub](https://github.com/astrale-sharp/wasm-minimal-protocol#wasi-stub), for [stubbing all WASI functions](https://typst.app/docs/reference/foundations/plugin/#wasi) in a WebAssembly file

- **Miscellaneous**

   - [typst-ts-cli](https://myriad-dreamin.github.io/typst.ts/cookery/guide/compiler/ts-cli.html), for running in JavaScriptWorld
   - [typst-upgrade](https://github.com/Coekjan/typst-upgrade), for upgrading typst packages
   - [typstscript](https://github.com/ChaseRensberger/typstscript), for creating screenplays

- **Extensions**

   - [mdbook-typst-highlight](https://github.com/sitandr/mdbook-typst-highlight), for highlighting typst code in [mdBook](https://rust-lang.github.io/mdBook/)

[dev-builds]: https://typst-community.github.io/dev-builds/ "Typst dev builds — Unofficial builds of Typst artifacts for development purposes."

## How do I install these tools?

Run the following:

```pwsh
scoop bucket add typst-community https://github.com/typst-community/scoop-bucket

scoop install typst-community/⟨tool-name⟩
# For example:
# scoop install typst-community/tinymist
```

> [!TIP]
>
> The [official Typst compiler](https://github.com/typst/typst/) is not included in this bucket. You can install it from the [Main bucket](https://github.com/ScoopInstaller/Main/) instead:
>
> ```pwsh
> scoop bucket add main
> scoop install main/typst
> ```

> [!NOTE]
>
> > Response status code does not indicate success: 403 (Forbidden).
> >
> > URL https://github.com/typst-community/REPO/releases/download/TAG/FILE.zip is not valid
>
> If you encounter the above error when installing an app, it is likely that Scoop has been blocked when detecting whether the repository is private.
>
> Most organizations on GitHub forbid access to REST API via a _fine-grained_ personal access tokens if the token’s lifetime is greater than _366 days_.
>
> **Solutions:**
>
> - Skip the detection by running `scoop config rm gh_token`.
>
>   You can run `scoop config gh_token` in advance to backup your token, then add it back later by running `scoop config gh_token ⟨token⟩`.
>
> - Adjust the lifetime of your existing token.
>
>   [Regeneration](https://github.com/settings/personal-access-tokens) is required for changing the expiration date.
>
> - Use a [classic](https://github.com/settings/tokens) token instead of a fine-grained token.
>
>   Most organizations do not forbid classic tokens.

## How do I contribute new manifests?

To make a new manifest contribution, please read the [Contributing
Guide](https://github.com/ScoopInstaller/.github/blob/main/.github/CONTRIBUTING.md)
and [App Manifests](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests)
wiki page.
