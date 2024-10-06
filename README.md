# Debug Buildpack

This is a [Cloud Native Buildpack](https://buildpacks.io/) whose sole purpose is to help debug Buildpacks. It:
 - Lists the CNB_* environment variables
 - Lists the files in the CNB_APP_DIR directory
 - Lists the files in the CNB_PLATFORM_DIR directory
 - Lists the files in the CNB_LAYERS_DIR directory
 - Lists the files in the /cnb directory
 - Lists the files in the CNB_PLATFORM_DIR/env directory
 - Prints the contents of CNB_APP_DIR/Procfile
 - Prints the contents of CNB_LAYERS_DIR/config/metadata.toml
 - Then sleeps for 10 minutes to allow for debugging

## Usage

Add this buildpack to your buildpack order to debug the build process.

Use on [Build.io](https://build.io?utm_source=github&utm_medium=readme&utm_campaign=buildpack-debug):
```
$ bld buildpacks:add https://github.com/buildio/buildpack-debug
```

Or use it with `pack`:
```
$ pack build --buildpack buildio/buildpack-debug myapp
```

## License

MIT

## Disclaimer

This buildpack is experimental and not yet intended for production use.
