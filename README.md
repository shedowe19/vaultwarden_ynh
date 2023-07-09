<!--
N.B.: This README was automatically generated by https://github.com/YunoHost/apps/tree/master/tools/README-generator
It shall NOT be edited by hand.
-->

# Vaultwarden for YunoHost

[![Integration level](https://dash.yunohost.org/integration/vaultwarden.svg)](https://dash.yunohost.org/appci/app/vaultwarden) ![Working status](https://ci-apps.yunohost.org/ci/badges/vaultwarden.status.svg) ![Maintenance status](https://ci-apps.yunohost.org/ci/badges/vaultwarden.maintain.svg)

[![Install Vaultwarden with YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=vaultwarden)

*[Lire ce readme en français.](./README_fr.md)*

> *This package allows you to install Vaultwarden quickly and simply on a YunoHost server.
If you don't have YunoHost, please consult [the guide](https://yunohost.org/#/install) to learn how to install it.*

## Overview

Alternative implementation of the Bitwarden server API written in Rust and compatible with upstream Bitwarden clients*, perfect for self-hosted deployment where running the official resource-heavy service might not be ideal.

**Shipped version:** 1.28.1~ynh2

**Demo:** https://vault.bitwarden.com/#/register

## Screenshots

![Screenshot of Vaultwarden](./doc/screenshots/screenshot1.png)

## Disclaimers / important information

### Install

This package compile Vaultwarden from sources, that can take a long time on a small computer :

* When installing on a Raspberry Pi 3, this can take more than 1 hour.
* When installing from the webadmin, you can encounter the "504 Gateway Timeout": this is fine, just let it finish in the background.

### Migrate from Bitwarden

This package handle the migration from Bitwarden to Vaultwarden.
For that, you will have to upgrade your Bitwarden application with this repository.
This can only be done from the command-line interface - e.g. through SSH.
Once you're connected, you simply have to execute the following:

```bash
sudo yunohost app upgrade bitwarden -u https://github.com/YunoHost-Apps/vaultwarden_ynh --debug
```

The `--debug` option will let you see the full output. If you encounter any issue, please paste it.

## Documentation and resources

* Official user documentation: <https://help.bitwarden.com/>
* Official admin documentation: <https://github.com/dani-garcia/vaultwarden/wiki>
* Upstream app code repository: <https://github.com/dani-garcia/vaultwarden>
* YunoHost documentation for this app: <https://yunohost.org/app_vaultwarden>
* Report a bug: <https://github.com/YunoHost-Apps/vaultwarden_ynh/issues>

## Developer info

Please send your pull request to the [testing branch](https://github.com/YunoHost-Apps/vaultwarden_ynh/tree/testing).

To try the testing branch, please proceed like that.

``` bash
sudo yunohost app install https://github.com/YunoHost-Apps/vaultwarden_ynh/tree/testing --debug
or
sudo yunohost app upgrade vaultwarden -u https://github.com/YunoHost-Apps/vaultwarden_ynh/tree/testing --debug
```

**More info regarding app packaging:** <https://yunohost.org/packaging_apps>
