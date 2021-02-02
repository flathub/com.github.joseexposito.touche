# Touché Flathub Repo

[This repository](https://github.com/flathub/com.github.joseexposito.touche) contain the required
files to publish [Touché](https://github.com/JoseExposito/touche) on
[Flathub](https://flathub.org/apps/details/com.github.joseexposito.touche).

## How to publish a new release

### Touché repository:

- Update the version number in `meson.build` and `package.json`
- Update the changelog in `data/gnome.appdata.xml.in.in`, `data/elementary.appdata.xml.in.in` and `debian/changelog`.
- Generate the Flatpak archive:
```bash
$ npm run flatpak:archive
```
- Copy the printed SHA-256 and paste it in `com.github.joseexposito.touche.yml`
- Update the archive URL: `https://github.com/JoseExposito/touche/releases/download/X.Y.Z/flatpak-archive.tar.gz`
- Commit and push changes
- Generate a new release on [GitHub](https://github.com/JoseExposito/touche/releases/new) and add
`../flatpak-archive.tar.gz` as attachment

### This repository:

- Replicate the changes to `com.github.joseexposito.touche.yml` here
- Commit and push changes

## Useful links:

https://github.com/flathub/flathub/wiki/App-Maintenance