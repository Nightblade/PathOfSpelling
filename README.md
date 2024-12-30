# PathOfSpelling

Dictionary file for [Path Of Exile](https://www.pathofexile.com) (PoE) 1 & 2, by [Grinding Gear Games](https://www.grindinggear.com) (GGG).

Includes example [Code Spell Checker](https://cspell.org/) (CSpell) config file.


## Components

| Filename                       | Description
| ------------------------------ | -----------
| [poe-dict.txt](poe-dict.txt) | Words specific to [Path of Exile](https://www.pathofexile.com/) 1 & 2.
| [cspell.json](cspell.json) | Example minimal CSpell settings file for VSCode.

`poe-dict.txt` file format:
* plain-text
* single word per line
* sorted ascending (a-z), case-insensitive
* `LF` terminated
* `UTF-8` encoded


## Installation

There are no special installation instructions; it's a flat text file.

### <sup><sub>(optional)</sub></sup> VSCode spell-checking with CSpell 

* Requirements: [CSpell](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) VSCode extension.
* Clone this repo to a local directory parallel to the project you wish to spellcheck, such that the relative path `..\PathOfSpelling` is valid.
* Add the following lines to `.vscode\settings.json` in your project:
```json
{
  "CSpell.import": [ "../../PathOfSpelling/cspell.json" ],
  "CSpell.language": "en,en-GB"
}
```

### <sup><sub>(optional)</sub></sup> Command-line spell-checking with CSpell

* Requirements: [CSpell NPM package](https://www.npmjs.com/package/cspell).
* Clone this repo to a local directory parallel to the project you wish to spellcheck, such that the relative path `..\PathOfSpelling` is valid.

Example:  To run a full scan of a local project with some helpful options enabled:
```powershell
PS C:\YourProject> cspell --config "..\PathOfSpelling\cspell.json" --relative --show-context --no-progress "**"
```

## Contributing

Contributions of any kind are welcome; please use GitHub's issue system.

## License

[MIT](https://opensource.org/licenses/MIT)
