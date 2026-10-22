### About

This project is a fork from [mrclksr/linux-browser-installer](https://github.com/mrclksr/linux-browser-installer)

`prootdistro-chromium-installer` is bash script to install chromium-based web browser on proot-distro, and patch their desktop launcher

```
brave - Brave Browser
braveorigin - Brave Origin
chrome - Google Chrome
vivaldi - Vivaldi Browser
```

### Usage

Download the scripts

````
# For Debian/Ubuntu
$ curl -fsSLO https://raw.githubusercontent.com/arfshl/prootdistro-chromium-installer/refs/heads/main/chromium-installer-apt
````

Proceed as user root or sudo with the following steps.

#### Install browser

````
# ./chromium-installer-apt install <browser>
````

You'll will found the patched desktop launcher with `(proot launcher)` prefix, for example `Google Chrome (proot launcher)` located on `/usr/local/share/applications/` with filename `<browser>-proot.desktop`

#### Uninstall browser

````
# ./chromium-installer-apt uninstall <browser>
````

This command uninstall the browser, and removes its desktop file on `/usr/local/share/applications/<browser>-proot.desktop`