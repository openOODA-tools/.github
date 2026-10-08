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
| **[oofetch](https://github.com/openOODA-tools/oofetch)** | `fastfetch` / `neofetch` | System fetch, hardware posture, dynamic ASCII mascots, oote palette swatches | `oofetch --mcp` (`host_info`, `system_posture`) | `curl -fsSL https://tools.openooda.org/oofetch/install.sh \| bash` |
| **[oocat](https://github.com/openOODA-tools/oocat)** | `bat` / `cat` | Capability-bounded syntax viewer, oote themes, line ranges, squeeze blanks | `oocat --mcp` (`oocat_view`, `oocat_highlight`) | `curl -fsSL https://tools.openooda.org/oocat/install.sh \| bash` |
| **[ootop](https://github.com/openOODA-tools/ootop)** | `btop` / `top` | Real-time TUI dashboard, systemd slice grouping (`app`, `system`, `user`), load-reactive mascot moods | `ootop --mcp` (`system_metrics`, `process_list`, `systemd_slices`) | `curl -fsSL https://tools.openooda.org/ootop/install.sh \| bash` |
| **[oofzf](https://github.com/openOODA-tools/oofzf)** | `fzf` | Sovereign interactive fuzzy finder, subsequence scoring, oote palettes | `oofzf --mcp` (`fuzzy_match`, `rank_candidates`) | `curl -fsSL https://tools.openooda.org/oofzf/install.sh \| bash` |
| **[ools](https://github.com/openOODA-tools/ools)** | `ls` / `eza` | Sovereign directory lister, file kind classification, oote themes | `ools --mcp` (`list_directory`, `stat_entry`) | `curl -fsSL https://tools.openooda.org/ools/install.sh \| bash` |
| **[ootree](https://github.com/openOODA-tools/ootree)** | `tree` | Directory hierarchy visualizer, Unicode branch glyphs (`├── `, `└── `), `.gitignore` skipping | `ootree --mcp` (`tree_view`, `tree_summary`) | `curl -fsSL https://tools.openooda.org/ootree/install.sh \| bash` |
| **[ooclock](https://github.com/openOODA-tools/ooclock)** | `tty-clock` / `pomodoro` | Digital matrix clock, Pomodoro focus timer, stopwatch, circadian mascot moods | `ooclock --mcp` (`clock_now`, `pomodoro_status`) | `curl -fsSL https://tools.openooda.org/ooclock/install.sh \| bash` |
| **[oosed](https://github.com/openOODA-tools/oosed)** | `sed` | Capability-bounded stream editor, atomic in-place edits (`FsWriteCap`), safe text transformer | `oosed --mcp` (`sed_substitute`, `sed_stream`) | `curl -fsSL https://tools.openooda.org/oosed/install.sh \| bash` |
| **[ootar](https://github.com/openOODA-tools/ootar)** | `tar` | Traversal-resistant archive manager, zero zip-slip vulnerability, POSIX USTAR standard | `ootar --mcp` (`tar_list`, `tar_inspect`) | `curl -fsSL https://tools.openooda.org/ootar/install.sh \| bash` |
| **[oops](https://github.com/openOODA-tools/oops)** | `ps` / `pstree` | Process tree visualizer, systemd slice grouping (`system.slice`, `user.slice`), POSIX signals | `oops --mcp` (`ps_list`, `ps_tree`, `ps_kill`) | `curl -fsSL https://tools.openooda.org/oops/install.sh \| bash` |
| **[oocurl](https://github.com/openOODA-tools/oocurl)** | `curl` | Capability-bounded HTTP/API client, status classification, syntax-highlighted responses | `oocurl --mcp` (`http_request`, `parse_url`) | `curl -fsSL https://tools.openooda.org/oocurl/install.sh \| bash` |
| **[oowatch](https://github.com/openOODA-tools/oowatch)** | `watch` | Continuous command scheduler, ANSI delta diff highlighting via oote themes, iteration bounds | `oowatch --mcp` (`watch_poll`, `watch_diff`) | `curl -fsSL https://tools.openooda.org/oowatch/install.sh \| bash` |
| **[oomcp](https://github.com/openOODA-tools/oomcp)** | Universal MCP gateway / orchestrator | Multi-tool routing & dynamic discovery, multi-server stdio proxying, schema aggregation | `oomcp serve` / `oomcp list` | `curl -fsSL https://tools.openooda.org/oomcp/install.sh \| bash` |
| **[oo7z](https://github.com/openOODA-tools/oo7z)** | `7z` / `7za` | 7-Zip multi-format container unpacker and lister, anti-zip-slip safe extraction | `oo7z --mcp` (`oo7z_inspect`, `oo7z_test`, `oo7z_verify_path`) | `curl -fsSL https://tools.openooda.org/oo7z/install.sh \| bash` |
| **[ooalias](https://github.com/openOODA-tools/ooalias)** | `alias` | Cryptographically verifiable command macro and alias resolver with scope isolation | `ooalias --mcp` (`alias_resolve`, `alias_list`, `alias_verify`) | `curl -fsSL https://tools.openooda.org/ooalias/install.sh \| bash` |
| **[ooansi](https://github.com/openOODA-tools/ooansi)** | ANSI sequence generator | TrueColor RGB formatting, 256-color indexed palettes, cursor navigation, text sanitizer | `ooansi --mcp` (`ansi_generate`, `ansi_strip`, `ansi_cursor`) | `curl -fsSL https://tools.openooda.org/ooansi/install.sh \| bash` |
| **[ooapparmor](https://github.com/openOODA-tools/ooapparmor)** | `apparmor_parser` | Capability-bounded AppArmor profile generator & confinement auditor, negative trust enforcement | `ooapparmor --mcp` (`apparmor_generate`, `apparmor_verify`) | `curl -fsSL https://tools.openooda.org/ooapparmor/install.sh \| bash` |
| **[ooarchive](https://github.com/openOODA-tools/ooarchive)** | `tar` / `cpio` / `ar` | Deterministic reproducible archive builder, byte-for-byte outputs across TAR/CPIO/AR | `ooarchive --mcp` (`archive_list`, `archive_inspect`, `archive_verify_path`) | `curl -fsSL https://tools.openooda.org/ooarchive/install.sh \| bash` |
| **[ooarp](https://github.com/openOODA-tools/ooarp)** | `arp` / `ip neigh` | Capability-bounded ARP cache & neighbor discovery auditor, duplicate MAC poisoning detection | `ooarp --mcp` (`arp_list`, `arp_audit`, `arp_validate_mac`) | `curl -fsSL https://tools.openooda.org/ooarp/install.sh \| bash` |
| **[ooastdiff](https://github.com/openOODA-tools/ooastdiff)** | AST syntax differ | Language-agnostic AST syntax differ with token LCS alignment, comment/whitespace insensitivity | `ooastdiff --mcp` (`astdiff_compare`, `astdiff_tokenize`, `astdiff_check_identity`) | `curl -fsSL https://tools.openooda.org/ooastdiff/install.sh \| bash` |
| **[ooat](https://github.com/openOODA-tools/ooat)** | `at` / `batch` | Single-run scheduled command coordinator backed by transient systemd timer units | `ooat --mcp` (`at_schedule`, `at_parse_time`, `at_cancel`, `at_list`) | `curl -fsSL https://tools.openooda.org/ooat/install.sh \| bash` |
| **[ooattest](https://github.com/openOODA-tools/ooattest)** | `tpm2_pcrread` / `tpm2_checkquote` | Attests system state and measured boot hashes using TPM2 hardware security chips | `ooattest --mcp` (`attest_status`, `attest_pcrs`, `attest_verify`, `attest_hash_pcr`) | `curl -fsSL https://tools.openooda.org/ooattest/install.sh \| bash` |
| **[ooaudit](https://github.com/openOODA-tools/ooaudit)** | `auditd` / `syscheck` | Immutable audit recorder logging system calls, IO streams, and agent decisions | `ooaudit --mcp` (`audit_record`, `audit_verify`, `audit_query`, `audit_stats`) | `curl -fsSL https://tools.openooda.org/ooaudit/install.sh \| bash` |
| **[ooawk](https://github.com/openOODA-tools/ooawk)** | `awk` / `gawk` | Data-driven pattern scanning and text processing language with exact arithmetic | `ooawk --mcp` (`awk_eval`, `awk_filter`, `awk_project`, `awk_stats`) | `curl -fsSL https://tools.openooda.org/ooawk/install.sh \| bash` |

---

## ⚡ The Philosophy: Two Faces, One Engine

Every utility in `openOODA-tools` is architected from the start for dual consumption:

1. **For Humans**: Familiar POSIX flags, instant response times (<2ms startup), colorized outputs, and native packaging (`.deb`, `.rpm`, or curl-to-bin).
2. **For AI Agents**: Pass `--mcp` and any tool instantly becomes a JSON-RPC 2.0 Model Context Protocol server. Agents query files, diff trees, or filter logs with mathematically bounded capabilities — no shell escape vulnerabilities, no ambient disk leakage.

---

License: Apache-2.0. Built with [openOODA](https://openooda.org).
