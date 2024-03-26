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
- [trash-cli](https://github.com/andreafrancia/trash-cli)

## Usage

To use the script, pass the directory to where you want your config directories stored, for example:

```bash
quick-backup-cli ~/Drive/Backups/
```

## Features

- Configure: add programs to `quick-backup-cli`.
- Backup: copy the config directory of a program to your specified location. If the config directory already exists in your specified location, then send it to the trash.
- Download: copy the config directory of a program from your specified location to it's config location. If the directory already exists in the config location, then send it to the trash.
