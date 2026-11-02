# KO2 Tactics Editor — quick user guide

## Start
1. Unzip the whole folder somewhere you can write (e.g. Desktop or Documents, not `C:\Program Files`).
   The editor keeps your tactics next to the exe.
2. Double-click `KO2TacticEditor.exe`. The first time Windows may say "Windows protected your PC":
   click *More info* → *Run anyway*.
3. A black console window opens: keep it open while you use the editor (closing it stops the editor).
4. Open http://localhost:5000 in your browser. After an update, refresh with **Ctrl+F5**.

Only one copy can run at a time (it uses port 5000).
The **Players** page and the **Speed** dropdown need your own Kick Off 2 disk: copy `KO2CV137.ADF` into the
`Sources` folder (or add it from the Import / Export page). Everything else works without it.
The Players page also reads a Player Manager game disk and saved careers: copy those disks into `Sources` too
(a save disk still needs a Kick Off 2 or Player Manager game disk next to it, for the player names).

## Basics
- A tactic gives the position of the 10 outfield players (P2–P11) in 20 situations:
  - 12 **ball zones** (the pitch split into 4 × 3 zones; zone 1 is near your own goal);
  - **Own / Opp Kick-off**, **Own / Opp Goal Kick**;
  - 4 **corners**.
- **Choose the situation**:
  - click a button under *Specials* on the right, or open *Zones ▶* and click a zone;
  - or click an empty spot of the pitch to jump to that ball zone.
- **Move a player**: drag it. The 8 standard tactics are read-only: clone one to edit it.
- **Tactic** dropdown: pick the tactic to edit.
  - **New**, **Clone**, **Rename** and **Delete** do what their names say.
  - **Save** writes your changes.
- **Undo / Redo**: Ctrl+Z / Ctrl+Y. The **▶** button next to them shows the history list; click an entry to go back to it.

## Looking at a tactic
- **Compare**: draws a second tactic over yours.
  - **Attack / Defend** sets how it is drawn. In Defend mode the second tactic is turned 180°, as the opponent sees it.
- **L → R** cycles the pitch orientation: left-right, down-up, up-down.
- **Movement** shows arrows from the previous situation to the current one.
- **Circles** switches between players drawn as circles or as numbers only.
- **Zoom**: Ctrl + mouse wheel zooms; **Fit** resets the view.
- **Animate** moves the players from the previous situation to the new one when you change situation. The box next to it sets the duration in seconds.
- **Speed**: a team whose Pace sets how fast the players run in the animation (Pace 200 = full speed).

## Editing faster
- **Copy Zone / Paste Zone**: copies all positions of one situation into another, also between tactics.
- **Mirror**: makes the situation symmetric left / right, using the player pairs of the formation.
- Right-click a zone (on the pitch or on its button) for the same three commands.
- **Formation** panel: shows which players are in each line (attack, midfield, defence).
  - Drag players between the lines.
  - **Auto** guesses the formation from zone 7.

## Limits and Validate all
These tools keep a tactic close to the 8 standard tactics.

- **Distance dropdown**: *original* or *1, 2, 3, 5, 10 m inside* (on a 105 m pitch). It moves the limits towards the halfway line.
- **Validate all** checks every situation against all 8 standard tactics. In each situation, the most forward player and the last player must be within those of at least one standard tactic, moved inwards by the chosen distance. A report lists the situations that fail.
- **Limits**: choose a standard tactic as the base for your tactic. In each of the 12 ball zones:
  - no player may be more forward than the base tactic's most forward player, nor further back than its last player (minus the distance);
  - the pitch beyond the limits is greyed out, and you cannot drag a player there;
  - players outside the limits get a red ring, and the message next to Limits lists them (e.g. *ball in zone 3: P7, P9*).
- The Limits choice is saved with the tactic.
- When you clone a standard tactic, Limits is set to it automatically.
- Set Limits to *-- none --* to remove it.
- **Always on, with or without a base**:
  - **Kick-offs**: players must stay in their own half. This is enforced.
  - **Goal kicks**: the strip near the goal of the kick is only *discouraged*. It is shaded lightly, players there get an orange ring, and you can still drag them in. The exact box is not known, and the game probably moves players out of it anyway.
- Corners are free.

## Other pages
- **Players** (`/players`): the skills of the players on a Kick Off 2 or Player Manager game disk, or in a Player Manager saved career (each save on a disk is listed on its own; a game disk must also be in Sources, because the names are generated from tables in the game). Filter by disk, team and role, or search by name. For Player Manager the teams show their division, and the players with no club are listed apart.
- **Import / Export** (`/disk`):
  - **Tactic Roster** (left): select tactics as in a file manager (click, Ctrl+click, Shift+click; click again to unselect) and right-click to open them, add them to the new disk or remove them from the roster. The search box filters by name, disk, author, derived from or comment. Removing a tactic from the roster does not change the disk it was imported from; the standard tactics (locked) cannot be removed.
  - **Import from Disk** (centre): add Amiga disk images (`.adf` / `.sdf`) and import their tactics into your roster.
  - **Export to Tactic Disk** (right): the tactics of the new disk, at most 20. Right-click to remove them; **Export Disk** creates the ADF tactic disk to use in the game.
