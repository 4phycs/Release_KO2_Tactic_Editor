# Changelog

## 1.1 - 2026-11-02

### Added
- **Players**: the teams of a Player Manager game disk, with their division, and the players with no club (free to be hired).
- **Players**: the teams of Player Manager saved careers. Each save on a disk is listed on its own. A game disk must also be in Sources, because the names are generated from tables in the game.
- **Import / Export**: select tactics as in a file manager (click, Ctrl+click, Shift+click; click again, or click the middle panel, to unselect), with a right-click menu instead of buttons on each row.
- **Import / Export**: a search box above the roster that filters by name, source disk, author, derived from or comment.

### Changed
- **Import / Export**: the right panel is now the new tactic disk. Add tactics from the roster menu and remove them from the panel's own menu. It holds at most 20 and is remembered by the browser.
- **Import / Export**: "Delete" is now "Remove from roster". It is greyed out when a standard tactic is selected, and it states that the original disks are not changed.

### Fixed
- **Import**: tactics read wrongly from some disks, such as Robert.adf, with all the players stuck on one side of the pitch whatever the zone.
- **Import**: disks wrongly labelled "Game Disk". Disks are now labelled by what they contain: KO2 Game Disk, PM Game Disk, PM Save Disk or Tactic Disk.

## 1.0 - 2026-10-31

First release: Windows executable and Python source.

- **Editor**: edit the positions of the 10 outfield players for each zone and situation, with the 8 standard tactics included.
- **Limits**: keep a tactic within a standard tactic plus a chosen distance, with the areas outside shown in grey and dragging held inside them.
- **Validate all**: check a tactic against the same distance and list the players outside the limits.
- **Special situations**: the kick-off keeps players in their own half, and the goal kicks discourage the strips near the box.
- **Players**: the squads and skills of a Kick Off 2 game disk.
- **Import / Export**: import tactics from Amiga disk images (`.adf` / `.sdf`) and export up to 20 tactics to a new tactic disk.
- User guide and MIT license.
