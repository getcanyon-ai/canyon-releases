# Canyon releases

Canyon's releases: the `canyon` CLI, the Helm chart and the list of Canyon's container images, one
GitHub release per version. Canyon's source code is at
[getcanyon-ai/canyon](https://github.com/getcanyon-ai/canyon).

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

https://www.getcanyon.ai/docs/

## Licence

Canyon is open source under the GNU Affero General Public License v3.0 (AGPL-3.0-only). The `canyon`
CLI with its agent skill, and the contracts in `contracts/`, are under the Apache License 2.0, and the
Canyon Enterprise code in `ee/` is under the Elastic License 2.0. The source repository's
[LICENSE](https://github.com/getcanyon-ai/canyon/blob/main/LICENSE) says which part is under which
licence, and every archive and the chart carry it as `LICENSE`. Third-party components carry their own
licences, listed in `NOTICE` and `THIRD_PARTY_NOTICES`.
