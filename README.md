# Liftany

Run small Python scripts from anywhere without packaging or path management.  A convenience utility for ad hoc creation and use of Python and Rust micro-tools.

## Example use case

A user casually creates a new Python script — a micro-tool made in the least amount of time possible.

No project structure. No pip install. Just a single .py file.

Liftany allows that script to be run on the command line as simply `liftany <name>` from anywhere.  There is no need to remember the .py extension or retype the full path, even when routinely creating new subfolders for organization.   Liftany recursively searches all subfolders under previously-known top-level folders.

## Top uses include

| Command | Description |
|---|---|
| `liftany <name>` | Finds and runs a Python script located under any subfolder of the top-level folders listed in `liftany.cfg` |
| `liftany -s <name>` | Creates a Windows desktop shortcut equivalent to `liftany <name>` |
| `liftany *` | Rebuilds the current Rust project and lifts the resulting binary or binaries from nested build folders into the current folder |
| `liftany -a` | Archives relevant contents of the current workspace into a sibling folder whose name ends with `-archive` |
| `liftany --help` | Displays help |

## Setup of liftany (Windows)

Place `liftany.exe` in a folder that is included in the system `PATH`.

The first time it runs, liftany automatically creates `liftany.cfg` next to the executable. The file contains comments explaining the configuration format.  The file also has its folder already added as a top-level folder.  You can edit or add folders by opening `liftany.cfg` in any text editor, such as Notepad.
