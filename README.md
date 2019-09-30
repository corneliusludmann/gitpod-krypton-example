# Example Gitpod Workspace Image with Krypton

This repository shows an example Gitpod Docker image that has Krypton installed.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/corneliusludmann/gitpod-krypton-example)


## How to use Krypton to sign Github commits

First, pair your workspace with your phone:
```console
$ kr pair
```

Enable codesigning:
```console
$ kr codesign
```

Test, that everything works:
```console
$ export GPG_TTY=$(tty); kr codesign test
```


## See also
- [Krypton Website](https://krypt.co/)
- [Krypton for Developers](https://krypt.co/developers/)
- [Krypton Documentation](https://krypt.co/docs/)
- [PGP Signing Git Commits with Krypton (Krypton Documentation)](https://krypt.co/docs/start/code-signing.html)
