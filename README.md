# PathOfSpelling

Dictionary file for [Path Of Exile](https://www.pathofexile.com) (PoE), a game by [Grinding Gear Games](https://www.grindinggear.com) (GGG).  Should also work with PoE2.

Includes example [Code Spell Checker](https://cspell.org/) (CSpell) config file.


## Components

| Filename                       | Description
| ------------------------------ | -----------
| [poe-dict.txt](poe-dict.txt) | Words specific to [Path of Exile](https://www.pathofexile.com/).
| [cspell.json](cspell.json) | Example CSpell settings file.

`poe-dict.txt` file format:
* plain-text
* single word per line
* sorted ascending (a-z), case-insensitive
* `LF` terminated
* `UTF-8` encoded


## Installation

Nothing special, you can use `poe-dict.txt` as needed.

### VSCode <sup><sub>(optional)</sub></sup>

* Clone this repo to a local directory parallel to the project you wish to spellcheck such that the relative path `..\PathOfSpelling` is valid.
* Install the [CSpell](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) VSCode extension.
* Add the following lines to `.vscode\settings.json` in your project:
```json
{
  "CSpell.import": [ "../../PathOfSpelling/cspell.json" ],
  "CSpell.language": "en,en-GB"
}
```

### Command-line <sup><sub>(optional)</sub></sup>

* Clone this repo to a local directory parallel to the project you wish to spellcheck such that the relative path `..\PathOfSpelling` is valid.
* Install the [CSpell NPM package](https://www.npmjs.com/package/cspell).

Example:  Run a full scan of a local project, with some helpful options enabled:
```powershell
PS C:\YourProject> cspell --config "..\PathOfSpelling\cspell.json" --relative --show-context --no-progress "**"
```

## Contributing

Contributions of any kind are welcome; please use GitHub's issue system.

## License

[MIT](https://opensource.org/licenses/MIT)
