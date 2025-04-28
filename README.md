# Dotfiles

A collection of my personal configuration files managed with [GNU Stow](https://www.gnu.org/software/stow/).

## Prerequisites

- **GNU Stow**: Ensure you have Stow installed. You can install it using your package manager:

  ```bash
  # On Fedora
  sudo dnf install stow

  # On Debian/Ubuntu
  sudo apt-get install stow

  # On macOS using Homebrew
  brew install stow
  ```

## Installation

1. **Clone the Repository**

    Clone your dotfiles repository to your home directory:

    ```bash
    git clone https://github.com/kalidyasin/dotfiles.git ~/.dotfiles
    ```

2. **Navigate to the Dotfiles Directory**

    ```bash
    cd ~/.dotfiles
    ```

3. **Use Stow to Symlink Your Dotfiles**

    Run Stow to create symbolic links for all your configurations:

    ```bash
    stow .
    ```

## Adding New Dotfiles

1. **Create a New Configuration Directory**

    Inside your `~/.dotfiles` directory, create a new folder for your configuration. For example, for `tmux`:

    ```bash
    mkdir tmux
    ```

2. **Add Your Configuration Files**

    Add your `.tmux.conf` file to the `tmux` directory:

    ```
    ~/.dotfiles/tmux/.tmux.conf
    ```

3. **Symlink Using Stow**

    ```bash
    stow tmux
    ```

## Removing Dotfiles

To remove the symlinks created by Stow:

```bash
stow -D package_name
```

Replace `package_name` with the name of the configuration directory you want to remove. For example:

```bash
stow -D vim
```

## Updating Dotfiles

After making changes to your configuration files, you can update the symlinks by running Stow again:

```bash
stow -R package_name
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
