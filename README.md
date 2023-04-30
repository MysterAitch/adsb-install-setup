## ADSB Installation Helper

This repository is a personal helper to make installation simpler and repeatable.

While others might find it useful, it is not intended for general use.
Perhaps you might find it useful as a reference, or to fork.

### Usage

1. Set-up your operating system
    1. Typically Raspbian Lite on a Raspberry Pi
        - Follow normal installation instructions for your OS
        - (e.g., setting up wifi, `sudo raspi-config`, sharing of SSH keys, etc)
    2. Update OS
        - ```shell
          sudo apt-get update
          sudo apt-get upgrade
          ```
    3. Install core pre-requisites
        - ```shell
          sudo apt-get update
          sudo apt-get install git
          ```
    4. TODO - Specific notes regarding:
        - Monitoring agents (Zabbix)
        - Security (fail2ban, ufw, etc)
        - HTTPS / Let's Encrypt (certbot) - though, likely a step for later, after the webserver is installed
        - VPN (Wireguard) to enable remote access
        - Remote access (SSH, VNC, etc)
2. Install optional pre-requisites
    - ```shell
      sudo apt-get update
      sudo apt-get install htop
      ```
4. Clone this repository to a staging area within your home directory
    - ```shell
      ## We will be cloning various repositories here, to avoid using curl/wget
      mkdir -p ~/.adsb-install
      cd ~/.adsb-install

      ## Note that SSH is typically preferred, but HTTPS can be used here for simplicity.
      git@github.com:MysterAitch/adsb-install-setup.git
      git clone https://github.com/MysterAitch/adsb-install-setup.git
      ```

