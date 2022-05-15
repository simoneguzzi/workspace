# Infrastructure

## Setup Windows workspace using Chocolatey

1. Install Chocolatey following [instructions](https://chocolatey.org/install#individual).
2. Run

   ```bash
   choco install path/to/chocolatey/essentials.config -y
   ```

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
