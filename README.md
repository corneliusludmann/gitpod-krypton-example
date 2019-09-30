# Example Gitpod Workspace Image with Krypton

This repository shows an example Gitpod Docker image that has Krypton installed.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/corneliusludmann/gitpod-krypton-example)


## How to use Krypton to sign GitHub commits

Krypton allows you to sign your GitHub commits with a GPG key. The private key for signing is stored securely on your phone and never leaves it. First, install the app on your phone. Then, pair your workspace with your phone:
```console
$ kr pair
```

To enable codesigning run:
```console
$ kr codesign
```

The first time you use Krypton for GitHub code signing you have to go to `https://github.com/settings/keys` and and the GPG key printed by `kr codesign` to GitHub.

Test, that everything works:
```console
$ export GPG_TTY=$(tty); kr codesign test
```


## See also
- [Krypton Website](https://krypt.co/)
- [Krypton for Developers](https://krypt.co/developers/)
- [Krypton Documentation](https://krypt.co/docs/)
- [PGP Signing Git Commits with Krypton (Krypton Documentation)](https://krypt.co/docs/start/code-signing.html)
