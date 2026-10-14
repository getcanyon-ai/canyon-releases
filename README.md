# Canyon releases

Downloads for Canyon's design partners: the `canyon` CLI, the Helm chart and the list of Canyon's
container images, one GitHub release per version. Canyon's source code is not published here.

## Install the CLI

```sh
curl -fsSL https://github.com/getcanyon-ai/canyon-releases/releases/latest/download/install.sh -o install.sh && sh install.sh
```

macOS and Linux, on amd64 and arm64. The script checks the archive against the release's
`SHA256SUMS` before it installs anything. On Windows, download the `.zip` from the release page and
check it against `SHA256SUMS` yourself.

## Run Canyon

Each release carries what you install Canyon with; none of it needs Canyon's source:

- `canyon-deploy.tar.gz`: a `canyon/` directory with the laptop demo
  (`docker compose --profile demo-apps up` inside it) and `deploy/k8s`, the Kubernetes install base.
- `canyon-chart.tgz`: the Helm chart, an all-in demo on one node.
- `images.txt`: Canyon's images (`ghcr.io/getcanyon-ai/canyon-*`), each by digest.

```sh
curl -fsSL https://github.com/getcanyon-ai/canyon-releases/releases/latest/download/canyon-deploy.tar.gz | tar -xz && cd canyon
docker compose --profile demo-apps up
```

## Documentation

https://canyon-docs.boyann.workers.dev is open to invited email addresses only: sign in with the
one-time code Cloudflare emails you.

## Licence

Canyon is licensed under the Canyon Design Partner Evaluation License, included as `LICENSE` in every
archive and in the chart. It allows use within the design partner evaluation program only, and no
redistribution.
