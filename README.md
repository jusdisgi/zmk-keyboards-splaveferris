# SplaveFerris ZMK Module

This repository contains the shield files for the [SplaveFerris](https://github.com/jusdisgi/SplaveFerris) to allow users to build firmware. This can be done by adding the module to the west.yml found in your zmk-config's config directory. There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the splaveferris module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: petejoganson
      url-base: https://github.com/petejohanson
    - name: jusdisgi
      url-base: https://github.com/jusdisgi
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: ec-support-zmk-module
      remote: petejohanson
      revision: main
    - name: zmk-keyboards-splaveferris
      remote: jusdisgi
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's shield directory or in ZMK main.
