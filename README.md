# Saj Loop — release artifacts

**This repository holds signed release binaries and, from v0.5.1, the source of the six
MPL-2.0 crates that ship inside them. The rest of the Saj Loop source is private.**

Product: [sajloop.com](https://sajloop.com) · Trust page: [sajloop.com/security](https://sajloop.com/security)

## Verify Linux downloads

```bash
# minisign public key: sajloop-minisign.pub in this repo, and independently at
# https://sajloop.com/keys/sajloop-minisign.pub (key ID 9683811CD14973AE)
minisign -Vm saj-loop_0.5.1_amd64.deb -p sajloop-minisign.pub
minisign -Vm saj-loop-mpl-src-0.5.1.tar.gz -p sajloop-minisign.pub
sha256sum -c --ignore-missing SHA256SUMS   # only the files you downloaded
```

## Releases

| Version | Platform | Artifacts |
|---|---|---|
| **v0.5.1** (current) | Linux x86_64 | `saj-loop_0.5.1_amd64.deb` (full stack: desktop app + helper + MCP + `sajloop`/`sajloopctl` CLIs) · `saj-loop-mpl-src-0.5.1.tar.gz` (source of the six MPL-2.0 crates, same commit as the binaries) · `.minisig` for each · `SHA256SUMS` |
| v0.5.0 (superseded) | Linux x86_64 | `.deb` + `.AppImage` (GUI only). Superseded by v0.5.1 — security fixes; the v0.5.0 AppImage is not supported with the 0.5.1 helper. |
| — | macOS | Coming (kill-switch live end-to-end gate). |
| — | Windows | Coming. |

## Source

The six MPL-2.0 crates — `saj-tunnel`, `saj-pq`, `saj-shield`, `saj-dns`, `saj-loop-ipc`,
`saj-obfs` — are published with each Linux release as `saj-loop-mpl-src-<version>.tar.gz`,
extracted from the exact commit the binaries were built from, with a detached minisign
signature. Everything else in Saj Loop remains proprietary.

Report security issues: security@sajdak.one
