# Configuration reference

Custom plugin gitlinks live under pack/plugins/start/. The parent repository records exact commits; each plugin retains its own history. Initialize submodules before launching a source checkout.

The [flake](../flake.nix) exports homeManagerModules.default and packages for its declared systems. Import that module into an existing Home Manager configuration and set programs.nvimconf.enable = true. Read the options in the flake for package, extraConfig, theme and themeMode.

The Home Manager module's default theme differs from the source checkout's config.toml. themeMode overrides theme when set. Those module choices are configuration policy, not a claim that every theme variant or host has been tested.

Third-party editor plugins are declared in the separate [nixos-config repository](https://github.com/olegpustovit/nixos-config), currently under home/default.nix. A Home Manager module import alone is not proof that every external executable or plugin required by a language configuration is present.

The public Nix integration was not installed for the capture. Keep the existing lockfile and gitlinks unless intentionally performing a separately verified plugin update. Do not use make sync for a documentation change or a scoped commit.
