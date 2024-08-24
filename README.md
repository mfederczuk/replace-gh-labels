<!--
  Copyright (c) 2024 Michael Federczuk
  SPDX-License-Identifier: CC-BY-SA-4.0
-->

# `replace-gh-labels` #

[version_shield]: https://img.shields.io/badge/version-1.0.0--rc01-informational.svg
[release_page]: https://github.com/mfederczuk/replace-gh-labels/releases/tag/v1.0.0-rc01 "Release v1.0.0-rc01"
[![version: 1.0.0-rc01][version_shield]][release_page]
[![Changelog](https://img.shields.io/badge/-Changelog-informational.svg)](CHANGELOG.md "Changelog")

## About ##

`replace-gh-labels` is a Bash script to replace all existing issue labels of a GitHub repository with new ones supplied
from a file.

## Usage ##

The first argument is the repository owner and repository name — separated by a slash.  
The second argument is the path to the JSON file containing the new issue labels.

```sh
replace-gh-labels mfederczuk/replace-gh-labels issue_labels.json
```

The JSON schema of the file is:

```ts
[
	{
		"name": string,
		"description": string | null,
		"color": string | null
	}
]
```

The username and personal access token that are used for authentication are read from the files
`$XDG_CONFIG_HOME/replace-gh-labels/user.txt` and `$XDG_CONFIG_HOME/replace-gh-labels/access_token.txt` respectively.  
If username file does not exist, then repository owner is used instead.

## Download & Installation ##

Just download the script from this repository, add the executable bit.  
Optionally add it to the `$PATH`.

```sh
wget https://github.com/mfederczuk/replace-gh-labels/raw/v1.0.0-rc01/replace-gh-labels &&
	chmod +x replace-gh-labels
```

## Contributing ##

Read through the [Contribution Guidelines](CONTRIBUTING.md) if you want to contribute to this project.

## License ##

`replace-gh-labels` is licensed under both the [**Mozilla Public License 2.0**](LICENSES/MPL-2.0.txt) AND
the [**Apache License 2.0**](LICENSES/Apache-2.0.txt).  
For more information about copying and licensing, see the [`COPYING.txt`](COPYING.txt) file.
