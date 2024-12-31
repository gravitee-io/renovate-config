# Gravitee-io - Renovate Config

Shared [renovate presets](https://docs.renovatebot.com/config-presets/) used by Gravitee.io repositories.

[Slab page](https://gravitee.slab.com/posts/renovate-keeping-up-to-date-gz65c5er)

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

## Available presets

- `default`: Default preset for all Gravitee.io repositories.
- `lib`: Base preset for Gravitee.io library repositories.
- `plugin`: Base preset for any Gravitee.io plugin repositories (policy, reporter, endpoint, entrypoint...).
- <del>`policy`: Base preset for Gravitee.io policy repositories.</del> Use `plugin` instead
- <del>`reporter`: Base preset for Gravitee.io reporter repositories.</del> Use `plugin` instead
- `federationagent`: Base preset for Gravitee.io Federation Agent repositories.
