# Infrastructure

## Setup Windows workspace using Chocolatey

1. Install Chocolatey following
   [instructions](https://chocolatey.org/install#individual).
2. Run

   ```bash
   choco install path/to/chocolatey/essentials.config -y
   ```

## Setup Windows workspace using Scoop

1. Install Scoop following
   [instructions](https://github.com/ScoopInstaller/Install#installation).
2. Run

   ```bash
   scoop install git
   gc buckets.txt |% { scoop bucket add $_ }
   gc essentials.txt |% { scoop install $_ }
   ```

Search for apps on <https://scoop.sh>.

## Setup Mac workspace using Brew

1. Install Brew by running

   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. Run

   ```bash
   xargs brew install < path/to/brew/essentials.txt
   xargs brew install --cask < path/to/brew/essentials_cask.txt
   ```

## Setup VS Code

### Add the `code` command to the path

1. Launch VS Code.
2. Open the Command Palette - `Cmd + Shift + P`.
3. Type `shell command` to find the Shell Command **Install 'code' command in
   PATH command**.
4. Restart the terminal for the new `$PATH` value to take effect.

### Backup extensions

1. If you haven't done it yet, add the `code` command to the path.
2. Run `code --list-extensions > vscode_extensions.txt`.

### Install extensions

1. If you haven't done it yet, add the `code` command to the path.
2. Run `cat vscode_extensions.txt | xargs -L 1 code --install-extension`.
