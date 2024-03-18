# Config Backup CLI

A shell script made for quickly backing up configs to cloud storage.

## Table of Contents

<!--toc:start-->

- [Features](#features)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Currently Supported Programs](#currently-supported-programs)
<!--toc:end-->

## Features

The features described here will only work with the [currently supported programs](#currently-supported-programs):

- Backup: copy the config directory of a program to your specified location. If the config directory already exists in your specified location, then send it to the trash.
- Download: copy the config directory of a program from your specified location to it's config location. If the directory already exists in the config location, then send it to the trash.

## Dependencies

- [trash-cli](https://github.com/andreafrancia/trash-cli)

## Usage

To use the script, pass the directory to where you want your backups stored, for example:

```bash
config-backup-cli ~/Drive/Backups/
```

## Currently Supported Programs

- Retroarch
- Yuzu
- RPCS3
- osu!lazer
