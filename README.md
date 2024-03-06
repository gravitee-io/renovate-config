# Gravitee-io - Renovate Config

Here you can define shared renovate presets to be reused later from other repositories 
as described [here](https://docs.renovatebot.com/config-presets/)

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




