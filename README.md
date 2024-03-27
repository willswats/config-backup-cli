# Quick Backup CLI

Quickly copy directories to a specified location, and vice versa.

## Table of Contents

<!--toc:start-->

- [Dependencies](#dependencies)
- [Features](#features)
- [Configuration](#configuration)
<!--toc:end-->

## Dependencies

- grep
- sed
- cut
- [trash-cli](https://github.com/andreafrancia/trash-cli)

## Features

### Configure

Add programs to `~/.config/quick-backup-cli/programs.csv` for use with `quick-backup-cli`.

### Backup

1. Trash (if it exists) the backup directory.
2. Make the backup directory.
3. Copy the contents of the program directory to the backup directory.

### Download

1. Trash (if it exists) the program directory.
2. Make the program directory.
3. Copy the contents of the backup directory to the program directory.

## Configuration

You can add programs to `quick-backup-cli` with the `configure` option when running the script, alternatively you can can create the file manually.

This is an example of a `programs.csv` file, located at `~/.config/quick-backup-cli/programs.csv`:

```csv
Retroarch,/home/user/.config/retroarch/,/home/user/Drive/Games/Backups/Retroarch/
osu!,/home/user/.local/share/osu/,/home/user/Drive/Games/Backups/osuBackup/
```

Explanation of columns (each value separated by a comma):

1. The first column is the program name (only used within quick-backup-cli).
2. The second column is the path to the directory that you would like to backup.
3. The third column is the path to the backup directory.

The trailing `/` is required for the second and third column.
