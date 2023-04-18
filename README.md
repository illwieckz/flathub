# Unvanquished Tray Flatpak

![Unvanquished Tray](https://raw.githubusercontent.com/Unvanquished/unvanquished-tray-browser/main/package/icons/128x128/unvtray.png)

This repository provides the sources for building the Unvanquished Tray Flatpak package.

[Unvanquished Tray](https://github.com/Unvanquished/unvanquished-tray-browser) is a minimalistic [Unvanquished](https://unvanquished.net) server browser that runs in your system tray. The icon shows the player count of the most populated server. A left click on the icon connects to this server (on supported platforms) while a right click opens a server list in a context menu. Clicking on a server will launch the game and connect to it.

- Unvanquished Tray repository: https://github.com/Unvanquished/unvanquished-tray-browser
- Unvanquished website: https://unvanquished.net
- Unvanquished forums: https://forums.unvanquished.net
- Unvanquished wiki: https://wiki.unvanquished.net


## Building and running the Flatpak

```sh
flatpak remote-add --user --if-not-exists \
	flathub https://flathub.org/repo/flathub.flatpakrepo
```

```sh
flatpak-builder --install --install-deps-from=flathub \
	--user --force-clean \
	.build-dir net.unvanquished.unvtray.yml
```


## Running the Flatpak

Running Unvanquished Tray:

```sh
flatpak run net.unvanquished.unvtray
```
