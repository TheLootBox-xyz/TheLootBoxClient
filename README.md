# TheLootBoxWallet

TheLootBoxWallet is an Ethereum wallet that runs locally on your desktop with a focus on privacy and security. A lockbox for your ethereum assets powered by Toga and coffee .

---

### Features

- Account wallet credentials are stored encrypted and decrypted only when the client is in use and unlocked by the account key.

- Create multiple accounts.

- Send Ether. 

- Auto sign and send transactions locally from trusted sources

- Lookup other addresses if multiple were created.

- Runs locally as a self-contained stand-alone application.

- Soon to be cross-platform.

---

### Install from .deb file release

#### Steps to install

- Download the deb file from the latest release.

https://github.com/TheLootBox-xyz/TheLootBoxWallet/releases

- Run the install command.

`sudo dpkg -i thelootboxwallet-release`

- Start thelootboxwallet from `/usr/bin/TheLootBoxWallet` or from TheLootBoxWallet app shortcut via the Show Applications menu.

---

### Setup from source

Dependencies for Ubuntu 20.04.

`sudo apt install build-essential git pkg-config python3-dev python3-venv libgirepository1.0-dev libcairo2-dev gir1.2-webkit2-4.0 libcanberra-gtk3-module`

I highly recommended creating a virtual environment to avoid dependency conflicts.

`python3 -m venv envname`

Once the venv is created source it in order to install the dependencies to that environment.

`source path/to/envname/bin/activate`

Install briefcase and required dependencies.

`pip install briefcase Flask web3 cyptography Flask-WTF toga`

Start app in Dev mode.

`briefcase dev`

Build and run the app.

`briefcase run`

---

### Customize default settings

You can customize the default network and ethereum account with a `config.ini` file. If you don't have a `config.ini` file TheLootBoxWallet will use the first public address created as the default address.

Example `config.ini` file:

```bash
[DEFAULT]

network = https://goerli-rollup.arbitrum.io/rpc
default_address = your_public_ethereum_address
ens_mainnet_node = your_mainnet_node_url
logs = False
```

### Preview screenshot

![TheLootBoxClient](src/TheLootBoxWallet/code/static/images/TheLootBoxWallet.png)

### Supporting development

https://www.buymeacoffee.com/thelootbox

