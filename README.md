# wt

Interactive git worktree manager. Add, list, remove worktrees — with fzf.

## Install

```bash
git clone https://github.com/you/wt ~/code/wt
ln -s ~/code/wt/wt ~/.local/bin/wt
```

Requires [fzf](https://github.com/junegunn/fzf).

## Usage

Run from any git repo:

```bash
wt          # add a worktree (pick branch interactively)
wt ls       # list worktrees
wt rm       # remove a worktree (pick interactively)
wt rm feat  # remove by partial name match
```

### Add options

| Flag | Effect |
|------|--------|
| `-n`, `--no-env` | Skip copying env files |
| `-c`, `--copy <glob>` | Custom glob to copy (default: `.env*`) |

On first run, you'll be prompted for a worktree root directory.
Saved to `~/.wtroot`. Override anytime with:

```bash
WT_ROOT=~/other/path wt
```
