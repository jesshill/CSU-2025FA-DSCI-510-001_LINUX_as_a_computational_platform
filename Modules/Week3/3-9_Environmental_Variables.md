# Environmental Variables 

### The Environment

Every shell session operates in the context of a larger **environment** or the general, system-wide context in which the shell is operating. For example, the user's name, the default terminal display, and the default language will all be aspects of the environment. Information about the environment is stored in the shell as **environmental variables**. We can examine the environment using the command `printenv`

```
$ printenv
```

For me, this spits out the following …

```
TERM_PROGRAM=Apple_Terminal
SHELL=/bin/bash
TERM=xterm-256color
HOMEBREW_REPOSITORY=/opt/homebrew
TMPDIR=/var/folders/5y/0vkm85c12s935r1qs0ls7_y80000gn/T/
TERM_PROGRAM_VERSION=455.1
TERM_SESSION_ID=F0CF53E9-C39B-44D0-84B5-530DA68BB5C4
USER=jessicahill
SSH_AUTH_SOCK=/private/tmp/com.apple.launchd.SztT4e4boM/Listeners
PATH=/opt/homebrew/bin:/opt/homebrew/sbin:/usr/local/bin:/System/Cryptexes/App/usr/bin:/usr/bin:/bin:/usr/sbin:/sbin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/local/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/appleinternal/bin:/Library/Apple/usr/bin
__CFBundleIdentifier=com.apple.Terminal
PWD=/Users/jessicahill
LANG=en_US.UTF-8
XPC_FLAGS=0x0
XPC_SERVICE_NAME=0
SHLVL=1
HOME=/Users/jessicahill
HOMEBREW_PREFIX=/opt/homebrew
LOGNAME=jessicahill
INFOPATH=/opt/homebrew/share/info:
HOMEBREW_CELLAR=/opt/homebrew/Cellar
_=/usr/bin/printenv
```
