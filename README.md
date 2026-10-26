# iRev Vaultwarden browser extension

A browser extension for iRevolution Group's self-hosted [Vaultwarden](https://github.com/dani-garcia/vaultwarden) server. It is a stripped-down fork of the Bitwarden browser client, fixed to one server so that upstream release changes cannot break it.

- **Fixed server:** `https://vaultwarden.sunderland.irevolution.group`. The server selector is removed and stored server settings are ignored.
- **Removed:** the desktop, CLI and web apps, Bitwarden's non-GPL commercial code (`bitwarden_license`), the phishing blocklist that downloaded data from Bitwarden's servers, promo pages, and non-English locales.
- **Rebranded:** names, icons and logos are placeholders for "iRev Vaultwarden".

## Building

Requires Node 24 (see `.nvmrc`).

```bash
npm install --ignore-scripts
cd apps/browser
npm run build:firefox      # output in apps/browser/build
npm run build:prod:chrome  # Chrome
npm run build:prod:edge    # Edge
```

## Licence and attribution

This project is based on [bitwarden/clients](https://github.com/bitwarden/clients), commit `86f41566aebe5a024796df8abfb3d4d89ec509c1`, Copyright Bitwarden Inc., and is licensed under the GNU General Public License v3.0 (see `LICENSE_GPL.txt` and `LICENSE.txt`). Our changes are released under the same licence. This project is not affiliated with or endorsed by Bitwarden Inc. "Bitwarden" is a trademark of Bitwarden Inc.

The vault encryption comes from the `@bitwarden/sdk-internal` package, which is installed from npm and is not part of this repository.
