# Skopeo for Windows

This builds [Skopeo](https://github.com/containers/skopeo) for Windows based on [this comment](https://github.com/containers/skopeo/issues/715#issuecomment-917412078).

It runs once a week to check for a new release, and if it finds one, automatically builds it and publishes it in the [releases tab](https://github.com/passcod/winskopeo/releases).
The release versions are the same as the upstream ones.

It builds a GPGme-less version, so operations involving signatures won't work.
If you need that, please fork, make it build, and send a PR!

## Usage in Github Actions

```yaml
- name: Download Skopeo
  run: curl.exe -LO https://github.com/passcod/winskopeo/releases/latest/download/skopeo.exe
```
