# picasso

Feather weight CLI tool for synching Github issue labels across repos.

## Usage

* Create a simple JSON object mapping `name` to `color` (e.g. `labels.example.json`):

**labels.example.json**
``` js
  {
    "bug":         "fc2929",
    "duplicate":   "cccccc",
    "enhancement": "84b6eb",
    "invalid":     "e6e6e6",
    "question":    "cc317c",
    "wontfix":     "ffffff",
    "design":      "6fa35a",
    "development": "0b02e1",
    "regression":  "e10c02",
    "blocked":     "444444",
    "deployed":    "02e10c"
  }
```

* Install and run `picasso`:

```
  npm install picasso -g
  picasso --username [gh-username] --password [gh-password] \
    --repo indexzero/picasso --file labels.json
```

_Watch as the labels are added to your repo:_

```
  $ picasso 
  ƒ. username indexzero
  ƒ. password 
  ƒ. repo indexzero/picasso
  ƒ. label-file labels.example.json
  ⅰ. Listing labels for indexzero/picasso
  ⅰ. Updating bug in indexzero/picasso
  ⅰ. Updating duplicate in indexzero/picasso
  ⅰ. Updating enhancement in indexzero/picasso
  ⅰ. Updating invalid in indexzero/picasso
  ⅰ. Updating question in indexzero/picasso
  ⅰ. Updating wontfix in indexzero/picasso
  ⅰ. Updating design in indexzero/picasso
  ⅰ. Updating development in indexzero/picasso
  ⅰ. Updating regression in indexzero/picasso
  ⅰ. Updating blocked in indexzero/picasso
  ⅰ. Updating deployed in indexzero/picasso
  ⅰ. Done syncing labels with indexzero/picasso
```

## `picasso` uses [frameless](https://github.com/dscape/frameless)

1. Passing `--save` will save all options to `~/picasso.f.json`
2. If any CLI option is not provided you will be prompted for it.

#### LICENSE: MIT
#### Author: [Charlie Robbins](http://nodejitsu.com)