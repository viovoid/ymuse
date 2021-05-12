In this repository I have made some interface tweaks so that the window fits reasonably on a PinePhone screen. Tested in Mobian Phosh, at 200% scaling, with `scale-to-fit ymuse on`. Essentially, playlist functionality has been removed (with all of its buttons), and double click-events fire from a single click, to avoid the need to use the PinePhone keyboard (right-click functionality has also been removed).

Also, Album Artist is used over Artist for grouping/sorting purposes, as a matter of preference :)

The original readme is retained below:


[![Latest release](https://img.shields.io/github/v/release/yktoo/ymuse.svg)](https://github.com/yktoo/ymuse/releases/latest)
[![Releases](https://img.shields.io/github/downloads/yktoo/ymuse/total.svg)](https://github.com/yktoo/ymuse/releases)
[![License](https://img.shields.io/github/license/yktoo/ymuse.svg)](COPYING)
[![Build Status](https://travis-ci.org/yktoo/ymuse.svg?branch=master)](https://travis-ci.org/yktoo/ymuse)
[![Go Report Card](https://goreportcard.com/badge/github.com/yktoo/ymuse)](https://goreportcard.com/report/github.com/yktoo/ymuse)

# ![Ymuse icon](resources/icons/hicolor/32x32/apps/ymuse.png) Ymuse

**Ymuse** is an easy, functional, and snappy GTK front-end (client) for [Music Player Daemon](https://www.musicpd.org/) written in Go.

[![Ymuse screenshot](https://res.cloudinary.com/yktoo/image/upload/blog/vx7vpdn1lrskop110ts6.png)](https://res.cloudinary.com/yktoo/image/upload/blog/vx7vpdn1lrskop110ts6.png)

It supports library browsing and search, playlists, streams etc.

[![Ymuse screenshot](https://res.cloudinary.com/yktoo/image/upload/t_s320/blog/tyje15w0q4m48tf1d2wz.png)](https://res.cloudinary.com/yktoo/image/upload/blog/tyje15w0q4m48tf1d2wz.png)
[![Ymuse screenshot](https://res.cloudinary.com/yktoo/image/upload/t_s320/blog/xpqgooxdhya2ij0hgfka.png)](https://res.cloudinary.com/yktoo/image/upload/blog/xpqgooxdhya2ij0hgfka.png)

Have a look at the [Feature Tour video](https://youtu.be/FuO7QWOaS1A) for more details.

## Installing

You can:

* If your distribution supports [snap packages](https://snapcraft.io/ymuse): `sudo snap install ymuse`
* Otherwise, you can use a binary package from the [Releases](https://github.com/yktoo/ymuse/releases) section.

## Building from source

### Requirements

* Go 1.15+

### Getting started

1. [Install Go](https://golang.org/doc/install)
2. Make sure you have the following dependencies installed:
   * `libc6`
   * `libgtk-3-0`
3. Clone the source and compile:
```bash
git clone https://github.com/yktoo/ymuse.git
cd ymuse
go generate
go build
```
4. Copy over the icons and localisations:
```bash
sudo cp -r resources/icons/* /usr/share/icons/
sudo cp -r resources/i18n/generated/* /usr/share/locale/
sudo update-icon-caches /usr/share/icons/hicolor/*
```

This will create the application executable `ymuse` in the project root directory, which you can run straight away.

## License

See [COPYING](COPYING).

## Credits

* [gotk3](https://github.com/gotk3/gotk3)
* [gompd](https://github.com/fhs/gompd) by Fazlul Shahriar
* [go-logging](https://github.com/op/go-logging) by Örjan Fors
* [goreleaser](https://goreleaser.com/) by Carlos Alexandro Becker et al.

## TODO

* Automated UI testing.
* Drag’n’drop in the play queue.
* More settings.
* Multiple MPD connections support.
