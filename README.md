# Git LFS mirror of `ftp.ports.debian.org`

This git repository contains a mirror of
[ftp.ports.debian.org](https://ftp.ports.debian.org/), with external
objects stored using [Git LFS](https://git-lfs.com/).

This repository was created using rsync from [the `ftp.de.debian.org`
mirror of ftp.ports.debian.org](https://www.ports.debian.org/mirrors)
on 2024-05-05.  The goal is to keep it in sync with
`ftp.ports.debian.org` going forward.

## Cloning

The Git LFS objects are not available via GitLab, therefor to clone
this repository successfully you will need to disable Git LFS smudging
using the `GIT_LFS_SKIP_SMUDGE=1` environment variable like this:

```
GIT_LFS_SKIP_SMUDGE=1 git clone https://gitlab.com/debdistutils/archives/debian/ftp.ports.debian.org.git
```

# Signature Verification

Commits are signed using [my PGP
key](https://blog.josefsson.org/2019/03/21/openpgp-2019-key-transition-statement/)
with fingerprint:

```
pub   ed25519 2019-03-20 [SC]
      B1D2 BD13 75BE CB78 4CF4  F8C4 D73C F638 C53C 06BE
```

You may view git log and verify commit signatures them as follows:

```
git log --show-signature
```

To verify a single commit use something like this:

```
$ git verify-commit a0525d83117bfe0ac09e49f740fcf0389e9134df
gpg: Signature made Sun May  5 17:45:34 2024 CEST
gpg:                using EDDSA key A3CC9C870B9D310ABAD4CF2F51722B08FE4745A2
gpg: Good signature from "Simon Josefsson <simon@josefsson.org>" [ultimate]
$ 
```

## Contact

The maintainer is [Simon Josefsson](https://blog.josefsson.org/).
