<!--
  Copyright (c) 2024 Michael Federczuk
  SPDX-License-Identifier: CC-BY-SA-4.0
-->

<!-- markdownlint-disable no-duplicate-heading -->

# Changelog #

All notable changes to this project will be documented in this file.
The format is based on [**Keep a Changelog v1.0.0**](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [**Semantic Versioning v2.0.0**](https://semver.org/spec/v2.0.0.html).

## Unreleased ##

### Changed ###

* The script was given a much needed makeover
* Argument parsing was greatly improved
* The repo owner and issue label JSON file are now passed in through CLI arguments
* The access token file is now located at `$XDG_CONFIG_HOME/replace-gh-labels/access_token.txt`

### Added ###

* Added the option `--dry-run`
* There now is a proper help text when using the option `--help`
* It is now possible to authenticate with a different user than who the repository owner is

## [v1.0.0-rc01] - 2020-09-15 ##

[v1.0.0-rc01]: https://github.com/mfederczuk/replace-gh-labels/releases/tag/v1.0.0-rc01

Initial Release
