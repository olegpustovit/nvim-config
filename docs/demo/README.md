# Local capture

Captured on 23 October 2026 from base revision `6cf3dada5eab831518da5cb8b499589e272b72e9` with the documented fixes and examples in this commit.

Neovim 0.12.4 on Linux ARM64. The source checkout used its exact three gitlinks; no plugin revision or flake input was updated. XDG config/data/state/cache directories were isolated under /tmp. The actual startup loaded catppuccin_latte, mouse=a and the ThemePicker command. The terminal opened the included synthetic Lua buffer. editor.ansi and screen.txt accompany the PNG; Chromium replayed actual PTY output through xterm, rather than drawing a mock editor. LSP attachment, formatting, completion, Workbench enablement, Nix installation and performance gates were not tested.

Commands from the repository root after installing its documented dependencies:

```sh
git -c url.https://github.com/.insteadOf=git@github.com: submodule update --init --recursive
# Start through the isolated XDG command in the root README.
```
