# fragata-release

RPM sources of `fragata-release`, the release package of Fragata Host: brand of the system (`os-release`,
`/etc/issue`, `xcp.branding`), its update channel (`fragata.repo`) and the key that signs its packages.

It is built from `xcp-ng-release` (branch `8.3` of xcp-ng-rpms/xcp-ng-release) and replaces it:
`Provides`/`Obsoletes` of `xcp-ng-release`, `-presets` and `-config`, so that the packages requiring them
and the upgrades of XCP-ng hosts keep working.

Fragata changes:

- `SOURCES/fragata-branding`: brand values used instead of the ones of `branding-xcp-ng`;
- `SOURCES/fragata.repo`: the only package repositories of the host;
- `SOURCES/RPM-GPG-KEY-fragata`: public key of the packages and of the repository metadata.

Build: `fragata-host/scripts/packages/build-rpm.sh <this repository> <output directory>`.
