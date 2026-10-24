# Saj Loop — release artifacts

**This repository holds signed release binaries only. It does not contain source code.**

Source (private): not public.  
Product: [sajloop.com](https://sajloop.com)

## Verify Linux downloads

```bash
# minisign public key is in this repo: sajloop-minisign.pub
minisign -Vm saj-loop_0.5.0_amd64.deb -p sajloop-minisign.pub
sha256sum -c --ignore-missing SHA256SUMS   # only the files you downloaded
```

## v0.5.0

| Platform | Artifacts |
|---|---|
| Linux x86_64 | `.deb` (full stack: GUI + helper + MCP) + `.AppImage` (GUI only) |
| macOS | Coming (kill-switch live e2e gate) |
| Windows | Coming |

Report security issues: security@sajdak.one
