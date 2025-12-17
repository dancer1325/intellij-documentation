[//]: # (Source: https://www.jetbrains.com/help/idea/set-up-GPG-commit-signing.html)
[//]: # (Downloaded: 2025-12-17 20:00:13)

## Configure the environment

### Set up GPG support

  * Do one of the following:

    * Download and install the latest [GitForWindows](https://gitforwindows.org) version (you'll need version 2.19.2 or later). Pre-configured GPG is part of the package.

To verify everything is set up correctly, open GitBash, run the `gpgconf` command and make sure the output is like the following:

gpg:OpenGPG:/usr/bin/gpg gpg-agent:Private Keys:/usr/bin/gpg-agent scdaemon:Smartcards:/usr/lib/gnupg/scdaemon gpgsm:S/MIME:/usr/bin/gpgsm dirmngr:Network:/usr/bin/dirmngr pinentry:Passphrase Entry:/usr/bin/pinentry 

Make sure the pinentry shows a GUI prompt by running the `echo GETPIN | pinentry` command.

    * Download and install the [Gpg4Win](https://www.gpg4win.org) package and make sure that `git config gpg.program` points to the `gpg.exe` file from the package by doing the following:

      1. Run `where.exe gpg`.

      2. If the output returns several executables, locate the one from Gpg4Win (by default, the path is C:\Program Files (x86)\GnuPG\bin\gpg.exe.

      3. Run `git config --global gpg.program "path/to/gpg/from/Gpg4Win"`.




### Set up GPG support

  * Do one of the following:

    * Download and install [GPGTools](https://gpgtools.org). Pre-configured GPG is part of the package.

Make sure that `git config gpg.program` points to the gpg file from the package (by default, the path is /usr/local/MacGPG2/bin/gpg).

    * Download and open [Homebrew](https://brew.sh) and run the following command: `brew install gnupg pinentry-mac`.

To verify everything is set up correctly, open Terminal, run the `gpgconf` command and make sure the output is like the following:

pg:OpenGPG:/usr/local/MacGPG2/bin/gpg gpg-agent:Private Keys:/usr/local/MacGPG2/bin/gpg-agent scdaemon:Smartcards:/usr/local/MacGPG2/libexec/scdaemon gpgsm:S/MIME:/usr/local/MacGPG2/bin/gpgsm dirmngr:Network:/usr/local/MacGPG2/bin/dirmngr pinentry:Passphrase Entry:/usr/local/bin/pinentry 

Make sure the pinentry shows a GUI prompt by running the `echo GETPIN | pinentry-mac` command.




### Set up GPG support

  1. Install `gpg2` using a package manager that comes with your Linux distribution. The exact list of package will vary based on the distributive you are using, the most important being gnupg2, gnupg-agent, and a pinentry that shows a GUI prompt.

For example, on Ubuntu/Debian, run `sudo apt -y install gnupg2 gnupg-agent pinentry-gnome3`.

  2. To verify everything is set up correctly, open the Terminal, run the `gpgconf` command and make sure the output is like the following:

gpg:OpenPGP:/usr/bin/gpg gpg-agent:Private Keys:/usr/bin/gpg-agent scdaemon:Smartcards:/usr/lib/gnupg/scdaemon gpgsm:S/MIME:/usr/bin/gpgsm dirmngr:Network:/usr/bin/dirmngr pinentry:Passphrase Entry:/usr/bin/pinentry 

Make sure that the pinentry shows a GUI prompt using the `echo GETPIN | pinentry` command.



