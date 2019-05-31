# direnv - Snap

[direnv](https://direnv.net/) is an environment switcher for the shell. It knows how to hook into bash, zsh, tcsh, fish shell and elvish to load or unload environment variables depending on the current directory. This allows project-specific environment variables without cluttering the ~/.profile file.

This repository contains the code for the _direnv_ *snap* package.

**NOTE:**
  It works on Ubuntu, Fedora, Debian, and other major Linux distributions.

## Prerequisites

 Prerequisites include a linux installation and the snapd service. In order to install snapd please follow the [Install snapd](https://docs.snapcraft.io/core/install) guide.

## Installation

In order to install the direnv snap use the 'snap' cli i.e :

```
sudo snap instal 
```

## Setup

For direnv to work properly it needs to be hooked into the shell. Each shell has its own extension mechanism:

### BASH
Add the following line at the end of the _~/.bashrc_ file:

```eval "$(direnv hook bash)"```

Make sure it appears even after rvm, git-prompt and other shell extensions that manipulate the prompt.

### ZSH

Add the following line at the end of the _~/.zshrc_ file:

``` eval "$(direnv hook zsh)"```

### FISH

Add the following line at the end of the _~/.config/fish/config.fish file_:

```eval (direnv hook fish)```

### TCSH
Add the following line at the end of the _~/.cshrc_ file:

```eval `direnv hook tcsh```

### Elvish (0.12+)

Run:

``` $> direnv hook elvish > ~/.elvish/lib/direnv.elv```

and add the following line to your _~/.elvish/rc.elv_ file:

```
use direnv
l direnv
```

## Build

Checkout the source code and from inside the snap directory execute the following command :

```
snapcraft
```


## Contributing

 See the [contribution guidelines](CONTRIBUTING.md).

## License
```
MIT License

Copyright (c) 2018-2019 Ioannis Polyzos

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
