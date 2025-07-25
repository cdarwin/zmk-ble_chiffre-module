# BLe Chiffre ZMK Module

This repository contains the board files for the [BLe Chiffre](https://github.com/tominabox1/BLe-Chiffre) to allow users to build firmware. This can be done by adding the module to the west.yml found in your zmk-config's config directory. There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the akohekohe module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: zmk-ble_chiffre-module
      url-base: https://github.com/cdarwin
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk-ble_chiffre-module
      remote: cdarwin
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's board directory or in ZMK main.