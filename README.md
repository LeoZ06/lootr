# Lootr (Beta)

*by Dr. Jekyll*

An auto looter for StarBreak (SBPE plugin). It picks up the loot you want, and only that.

## Install

Drag `lootr.py` into your SBPE `plugins` folder. There's nothing else to set up and no other plugins are needed.

## How to use

1. Press **Esc** and click **LOOTR**.
2. Pick a **Class**, **Slot** and **Item** from the dropdowns at the top left.
3. Set up the table for that item:
   - **Columns** are how many mods the item has: Stock (0), Modified (1), Custom (2), Experimental (3), Prototype (4). Only the columns the item can actually roll are shown. Implants only have Stock, for example.
   - **Rows** are the mods that item can roll. Mods that can roll twice also get an **x2** row.

### Cells

- **Left click** cycles a cell: `--` (any), `√` (want), `×` (don't want).
- **Right click** puts it back to `--`.

An item is wanted when it has **every √ mod** in its column and **no × mod**. A column with no √ means "leave it".

### Column headers

Click a column's name to switch the whole column:

| Click | Header | Picks up |
|---|---|---|
| 1st | **ANY Modified** (green) | every item with that many mods, except ones with an × mod |
| 2nd | **NONE Modified** (red) | nothing with that many mods |
| 3rd | **Modified** (normal) | whatever your √ / × marks say |

- **Right click** a header to put it straight back to normal.
- Your √ and × marks are kept underneath and come back when you switch the column back to normal.
- **Stock** only has its header: set it to **ANY Stock** to pick up stock ones.

**Example:** to pick up any Modified Soidal but never a stock one, click **Modified** once (ANY) and leave **Stock** as it is.

## Settings

Click **Settings** in the Lootr window:

| Setting | What it does |
|---|---|
| Auto Loot | Picks up wanted loot when you stand on it |
| Message On Pickup | A green "+ item" floats up when it's picked up |
| Highlight Items | A green box around wanted loot on the ground |
| Magnify Items | An enlarged copy above wanted loot on the ground |
| Highlight Items In Inventory | The same box in your inventory, stash and HUD |
| Show Chest Contents **(BETA)** | Shows wanted items above a chest before you open it, and HP when you're hurt |

Also:
- Items you drop yourself are never auto looted. They get a yellow box instead.
- A red **Inventory Full** shows when your backpack is full, at most every 5 seconds.
- **Reset To Defaults** asks first, then clears every setting and every mark.
- While the Lootr window is open, other plugins' on-screen text is hidden so it doesn't cover the menu.

Your marks and settings are saved in `lootr_settings.json` in the SBPE folder.

## Config (optional)

Paste this into `config.ini` to change the defaults:

~~~ini
[plugin_lootr]
enabled = yes
# text of the Esc menu button
label = Lootr
# your in-game interact key (SDL key name), pressed by Auto Loot
interact_key = A
~~~

If your interact key isn't **A**, set `interact_key` to match it, or Auto Loot won't pick anything up.

## Beta notes

- **Show Chest Contents** is still experimental.
- Found a bug, or a missing item, mod or x2 roll? Let me know.
