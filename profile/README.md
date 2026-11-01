<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/readme-banner-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="assets/readme-banner-light.svg">
    <img alt="pisentry: host security agent for Raspberry Pi and ARM Linux" src="assets/readme-banner-dark.svg" width="100%">
  </picture>
</p>

<p align="center">
  <a href="https://pisentry.dev/"><b>Website</b></a> ·
  <a href="https://github.com/pisentry/pisentry#readme"><b>Docs</b></a> ·
  <a href="https://github.com/pisentry/pisentry/releases/latest"><b>Download</b></a> ·
  <a href="https://pisentry.dev/roadmap.html"><b>Roadmap</b></a> ·
  <a href="https://github.com/pisentry/pisentry/security/policy"><b>Security</b></a>
</p>

**pisentry watches a small Linux host for the ten attacks that hit it most, ranks them, and tells you where to look first.**

- One static binary, Go standard library only. About 7 MB, under 1% CPU on a 2 GB Pi
- arm64, armv7 and amd64. Raspberry Pi OS, Ubuntu, Debian and RHEL-family hosts
- Prometheus metrics, JSON events and push alerts. Runs as a systemd service or a Kubernetes DaemonSet
- Release images ship with SLSA provenance and an SBOM

### Try it

Audit a Pi without installing anything. Exit code 2 if anything is High or Critical.

```bash
curl -fsSLO https://github.com/pisentry/pisentry/releases/latest/download/pisentry-linux-arm64
curl -fsSLO https://github.com/pisentry/pisentry/releases/latest/download/SHA256SUMS
sha256sum --check --ignore-missing SHA256SUMS
chmod +x pisentry-linux-arm64 && sudo ./pisentry-linux-arm64 audit
```

### Get involved

Detection rules and coverage gaps make the best first contributions. Read the [contributing guide](https://github.com/pisentry/pisentry/blob/main/CONTRIBUTING.md), report a [false positive](https://github.com/pisentry/pisentry/issues/new/choose), or report a vulnerability [privately](https://github.com/pisentry/pisentry/security/advisories/new).
