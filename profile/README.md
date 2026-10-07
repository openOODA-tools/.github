<div align="center">

<pre>
                  ___   ___  ____    _       _              _     
  ___  ___  _ __ / _ \ / _ \|  _ \  / \     | |_ ___   ___ | |___ 
 / _ \/ _ \| '_ \ | | | | | | | | |/ _ \ ___| __/ _ \ / _ \| / __|
| (_) (_) | |_) | |_| | |_| | |_| / ___ \___| || (_) | (_) | \__ \
 \___/\___/| .__/ \___/ \___/|____/_/   \_\  \__\___/ \___/|_|___/
           |_|                                                    
</pre>

### Capability-Bounded Everyday Utilities for the openOODA Era

**Two Faces, One Engine:** Blistering native CLI speed for humans • Zero-leakage MCP for AI agents  
Powered by the [openOODA](https://github.com/openOODA) sovereign systems language.

[Website](https://tools.openooda.org/) • [GitHub](https://github.com/openOODA-tools) • [openOODA Core](https://openooda.org)

</div>

---

## The Sovereign Userland

Modern CLI utilities written in 100% pure openOODA. Every tool compiles to a standalone, zero-dependency native binary, guarantees strict POSIX/GNU parity, and exposes a first-class Model Context Protocol (MCP) interface over stdio.

| Tool | Drop-in For | Parity & Capabilities | MCP Surface | Install One-Liner |
|:---|:---|:---|:---|:---|
| **[oosh](https://github.com/openOODA-tools/oosh)** | `bash` / `zsh` | Interactive sovereign shell, ambient daemon integration, dual POSIX/intent execution | Stdio IPC & daemons | `curl -fsSL https://tools.openooda.org/oosh/install.sh \| bash` |
| **[oogrep](https://github.com/openOODA-tools/oogrep)** | `grep` / `ripgrep` | Recursive regex search, `.gitignore` skipping, column tracking, colored hunks | `oogrep --mcp` (`grep_search`) | `curl -fsSL https://tools.openooda.org/oogrep/install.sh \| bash` |
| **[oodiff](https://github.com/openOODA-tools/oodiff)** | `diff` | Myers LCS algorithm, byte-for-byte GNU normal & unified (`-u`) diff parity | `oodiff --mcp` (`diff_files`) | `curl -fsSL https://tools.openooda.org/oodiff/install.sh \| bash` |
| **[oofind](https://github.com/openOODA-tools/oofind)** | `find` | Fast directory traversal, glob filtering, `-print0`, streaming JSON Lines | `oofind --mcp` (`find_files`) | `curl -fsSL https://tools.openooda.org/oofind/install.sh \| bash` |
| **[oojq](https://github.com/openOODA-tools/oojq)** | `jq` | 98% verified jq 1.8.1 parity, exact rational arithmetic, zero ambient authority | `oojq --mcp` (`jq_query`) | `curl -fsSL https://tools.openooda.org/oojq/install.sh \| bash` |
| **[ootail](https://github.com/openOODA-tools/ootail)** | `tail -f` | Inotify stream follower, truncate-safe replay, line windowing, oote themes | `ootail` IPC | `curl -fsSL https://tools.openooda.org/ootail/install.sh \| bash` |
| **[oote](https://github.com/openOODA-tools/oote)** | theme engine | Sovereign styling engine, 25 themes, dual light/dark modes, 39 semantic tokens | Theme & mascot CLI | `curl -fsSL https://tools.openooda.org/oote/install.sh \| bash` |

---

## ⚡ The Philosophy: Two Faces, One Engine

Every utility in `openOODA-tools` is architected from the start for dual consumption:

1. **For Humans**: Familiar POSIX flags, instant response times (<2ms startup), colorized outputs, and native packaging (`.deb`, `.rpm`, or curl-to-bin).
2. **For AI Agents**: Pass `--mcp` and any tool instantly becomes a JSON-RPC 2.0 Model Context Protocol server. Agents query files, diff trees, or filter logs with mathematically bounded capabilities — no shell escape vulnerabilities, no ambient disk leakage.

---

License: Apache-2.0. Built with [openOODA](https://openooda.org).
