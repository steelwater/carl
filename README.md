# CaRL

```text
  ____      ____  _
 / ___|__ _|  _ \| |
| |   / _` | |_) | |
| |__| (_| |  _ <| |___
 \____\__,_|_| \_\_____|
```

**Chronolith Adventure Runic Labyrinth**

A turn-based ASCII roguelike about a boy, a luminous Orb, and the things waiting beneath St. Roch Cemetery.

CaRL is presented as the **Chronolith Adventure Runic Labyrinth Simulator**—a recovered terminal reconstruction of an event said to have taken place in New Orleans in 1878.

---

```text
 ___ _____ ___  _____   __
/ __|_   _/ _ \| _ \ \ / /
\__ \ | || (_) |   /\ V /
|___/ |_| \___/|_|_\ |_|
```

## Story

**New Orleans, 1878.**

In an age of fever, mourning, ghouls, and ghosts, a boy named **Carl** follows a luminous Orb into a sealed mausoleum beneath St. Roch Cemetery.

The Orb feeds on fragments of Chronolith and grows stronger as Carl descends. Beneath the cemetery are three shifting labyrinth levels, hostile ghouls, locked passages, a Hell Gate, and a Demon guarding an unidentified Rune.

Guide Carl into the depths, defeat the Demon, allow the Orb to absorb the Rune, and return to the cemetery alive.

Within the fiction, **One Touched** preserved Carl's story by creating the simulator of what happened.

---

```text
  ___    _   __  __ ___
 / __|  /_\ |  \/  | __|
| (_ | / _ \| |\/| | _|
 \___|/_/ \_\_|  |_|___|
```

## Game Overview

CaRL is a compact browser game built with plain HTML, CSS, and JavaScript.

The game combines:

- turn-based movement
- procedurally arranged ASCII labyrinths
- line of sight and persistent exploration
- resource management
- character and Orb progression
- fleeing and pursuing enemy behavior
- environmental storytelling
- light and dark terminal themes
- keyboard and touch controls

The current adventure begins at **St. Roch Cemetery**, continues through three mausoleum depths, and ends when Carl returns above ground after recovering the Rune.

---

```text
  ___  ___      _   _
 / _ \| _ \    /_\ | |
| (_) |   /   / _ \| |__
 \___/|_|_\  /_/ \_\____|
```

## The Orb

The Orb is both Carl's protector and the game's progression system.

### Chronolith shards

- `.` Small Chronolith shards grant **20% XP**.
- At **100% XP**, the Orb levels up and gains **2 Skill Points**.
- `O` Large Chronolith shards restore **1 Light Aura charge**.

### Defensive Aura

The Defensive Aura absorbs damage before Carl loses HP.

Press `E` to spend 1 Skill Point and increase its maximum strength by 5.

### Light Aura

Press `Space` to consume one Light Aura charge and transform Carl from `c` into powered Carl `C`.

While powered, Carl:

- moves up to two tiles
- causes ghouls to flee
- destroys fleeing ghouls on contact
- can damage the Demon

Press `Q` to spend 1 Skill Point on the Light Aura, increasing its duration and power.

Returning to the cemetery under the Full Moon restores the Light Aura to 2 charges and completely refills the Defensive Aura.

---

```text
  ___ ___  _  _ _____ ___  ___  _    ___
 / __/ _ \| \| |_   _| _ \/ _ \| |  / __|
| (_| (_) | .` | | | |   / (_) | |__\__ \
 \___\___/|_|\_| |_| |_|_\\___/|____|___/
```

## Controls

| Key | Action |
| --- | --- |
| Arrow keys / `WASD` | Move Carl |
| `Space` | Activate the Light Aura |
| `E` | Spend a Skill Point on the Defensive Aura |
| `Q` | Spend a Skill Point on the Light Aura |
| `M` | Toggle the terminal theme |
| `R` | Restart the simulation |

Touch controls are shown automatically on smaller screens.

---

```text
 ___ __  __ ___  ___  _    ___
/ __|\ \/ /|  _ )/ _ \| |  / __|
\__ \ >  < |  _ \ (_) | |__\__ \
|___//_/\_\|___/\___/|____|___/
```

## Symbols

| Symbol | Meaning |
| --- | --- |
| `c` | Carl |
| `C` | Carl powered by the Light Aura |
| `G` | Ghoul |
| `g` | Fleeing ghoul |
| `.` | Small Chronolith shard |
| `O` | Large Chronolith shard |
| `k` | Mausoleum key |
| `M` | Passage to a deeper level |
| `<` | Stairs leading upward |
| `D` | Demon |
| `R` | Rune relic |
| `H` | Hell Gate |
| `t` | Tombstone—bump into it to read the inscription |
| `#` | Wall |

Creatures and items are only visible within Carl's current line of sight. Previously explored walls and passages remain mapped.

---

```text
  ___  ___      _ ___ ___ _____ _____   _____
 / _ \| _ )    | | __/ __|_   _|_ _\ \ / / __|
| (_) | _ \ _  | | _| (__  | |  | | \ V /| _|
 \___/|___/| |_| |___\___| |_| |___| \_/ |___|
             \___/
```

## Objective

1. Enter the mausoleum from St. Roch Cemetery.
2. Explore all three underground levels.
3. Collect shards and strengthen the Orb.
4. Find keys needed for deeper passages.
5. Survive the ghouls and the pursuing Demon.
6. Defeat the Demon while powered.
7. Collect the glowing Rune relic.
8. Climb back to the cemetery to complete the story.

Retreating to an upper level is always possible through `<`, and returning to the cemetery restores Carl's protective auras.

---

```text
 ___  _   _ _  _
| _ \| | | | \| |
|   /| |_| | .` |
|_|_\ \___/|_|\_|
```

## Run Locally

No build process or package installation is required.

Clone the repository:

```bash
git clone https://github.com/steelwater/carl.git
cd carl
```

Then open the game file in a browser:

```text
src/index.html
```

You can also serve the repository with any simple local web server:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/src/`.

---

```text
 _____ ___ ___ _  _ _  _ ___ ___  _   _
|_   _| __/ __| || | \| / _ \| | | |
  | | | _| (__| __ | .` | (_) | |_| |
  |_| |___\___|_||_|_|\_|\___/ \___/
```

## Technology

The game currently uses:

- semantic HTML
- responsive CSS
- vanilla JavaScript
- browser keyboard events
- touch-friendly controls
- procedural map generation
- ASCII rendering inside a terminal-style interface

The entire playable game is contained in [`src/index.html`](src/index.html).

---

```text
 ___ _____ _ _____ _   _ ___
/ __|_   _/_\_   _| | | / __|
\__ \ | |/ _ \| | | |_| \__ \
|___/ |_/_/ \_\_|  \___/|___/
```

## Status

Active and evolving.

The current version includes the complete core journey from St. Roch Cemetery through three mausoleum levels, Orb progression, fog of war, ghoul behavior, Demon combat, Rune recovery, and the closing return to the cemetery.

Development currently focuses on playtesting, balancing, bug fixes, presentation, and continued lore refinement.

---

```text
 _    ___  ___ ___
| |  / _ \| _ \ __|
| |_| (_) |   / _|
|____\___/|_|_\___|
```

## Lore Connection

CaRL shares concepts with the wider **Terminal Lore** universe, including Chronolith, recovered history, terminal simulations, and events reconstructed long after they occurred.

The game is designed to work as a self-contained adventure while also serving as a small interactive fragment of that larger setting.

---

```text
 _  _  ___ _____ ___
| \| |/ _ \_   _| __|
| .` | (_) || | | _|
|_|\_|\___/ |_| |___|
```

## Final Note

> The Orb remembers the path.
>
> The simulator remembers the boy.
>
> The cemetery remembers everything else.
