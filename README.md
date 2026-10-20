# pg_sift Homebrew tap

Install on macOS with Homebrew PostgreSQL 17 and 18:

```sh
brew tap brauliobo/pg_sift
brew install --HEAD brauliobo/pg_sift/pg_sift
brew test brauliobo/pg_sift/pg_sift
```

The formula builds both PostgreSQL versions and installs through Homebrew's versioned extension directories. Enable it in a database with `CREATE EXTENSION pg_sift;`.

The v3.1.0 source release does not build on Apple Silicon: its bitmap dispatcher calls x86 CPU detection unconditionally. Until a release includes the macOS portability changes, HEAD uses the `feat/homebrew` branch of pg_sift. After that PR is merged, HEAD will track `main`.

Uninstall with `brew uninstall pg_sift` and `brew untap brauliobo/pg_sift`. PostgreSQL installations and databases are managed separately.
