# vi-humanize

A skill for writing and editing natural Vietnamese: text that fits its
reader, keeps the author's meaning and voice, and drops formulaic,
machine-sounding, or translated-sounding patterns. It covers drafting,
editing, reviewing, and translating, and includes brief guidance for English.

Viết và biên tập tiếng Việt tự nhiên, đúng người đọc, giữ nghĩa và giọng tác giả.

The skill lives in [`skills/vi-humanize/`](skills/vi-humanize/SKILL.md). It
activates on its own description (for example "bớt giọng AI", "humanize",
"soát văn", or a Vietnamese email or report to draft). It ships no hooks or
scripts.

## Install

| Harness | Recommended installation | Fallback |
|---|---|---|
| Claude Code | Claude Code plugin | Copy `skills/vi-humanize` into `~/.claude/skills/` |
| Codex CLI / desktop | Codex native plugin | Copy `skills/vi-humanize` into `$HOME/.agents/skills/` |

The plugin and the skills-only copy load the same skill. The plugin is
easier to update and remove.

### Claude Code plugin

```bash
# try it in one session
claude --plugin-dir /path/to/vi-humanize

# or install persistently, from a local checkout
claude plugin marketplace add /path/to/vi-humanize
claude plugin install vi-humanize@vi-humanize

# or straight from GitHub
claude plugin marketplace add nguyentrieuanduong/vi-humanize
claude plugin install vi-humanize@vi-humanize
```

### Codex native plugin

```bash
# from GitHub (recommended)
codex plugin marketplace add nguyentrieuanduong/vi-humanize
# or from a local checkout (absolute path)
codex plugin marketplace add /absolute/path/to/vi-humanize

codex plugin add vi-humanize@vi-humanize
codex plugin list --json
```

`codex plugin add` copies the whole local directory into the plugin cache,
including untracked and gitignored files. For a local install, use a clean
clone rather than a working directory that holds `envs/` or `references/`.

### Skills-only fallback

```bash
cp -R skills/vi-humanize ~/.claude/skills/        # Claude Code
cp -R skills/vi-humanize "$HOME/.agents/skills/"  # Codex
```

## Upgrade and uninstall

To upgrade, update your checkout first (`git pull`), then refresh the
installed copy as described below.

**Claude Code plugin:**

```bash
# upgrade a cached install to a new plugin.json version, then restart
claude plugin update vi-humanize@vi-humanize

# uninstall
claude plugin uninstall vi-humanize@vi-humanize
claude plugin marketplace remove vi-humanize
```

A plugin installed from a local folder is read from that folder, so edits
take effect at the next session start or after `/reload-plugins`.

**Codex native plugin:**

```bash
# upgrade: re-adding copies the checkout into the plugin cache, then restart Codex
codex plugin add vi-humanize@vi-humanize

# uninstall (also removes the plugin cache)
codex plugin remove vi-humanize@vi-humanize
codex plugin marketplace remove vi-humanize
```

Codex installs a copy, so after every change to the checkout, run
`codex plugin add` again. This applies even when the version hasn't changed.

**Skills-only:** to upgrade, replace the copied `vi-humanize` directory; to
uninstall, delete it.

## Releasing

Bump `version` in both `.claude-plugin/plugin.json` and
`.codex-plugin/plugin.json` together. Claude Code's `plugin update` only
picks up changes when the version changes.

## Sources

vi-humanize is distilled from these projects. All the GitHub projects are
MIT-licensed:

| Project | License | What it contributed |
|---|---|---|
| [blader/humanizer](https://github.com/blader/humanizer) | MIT | Why machine text reads that way; the pattern groups; "a voice sample beats rules" |
| [andyluu98/vn-humanize](https://github.com/andyluu98/vn-humanize) | MIT | Vietnamese sign catalogue; signals to keep; register-by-genre table |
| [cuongducle/viet-humanize](https://github.com/cuongducle/viet-humanize) | MIT | Read context first; no banned-word list; preserve certainty level; output only the product |
| [fioenix/vietnamizer](https://github.com/fioenix/vietnamizer) | MIT | Translated-grammar patterns with "don't fix when" cases; dash conventions |
| [AnhTuan2111/vina-me](https://github.com/AnhTuan2111/vina-me) | MIT | Seven rules for new writing; the "person next to you" test; over-editing list |
| [longhang2004/vietnamese-humanizer](https://github.com/longhang2004/vietnamese-humanizer) | MIT | Forms of address and formality; separating translationese from valid passive and Sino-Vietnamese |
| [kkhanh-kas/humanizer-VietAcademic](https://github.com/kkhanh-kas/humanizer-VietAcademic) | MIT | Academic conventions not to "fix" |
| [conorbronsdon/avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing) | MIT | Capping edit passes; not inserting fake "human signals" |
| [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) | CC BY-SA 4.0 | Origin of most of the sign catalogue (ideas only) |

- [`skills/vi-humanize/references/sources.md`](skills/vi-humanize/references/sources.md)
  (Vietnamese) has the full breakdown, where this skill deliberately departs
  from its sources, how far its rules have been validated, and the upstream
  commits checked.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) reproduces each
  upstream copyright notice.

## License

[MIT](LICENSE). Third-party notices: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
