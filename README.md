My personal website reinstated, this time written in Spring

## Installing

### From Fedora COPR

Applicable to:

- Fedora 33
- Fedora 34
- Fedora 35
- Fedora Rawhide

Enable the `donaldsebleung/misc` repo and install the package `donaldsebleung-com`:

```bash
$ sudo dnf copr enable donaldsebleung/misc
$ sudo dnf install donaldsebleung-com
```

Then install the CA-issued key-certificate pair to their respective locations (or generate your own):

- `/etc/donaldsebleung-com/key.pem`
- `/etc/donaldsebleung-com/cert.pem`

If you private key is protected by a passphrase, edit `/etc/donaldsebleung-com/passwd` accordingly to contain the correct passphrase, then enable the service `donaldsebleung-com.service` to run at boot:

```bash
$ sudo systemctl enable --now donaldsebleung-com.service
```

## Credits

The front-end design is based on [Hyperspace](https://html5up.net/hyperspace) by [HTML5 UP](https://html5up.net), released under the [CC BY 3.0](http://creativecommons.org/licenses/by/3.0/) license.

## License

[MIT](./LICENSE)
