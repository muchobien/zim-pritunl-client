# zim-pritunl-client

> [!IMPORTANT]
> Moved to [muchobien/zim-modules](https://github.com/muchobien/zim-modules/tree/main/pritunl-client), with its history. This repo is archived. In `~/.zimrc`, replace `zmodule muchobien/zim-pritunl-client` with:
>
> ```zsh
> zmodule muchobien/zim-modules --root pritunl-client
> ```

[zim module](https://github.com/zimfw/zimfw) for [pritunl-client](https://client.pritunl.com),
the Pritunl client's command line tool

## Features

- Completion for `pritunl-client`, its commands and flags, generated from
  `pritunl-client completion zsh`.

## Install

Add it to `~/.zimrc`, then run `zimfw install`:

```zsh
zmodule muchobien/zim-pritunl-client
```

The Pritunl app ships `pritunl-client` inside its bundle and doesn't put it on
`PATH`. The module finds it there anyway, but completion runs `pritunl-client`
by name, so put it on `PATH` too, e.g. with mise:

```toml
[env]
_.path = ["/Applications/Pritunl.app/Contents/Resources"]
```

The completion is generated into `functions/_pritunl-client` in the module's
directory, again whenever `pritunl-client` is updated.
