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

## Backups

On the home page, open a project's **Manage** menu and choose **Backup**. This saves a dated copy, such as `tinaroo-dam__backup_2026-10-12_1842.json`, into `Data\Backups\`.

To restore one, click **Open project file (.json)** on the home page and choose the backup file. It opens as a project alongside the current one, so nothing is overwritten.

## Updating the planner

Download the latest `Core Rack Planner.html` from this GitHub repository and replace the copy in the shared folder. The `Data` folder isn't affected.
