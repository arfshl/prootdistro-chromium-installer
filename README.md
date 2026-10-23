### About

This project is a fork from [mrclksr/linux-browser-installer](https://github.com/mrclksr/linux-browser-installer)

`prootdistro-chromium-installer` is bash script to install chromium-based web browser on proot-distro, and patch their desktop launcher, this tool only supports Debian, Ubuntu, Fedora, RHEL-based and OpenSUSE

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
curl -fsSLO https://raw.githubusercontent.com/arfshl/prootdistro-chromium-installer/refs/heads/main/chromium-installer-apt

chmod +x chromium-installer-apt

# For Fedora
curl -fsSLO https://raw.githubusercontent.com/arfshl/prootdistro-chromium-installer/refs/heads/main/chromium-installer-dnf

chmod +x chromium-installer-dnf

# For OpenSUSE
curl -fsSLO https://raw.githubusercontent.com/arfshl/prootdistro-chromium-installer/refs/heads/main/chromium-installer-zypper

chmod +x chromium-installer-zypper
````

Proceed as user root or sudo with the following steps.

#### Install browser

````
./chromium-installer-apt install <browser>
./chromium-installer-dnf install <browser>
./chromium-installer-zypper install <browser>
````

You'll will found the patched desktop launcher with `(proot launcher)` prefix, for example `Google Chrome (proot launcher)` located on `/usr/local/share/applications/` with filename `<browser>-proot.desktop`

#### Uninstall browser

````
./chromium-installer-apt install <browser>
./chromium-installer-dnf install <browser>
./chromium-installer-zypper uninstall <browser>
````

This command uninstall the browser, and removes its desktop file on `/usr/local/share/applications/<browser>-proot.desktop`
