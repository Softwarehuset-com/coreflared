# coreflared

Zero-header tunnels to your services. This repository hosts the CLI releases
(`coreflared` and `coreflaredctl`) for macOS and Linux, amd64 and arm64.

## Install

```sh
brew install softwarehuset-com/tap/coreflared
```

or from a release tarball, verified against `SHA256SUMS`:

```sh
V=v0.1.0; OS=$(uname -s | tr A-Z a-z); ARCH=$(uname -m | sed 's/x86_64/amd64/;s/aarch64/arm64/')
curl -sfL "https://github.com/Softwarehuset-com/coreflared/releases/download/$V/coreflared_${V}_${OS}_${ARCH}.tar.gz" \
  | tar -xz -C /usr/local/bin coreflared coreflaredctl
```

## Use

```sh
coreflared --login                  # once; opens the browser
coreflared --host localhost:3000 --secure
```

Releases are built and signed off by the coreflared CI at code.core.ci.
