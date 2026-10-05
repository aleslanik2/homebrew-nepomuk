# Homebrew tap for nepomuk

[nepomuk](https://github.com/aleslanik2/nepomuk) is a post-quantum secrets vault that lives in a single file in git.

```bash
brew install aleslanik2/nepomuk/nepomuk          # the command line tool
brew install --cask aleslanik2/nepomuk/nepomuk-gui   # the desktop app (macOS)
```

Update with `brew upgrade nepomuk` and `brew upgrade --cask nepomuk-gui`, not with `nepomuk upgrade`.

## Where the hashes come from

The formula and the cask install the release binaries from GitHub. Their SHA-256 hashes are written by [`scripts/update-homebrew.sh`](https://github.com/aleslanik2/nepomuk/blob/main/scripts/update-homebrew.sh) in the nepomuk repository, only from a `SHA256SUMS` whose release signature verifies against the release key `SHA256:ZAaNBE10XNmiLIFzzdid/hBqmzlhfwf1grn5Qb0X9XA`. Nothing here bumps versions automatically.

The desktop app is not notarized yet. The cask removes the quarantine flag after Homebrew has checked the download against that hash, as nepomuk's own `install.sh` does.
