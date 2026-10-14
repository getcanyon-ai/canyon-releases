# Canyon releases

Downloads for Canyon's design partners: the `canyon` CLI, the Helm chart and the list of Canyon's
container images, one GitHub release per version. Canyon's source code is not published here.

## Install the CLI

```sh
curl -fsSL https://github.com/boyand/canyon-releases/releases/latest/download/install.sh -o install.sh && sh install.sh
```

macOS and Linux, on amd64 and arm64. The script checks the archive against the release's
`SHA256SUMS` before it installs anything. On Windows, download the `.zip` from the release page and
check it against `SHA256SUMS` yourself.

## Images and the Helm chart

Each release's `images.txt` names Canyon's seven images (`ghcr.io/boyand/canyon-*`) by digest, and
`canyon-<chart version>.tgz` is the Helm chart for that release.

## Documentation

https://canyon-docs.boyann.workers.dev is open to invited email addresses only: sign in with the
one-time code Cloudflare emails you.

## Licence

Canyon is licensed under the Canyon Design Partner Evaluation License, included as `LICENSE` in every
archive and in the chart. It allows use within the design partner evaluation program only, and no
redistribution.
