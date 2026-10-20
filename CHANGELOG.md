# Changelog

## 2.0.0

- Renamed from Plugin Sync to Omarchy Sync (`io.github.jacueblol.omarchy-sync`).
  Local state carries over; see the README to switch.
- Syncs keybindings (`hypr/bindings.lua`, on by default) and mouse and
  keyboard input settings (`hypr/input.lua`, off by default), plus any other
  files under `~/.config` you list.
- Pulls list each file they change with its added and removed lines, back up
  replaced files, and roll them all back if Hyprland reports new config
  errors.
- Per-machine overrides in `hypr/*.local.lua`, which never sync.
- The repo stays readable by Plugin Sync 1.x machines, which keep the new
  files when they push.

## 1.1.0

- Settings view in the panel (gear icon or `s`): choose what this machine
  syncs (installed plugins, bar layout, other shell settings), whether pulls
  remove plugins, machine-specific plugins, automatic sync mode, conflict
  handling, check interval, and notifications.
- Settings are per machine and never synced. Pushing only replaces the parts
  this machine syncs.
- Pulls are confirmed first with the exact plugins and settings they change.
  The default mode shares this machine's changes automatically and waits for
  you before applying anyone else's.
- Machine-specific plugins keep their place in the bar across pulls.
- A failed merge never writes `shell.json` or the repo.
- `settings` IPC method.

## 1.0.0

- First release.
