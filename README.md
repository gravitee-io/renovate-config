# Gravitee-io - Renovate Config

Shared [renovate presets](https://docs.renovatebot.com/config-presets/) used by Gravitee.io repositories.

## Defining presets

To define a `lib` presets, add a `lib.json` file to this repository.

```json
{
    "extends": ["config:base", "schedule:earlyMondays"],
    "prConcurrentLimit": 3,
    "rebaseWhen": "conflicted",
    "packageRules": [
        {
            "matchDatasources": ["orb"],
            "rangeStrategy": "replace"
        }
    ]
}
```

## Using presets

To reuse the lib preset just define your `.github/renovate.json` file as follows.

```json
{
  "extends": ["github>gravitee-io/renovate-config:lib"]
}
```




