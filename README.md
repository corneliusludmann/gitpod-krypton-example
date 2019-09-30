# Example Gitpod Workspace Image with Krypton

This repository shows an example Gitpod Docker image that has [Krypton](https://krypt.co/) installed.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/corneliusludmann/gitpod-krypton-example)


## How to use Krypton to sign GitHub commits

Krypton allows you to sign your GitHub commits with a GPG key. The private key for signing is stored securely on your phone and never leaves it.


### 1. Install the app on your phone

At first, you have to install the Krypton app on your phone:

<a href="https://appsto.re/us/weWofb.i" target="_blank">
    <img src="https://developer.apple.com/app-store/marketing/guidelines/images/badge-example-preferred.png">
</a>
<a href="https://play.google.com/store/apps/details?id=co.krypt.kryptonite" target="_blank">
    <img class="play-store" src="https://play.google.com/intl/en_us/badges/images/badge_new.png">
</a>


### 2. Pair your workspace

Then, pair your workspace with your phone. Open a terminal in Gitpod and run:
```console
$ kr pair
```
Resize the terminal window so that the whole QR code is shown. Scan the QR code with our Krypton app on your phone.

### 3. Enable code signing in your workspace
To enable code signing run the following in your terminal:
```console
$ kr codesign
```

### 4. Add GPG key to GitHub
The first time you use Krypton for GitHub code signing you have to go to https://github.com/settings/keys and add the GPG key printed by `kr codesign` to GitHub.

Test, that everything works:
```console
$ export GPG_TTY=$(tty); kr codesign test
```

### 5. Done

Next time you add a commit the GPG key is used to sign it. Since you added the GPG key to GitHub, your commit is marked as “verified.”

When you archive or delete your Gitpod workspace you could remove the paired computer from your Krypton app on your phone.

__Repeat the steps 2 and 3 for every new Gitpod workspace.__


## See also
- [Krypton Website](https://krypt.co/)
- [Krypton for Developers](https://krypt.co/developers/)
- [Krypton Documentation](https://krypt.co/docs/)
- [PGP Signing Git Commits with Krypton (Krypton Documentation)](https://krypt.co/docs/start/code-signing.html)
