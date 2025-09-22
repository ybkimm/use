# use

A simple bash script that automatically finds and activates Nix development environments.

## Usage

Run `use` in any directory to activate the appropriate development environment.

The script searches upward from the current directory for:
1. `flake.nix` - Runs `nix develop` in that directory
2. `.use_env` - Reads environment name and uses predefined environment. If empty, uses the directory name.

## Setup

1. Add `use` to your PATH.
2. Create `flake.nix` in your project or `~/.local/use_environments/<environment_name>/flake.nix`.

## Environment Variables

- `USE_DEVELOP_ENV_DIR` - Directory for predefined environments (default: `~/.local/use_environments`)
- `USE_DEVELOP_SHELL` - Shell to use with nix develop

