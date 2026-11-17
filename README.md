# Core Rack Planner

Plans where drill core boxes go in the core shed racks: rows, bays and slots, the shed map, and the move list for each core move.

It's a single file, `Core Rack Planner.html`. There's nothing to install.

## Setting it up on the shared drive

Make this layout on the shared drive. You only create the two folders; the planner creates everything inside `Data` itself.

```
S:\...\Software\Core Rack Planner\
    Core Rack Planner.html      ← the planner (from this GitHub repo)
    Data\                       ← connect the planner to this folder
        projects\               ← created by the planner: one file per project
        Backups\                ← created by the planner: dated backups
```

Then each team member, once:

1. Opens `Core Rack Planner.html` in **Microsoft Edge** or **Google Chrome**. Other browsers can't save to a shared folder.
2. On the home page, under **Where projects are saved**, clicks **Connect shared folder…** and chooses the `Data` folder.

After that:

- The browser remembers the folder. Each time you open the planner it asks you to click **Reconnect**, which is a browser security rule.
- Each project is one file in `Data\projects\`, holding the saved layout, all its core moves and saved filters.
- Changes made by others load automatically every 30 seconds, or straight away with **Refresh now**.
- If two people edit the same project at the same moment, the second person to save gets a warning. They can then choose **Load their version** or **Keep mine**.
- Deleting a project in the planner deletes its file from `Data\projects\`. Take a backup first if you might want it back.

Tip: make a desktop shortcut to `Core Rack Planner.html`.

## Voice control (online moves)

At the top of an online move, click **Move with Jasper**. Jasper grows out of the button to fill the window, with an animated orb, and starts listening (the small button at the top right makes it full screen); ✕ or Esc closes it. The normal on-screen controls are below the button, as before. With Jasper open, say a box, like “diamond drill one oh two box fourteen”. The planner shows it and answers “DD102 box 14 into slot A1-2”. Then say **placed**, **what slot**, **doesn’t fit**, **next option**, **slot changed to …** (then **confirmed**), **pallet**, **undo**, **next box**, **repeat**, **how many left** or **stop listening**. Add the feature first when two holes share a name (“bravo mike alpha one diamond drill one oh two box three”). The gear next to the mic turns on a wake word, so commands only count when they start with “Jasper”. The full list is in *CIS Voice Commands.docx*.

It runs entirely on the laptop using [Vosk](https://alphacephei.com/vosk/) and the computer’s own voices, so it works without internet once the files are in place. Set it up once:

1. Download `vosk.js` from the [vosk-browser](https://github.com/ccoreilly/vosk-browser) project (the `dist/vosk.js` file of its npm package).
2. Download the small English model, `vosk-model-small-en-us-0.15`, from the [Vosk models page](https://alphacephei.com/vosk/models). Keep it as a `.tar.gz` file (if it came as a `.zip`, re-pack the folder as `.tar.gz`).
3. Make a folder called `Voice` inside the shared `Data` folder and put both files in it:

```
Data\
    Voice\
        vosk.js
        vosk-model-small-en-us-0.15.tar.gz
```

4. In an online move, click **Voice control** and allow the microphone.

If no shared folder is connected, the planner asks you to choose the two files each time you turn voice on.

Hole IDs are matched by their letters and number: `DD102` is said “diamond drill one oh two”. `RC` is said “reverse circulation”. Other codes can be said as letters, plainly or with the phonetic alphabet.

### Pallet list (Jasper notes)

The small Jasper orb at the end of the tabs opens a pallet list you can dictate. Jasper fills the window, with the orb at the top and the table below. Press the orb (or your headphones’ play button) to start and stop listening, and read each box (“bravo mike alpha one, diamond drill one oh two, box three out of eight, from twelve point five until fifteen point two”, then “done”). Field names can be said in any order, “until” marks the end depth and “out of” the number of boxes. Jasper reads it back, then say “next” or “edit”. The table is editable on screen too, with a typed Notes column and a + to add rows. The icons at the top right export (Excel or CSV, with an option to reverse the order), clear and close; the ? at the top left has the dictation help and the phonetic alphabet. The columns match CIS’s pallet sheet, so the file can be uploaded in Move mode. Lists are kept per project in the browser until cleared.

If the voice model gets stuck on loading, click **Reset voice model** (shown after a failed load) or reload and start Jasper again; CIS clears a half-loaded copy by itself. Loading uses a few hundred MB, up to about 1 GB, so keep one CIS tab open while it loads.

## Backups

On the home page, open a project's **Manage** menu and choose **Backup**. This saves a dated copy, such as `tinaroo-dam__backup_2026-10-12_1842.json`, into `Data\Backups\`.

To restore one, click **Open project file (.json)** on the home page and choose the backup file. It opens as a project alongside the current one, so nothing is overwritten.

## Updating the planner

Download the latest `Core Rack Planner.html` from this GitHub repository and replace the copy in the shared folder. The `Data` folder isn't affected.
