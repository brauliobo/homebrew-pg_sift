# pg_sift Homebrew tap

This compatibility tap builds the source repository's `main` branch for Homebrew PostgreSQL 17 and 18. Existing install commands continue to work:

```sh
brew tap brauliobo/pg_sift
brew install --HEAD brauliobo/pg_sift/pg_sift
brew test brauliobo/pg_sift/pg_sift
```

The maintained formula now lives in the [source repository](https://github.com/brauliobo/pg_sift/tree/main/Formula). Point an existing tap there with:

```sh
brew tap --custom-remote brauliobo/pg_sift https://github.com/brauliobo/pg_sift.git
```

For a new installation, use `brew tap brauliobo/pg_sift https://github.com/brauliobo/pg_sift.git` before installing.

The formula builds both PostgreSQL versions and installs through Homebrew's versioned extension directories. Enable it in a database with `CREATE EXTENSION pg_sift;`.

Uninstall with `brew uninstall pg_sift` and `brew untap brauliobo/pg_sift`. PostgreSQL installations and databases are managed separately.
