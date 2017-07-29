# wekan-snap

[Wekan](https://wekan.github.io) server packaged as a snap for Ubuntu core. It consists of:
  - nodejs runtime
  - mongodb
  - wekan server implementation

## Screenshot

![Screenshot of Wekan][screenshot]

## Install and configure

This wekan snap is available in the Ubuntu store for release series 16 (e.g. Ubuntu 16.04). Search for wekan

 * Install snap package
   ```
   $ sudo snap install wekan
   ```
 * Review help
   ```
   $ snap run wekan.help
   ```
 * Configure snap package
   ```
   $ snap set wekan mail-url=smtp://127.0.0.1:25
   ...
   ```
 * Restart and check wekan
   ```
   $ systemctl restart snap.wekan.mongodb
   $ systemctl restart snap.wekan.wekan

   $ systemctl status snap.wekan.mongodb
   $ systemctl status snap.wekan.wekan
   ```

## Resources and facts:

 * At the moment only amd64 target is supported.
 * [URL settings](https://github.com/wekan/wekan-snap/wiki/Install) needs to be configured for Wekan to work correctly.
 * More documentation at the same [Wekan snap wiki](https://github.com/wekan/wekan-snap/wiki).
 * Wekan is also at: https://uappexplorer.com/snap/ubuntu/wekan 
 * [Wekan snap Documentation](https://github.com/wekan/wekan-snap/wiki)
 * [Wekan Documentation](https://github.com/wekan/wekan/wiki)

## Bug reports and feature requests

[Wekan snap package issues](https://github.com/wekan/wekan-snap/issues)

[Wekan issues](https://github.com/wekan/wekan/issues)

[screenshot]: https://wekan.github.io/screenshot.png


## Development


 * Fork this project at github if you do not have commit rights to the project
 * Install snapcraft
   ```
   sudo apt install snapcraft
   ```
 * As a regular user: download snap sources, improve the package and build and test package
   ```
   git clone git@github.com:scoopex/wekan-snap.git
   cd wekan-snap
   rm -f wekan_*.snap
   snapcraft
   snap install --dangerous wekan_*.snap
   ```
