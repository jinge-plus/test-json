# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a minimal configuration repository for managing proxy nodes and service status. No build, test, or lint commands needed — it's plain configuration files only.

## File Structure

| File | Purpose |
|------|---------|
| `nodes` | List of proxy node domain names (one per line, JSON array format) |
| `status` | Service status configuration (JSON): `enable`, `body`, `start_time`, `end_time` |
| `.json` | Same content as `status` (backup/hidden copy) |
| `.status` | Same content as `nodes` (backup/hidden copy) |

## Common Tasks

### Update proxy nodes
Edit `nodes` file to add/remove domains:
```
["app.astralx.com", "hk-uc.1app24.com", ...]
```

### Change service status
Edit `status` file to modify `enable` (0/1), time windows, or body content.

### Commit changes
```bash
git add <files>
git commit -m "description"
git push
```
