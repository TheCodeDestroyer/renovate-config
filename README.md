# Shareable Renovate Config

This package provides a shareable Renovate configuration. This configuration is designed for general use in any project to help ensure consistency and apply best practices for dependency updates.

## Installation

To use this configuration in your project, add it to your Renovate configuration file (e.g., `renovate.json` or `.github/renovate.json`). You can reference it in two ways:

1. **Using the default file** (recommended):

   ```json
   {
     "extends": ["github>thecodedestroyer/renovate-config"]
   }
   ```

   Renovate will automatically look for `default.json` in this location.

2. **Explicitly specifying the file**:
   ```json
   {
     "extends": [
       "github>thecodedestroyer/renovate-config//default.json"
     ]
   }
   ```

## Features

The configuration includes:

- Recommended base settings
- Automatic merging for linters and minor updates
- Branch automerging
- Lock file maintenance
- 3-day minimum release age for npm packages
- Hourly PR limit of 1
- Concurrent branch limit of 3

## License

MIT © [Nace Logar](https://thecodedestroyer.com)
