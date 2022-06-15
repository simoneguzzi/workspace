# Infrastructure

## Setup Windows workspace using Chocolatey

1. Install Chocolatey following [instructions](https://chocolatey.org/install#individual).
2. Run

   ```bash
   choco install path/to/chocolatey/essentials.config -y
   ```

## Setup Windows workspace using Scoop

1. Install Scoop following [instructions](https://github.com/ScoopInstaller/Install#installation).
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
