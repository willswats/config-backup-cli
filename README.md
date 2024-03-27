# Quick Backup CLI

Quickly copy config directories to a specified location, and vice versa.

## Table of Contents

<!--toc:start-->

- [Dependencies](#dependencies)
- [Usage](#usage)
- [Features](#features)
<!--toc:end-->

## Dependencies

- grep
- sed
- cut
- [trash-cli](https://github.com/andreafrancia/trash-cli)

## Usage

To use the script, pass the directory to where you want your config directories stored, for example:

```bash
quick-backup-cli ~/Drive/Backups
```

## Features

- Configure: add programs to `~/.config/quick-backup-cli/programs.csv` for use with `quick-backup-cli`.
- Backup: copy the config directory of a program to your specified location. If the config directory already exists in your specified location, then send it to the trash.
- Download: copy the config directory of a program from your specified location to it's config location. If the directory already exists in the config location, then send it to the trash.

## Configuration

You can add programs to `quick-backup-cli` with the `configure` option when running the script, alternatively you can can create the file manually.

This is an example of a `programs.csv` file, located at `~/.config/quick-backup-cli/programs.csv`:

```csv
Retroarch,/home/will/.config/,retroarch/
RPCS3,/home/will/.config/,rpcs3/
```

Explanation of columns (each value separated by a comma):

1. The first column is the program name (only used within quick-backup-cli).
2. The second column is the parent directory of the program's config directory.
3. The third column is the program's config directory name.

The trailing '/' is required for the second and third column.
