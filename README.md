# 39659

Running on Self-hosted Renovate(42.27.5) with custom global configuration.


## Current behavior

The `extends` property from the repository-provided config file is not migrated correctly when its type is a simple string.

The specification already specifies the correct type accepted by `extends`, i.e. a string array(https://docs.renovatebot.com/configuration-options/#extends), but there is a migrator(https://github.com/renovatebot/renovate/blob/main/lib/config/migrations/custom/extends-migration.ts) for this, so any logic modify `extends` before the migrator is incorrect.


## Expected behavior

The `extends` property will be correctly migrated from string type to string array.

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/39659
