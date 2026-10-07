# openOODA-tools: Organization House Laws & Standards (v1)

This document is the **single canonical source of truth** for all code, architecture, and system integration standards across the `openOODA-tools` organization. Every human contributor and AI agent working on any repository in this organization must strictly follow these rules without exception.

---

## 1. The Page Rule (Code Layout & Sizing)

Across all openOODA tool codebases:
- **16–256 Lines**: Every committed `.oo` and `.oot` source file must be between **16 and 256 lines**, counted as exact line breaks (blank lines and comments count).
- **Shim Exemption (Floor Only)**: A file is a shim when every non-comment line is an import or re-export (`import "..."`). Shims skip the 16-line floor. The **256-line ceiling still strictly applies**.
- **Directory Density ($\le 8$ files)**: At most **8 `.oo` files per directory**, tests included. Crowded directories must split into functional subdirectories grouped by domain.
- **Banned File Names (Name the function, not the drawer)**:
  `util.oo`, `utils.oo`, `helper.oo`, `helpers.oo`, `common.oo`, `misc.oo`, `shared.oo`, `base.oo`, `core.oo`.
- **Naming Conventions**: Action pages lead with a verb (`render_diff.oo`), state pages name what they own (`theme_spec.oo`), boundary pages speak trust verbs (`verify_token.oo`).

---

## 2. The 4-Element Academy Header (Mandatory on Every Page)

Every committed `.oo` file must begin with the standard 4-element Academy docstring within its first 7 lines:

```oo
// # Component Name - Subtitle
//
// Logline: Single-sentence imperative summary of functional responsibility.
//
// Setup: Preconditions, wired capability tokens, imported contracts.
//
// Beats:
//   1. First sequential phase of execution.
//   2. Next phase.
//   3. Final phase / exit state.
```

---

## 3. openOODA Capability & Zero-Trust Discipline

Every tool in `openOODA-tools` operates strictly on the Object-Capability (OCap) security model:
- **Zero Ambient Authority**: Privileged operations require explicit, unforgeable capability tokens passed as arguments (`&ProcessCap`, `&FsReadCap`, `&FsWriteCap`, `&EnvCap`, `&NetCap`, `&SysCap`, `&TimeCap`).
- **Subprocess Safety**: Never invoke `/bin/sh -c` or `/bin/bash -c`. Direct binary execution must use explicit argv arrays via `ProcessCap`. Clean environment variables of child processes.
- **Negative-Trust Edge Falsification**: Fail-closed validation on boundary inputs (0-byte files, cyclic loops, malformed frames).

---

## 4. Unified Theming with `oote`

All openOODA tools synchronize visual presentation through `oote`:
- **Single Source of Truth**: All tools read `~/.openooda/theme.oot` or respect `OODA_THEME`, `OODA_MODE`, and `OODA_BORDER`.
- **39-Token Semantic Taxonomy**: Spanning UI chrome, status, diffs, search hits, syntax highlighting, shell prompts, and logs.
- **Graceful Capability Degradation**: Automatically emits 24-bit TrueColor, degrades to 256 or 16-color ANSI, and suppresses all ANSI escapes under `NO_COLOR`, `OODA_NO_COLOR`, or `TERM=dumb`.

---

## 5. Native systemd Citizenship & Linux Integration

This server follows a pure systemd-native architectural pattern:
1. **System Services & Unit Placement**: Services managed in `/etc/systemd/system/`. Prefer drop-in overrides (`/etc/systemd/system/<unit>.service.d/*.conf`).
2. **Declarative State & Provisioning**: Accounts declared via `systemd-sysusers` in `/etc/sysusers.d/*.conf`; directory lifecycle via `systemd-tmpfiles` in `/etc/tmpfiles.d/*.conf`.
3. **Service Confinement & Hardening**: Use native sandboxing (`ProtectSystem=`, `ProtectHome=`, `PrivateTmp=`, `NoNewPrivileges=`).
4. **Logging & Schedulers**: Logging handled exclusively by `systemd-journald`. Scheduled tasks executed via `systemd.timer` units rather than legacy cron.
5. **Standard System Directories**: Use `$RUNTIME_DIRECTORY` (`/run/openooda`), `$STATE_DIRECTORY` (`/var/lib/openooda`), `$CONFIGURATION_DIRECTORY` (`/etc/openooda`).

---

## 6. Verification & Packaging Gate

Every tool repository must pass `make verify` and provide:
- Clean standalone uninstaller (`uninstall.sh`) and helper binary (`<tool>-uninstall`).
- DNF/RPM packaging (`packaging/<tool>.spec`).
- Arch Linux packaging (`packaging/PKGBUILD` and `packaging/arch/PKGBUILD`).
- Debian/Ubuntu packaging (`packaging/debian/`).
- Web installer (`install.sh`) supporting `--uninstall`, `--dry-run`, `--dnf`, `--deb`, `--pkgbuild`.
