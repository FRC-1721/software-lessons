# software-lessons

A collection of generic instructions, slideshows and notes, for use onboarding new software team members!


# Dependencies

## Ubuntu

```sh
sudo apt install texlive-latex-recommended texlive-latex-extra texlive-pictures pandoc rename
```

## Arch

```sh
sudo pacman -S base-devel pandoc
```

# Getting started making a new pres

First clone this repo

## With ssh:

```sh
git clone git@github.com:FRC-1721/software-lessons.git
```

## With https:

```sh
git clone https://github.com/FRC-1721/software-lessons.git
```

## Build the docs

CD into the docs directory

```sh
cd docs
make
```

## Make your own

Copy the example slides

```sh
cp presentations/Example_Presentation.md presentations/My_Presentation.md
```

Edit `presentations/My_Presentation.md`, and when you're done, invke make to build the presentations into PDFs!

```sh
make
```

NOTE: For arch users, `rename` is different than on ubuntu, so `make` may error, this is nonfatal though, you can still find the PDF output in `_build/pdf/`
