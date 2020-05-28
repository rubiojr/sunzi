## 2.1, release 2018-01-15
* Dotfiles (files that start with '.') in recipes, roles and files are now included.
* `sunzi.yml` is now evaluated as ERB to access environment variables. (e.g. `<%= ENV['MY_PASSWORD'] %>`)

## 2.0, release 2018-01-14
* Plug-in support for commands.
* Separate `setup` and `teardown` commands for VPS into the `sunzi-vps` gem as a plugin.
* "attributes" are now "vars" in sunzi.yml and shell scripts.
* ERB templating (e.g. <%= @vars.environment %>) is always enabled.
* Individual attribute files compiled/attributes/* are no longer supported. Use ERB template methods instead.

## 1.5, release 2013-09-27
* `sunzi deploy [linode|digital_ocean] [name]` will deploy to the instance with additional attributes.

## 1.4, release 2013-09-27
* `sunzi teardown` no longer requires instance names as an argument, it lets you choose from a list instead.

## Past Releases
* v1.3: SSH config support. Thanks to @toooooooby
* v1.2: Evaluate everything as ERB templates by default. Added "files" folder.
* v1.1: "set -e" by default. apt-get everywhere in place of aptitude. Linode DNS support for DigitalOcean instances.
* v1.0: System functions are refactored into sunzi.mute() and sunzi.install().
* v0.9: Support for [DigitalOcean](https://www.digitalocean.com) setup / teardown.
* v0.8: Added `--sudo` option to `sunzi deploy`.
* v0.7: Added `erase_remote_folder` and `cache_remote_recipes` preferences for customized behavior.
* v0.6: System function sunzi::silencer() added for succinct log messages.
* v0.5: Role-based configuration supported. Reworked directory structure. **Incompatible with previous versions**.
