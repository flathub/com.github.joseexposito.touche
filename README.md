# Touché Flathub Repo

[This repository](https://github.com/flathub/com.github.joseexposito.touche) contain the required
files to publish [Touché](https://github.com/JoseExposito/touche) on
[Flathub](https://flathub.org/apps/details/com.github.joseexposito.touche).

## How to publish a new release

### Touché repository:

- Update the version number in `meson.build`, `package.json` and `rpm/touche.spec`.
- Update the changelog in `data/app.appdata.xml.in.in`, `debian/changelog` and `rpm/touche.spec`.
- Create a tag to trigger the release GitHub workflow:
```bash
$ git tag X.Y.X && git push && git push --tags
```
- Wait until the draft release gets created, add a description and publish it.

### This repository:

- Create a branch to perform the changes:
```bash
$ git switch -c vX.Y.X
```
- Download the `ARCHIVE-SHA256SUM` file from the Touché release, copy the SHA-256 sum and paste it in `com.github.joseexposito.touche.yml`.
- Update the archive URL in `com.github.joseexposito.touche.yml`: `https://github.com/JoseExposito/touche/releases/download/X.Y.Z/archive.tar.gz`.
- Commit, push and create a pull request on [GitHub](https://github.com/flathub/com.github.joseexposito.touche).

## Useful links:

https://github.com/flathub/flathub/wiki/App-Maintenance

