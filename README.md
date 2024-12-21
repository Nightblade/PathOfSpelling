# PathOfSpelling

Dictionary file for the [Path Of Exile](https://www.pathofexile.com) (PoE) game by [Grinding Gear Games](https://www.grindinggear.com) (GGG), with example [Code Spell Checker](https://cspell.org/) (CSpell) config file.


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

### VSCode

* Checkout this repo to a directory that shares its parent dir with your project.
* Install the [CSpell](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) extension.
* Add the following lines to `.vscode/settings.json` in your project:
```json
{
  "CSpell.import": [ "../../PathOfSpelling/cspell.json" ],
  "CSpell.language": "en,en-GB"
}
```

### Command-line <sup><sub>(optional)</sub></sup>

* Install the [CSpell NPM package](https://www.npmjs.com/package/cspell).

To run a full scan of a local project, with some helpful options enabled:
```powershell
PS C:\YourProject> cspell --config "..\PathOfSpelling\cspell.json" --relative --show-context --no-progress "**"
```


## License

[MIT](https://opensource.org/licenses/MIT)
