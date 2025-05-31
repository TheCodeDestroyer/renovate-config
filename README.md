# Shareable Renovate Config

This repository offers shareable Renovate configurations. It includes a base configuration and two presets (`default.json` and `fast.json`) that extend it.

- **`base.json`**: Core Renovate configuration with recommended settings, automerging for linters and minor updates, lock file maintenance, and a 3-day minimum release age for npm packages. This is not meant to be used directly, but rather extended by other configurations.
- **`default.json`**: Extends `base.json`. Includes an hourly PR limit of 1 and a concurrent branch limit of 3. This is the recommended configuration for most projects.
- **`fast.json`**: Extends `base.json`. Includes a concurrent branch limit of 5. Use this if you need a higher throughput of PRs.

## Installation

To use these configurations in your project, add one of them to your Renovate configuration file (e.g., `renovate.json` or `.github/renovate.json`).

1. **Using the `default` configuration** (recommended for most users):

   ```json
   {
     "extends": ["github>thecodedestroyer/renovate-config"]
   }
   ```

   Renovate will automatically look for `default.json` in this location.

2. **Explicitly specifying a configuration file**:
   Choose the configuration that best suits your needs:
   ```json
   {
     "extends": [
       "github>thecodedestroyer/renovate-config//default.json"
     ]
   }
   ```
   or
   ```json
   {
     "extends": [
       "github>thecodedestroyer/renovate-config//fast.json"
     ]
   }
   ```

   You can also extend the `base.json` directly if you want to create a custom configuration:
   ```json
   {
     "extends": [
       "github>thecodedestroyer/renovate-config//base.json"
     ],
     // Add your custom rules here
   }
   ```

## Features

### Common Features (from `base.json`)

- Recommended base settings from Renovate (`config:recommended`)
- Automatic merging for linters (`:automergeLinters`)
- Automatic merging for minor updates (`:automergeMinor`)
- Semantic commit messages for Renovate PRs (`:semanticCommits`)
- Automatic labeling of PRs with `dependencies` (`:label(dependencies)`)
- Lock file maintenance (enabled and automerged)
- 3-day minimum release age for npm packages
- Configuration migration enabled

### `default.json` Specific Features

- Extends `base.json`
- Hourly PR limit of 1 (`:prHourlyLimit1`)
- Concurrent branch limit of 3

### `fast.json` Specific Features

- Extends `base.json`
- Concurrent branch limit of 5

## License

MIT © [Nace Logar](https://thecodedestroyer.com)
