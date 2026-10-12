# Core Rack Planner

Plans where drill core boxes go in the core shed racks: rows, bays and slots, the shed map, and the move list for each core move.

It's a single file, `Core Rack Planner.html`. There's nothing to install.

## Setting it up for the team

1. Put `Core Rack Planner.html` in the shared team folder, for example `S:\Core Shed\Core Rack Planner\`.
2. Make a folder next to it for the data, for example `S:\Core Shed\Core Rack Planner\Data`.
3. Open `Core Rack Planner.html` in **Microsoft Edge** or **Google Chrome**. Other browsers can't save to a shared folder.
4. On the home page, under **Where projects are saved**, click **Connect shared folder…** and choose the `Data` folder.

Everyone on the team does steps 3 and 4 once. After that:

- The browser remembers the folder. Each time you open the planner it asks you to click **Reconnect**, which is a browser security rule.
- Each project is saved as one file in `Data\projects\`, with all its core moves and saved filters.
- Changes made by others load automatically every 30 seconds, or straight away with **Refresh now**.
- If two people edit the same project at the same moment, the second person to save gets a warning. They can then choose **Load their version** or **Keep mine**.

Tip: make a desktop shortcut to `Core Rack Planner.html`.

## Updating the planner

Download the latest `Core Rack Planner.html` from this GitHub repository and replace the copy in the shared folder. Project data in the `Data` folder isn't affected.

## Backups

The `Data\projects` folder holds everything. Back it up like any other shared folder. You can also export a single project from inside the planner with **Export → Project file**.
