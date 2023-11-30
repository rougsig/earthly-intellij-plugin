# earthly-intellij-plugin

IntelliJ plugin for Earthly language support. 

Check the currently released versions [on the JetBrains Marketplace](https://plugins.jetbrains.com/plugin/20392-earthly/versions).

## Features
- [x] Syntax highlighting for Earthfiles
- [ ] Code completion
- [ ] Formatter
- [ ] Commenter
- [ ] Go To Symbol Contributor
- [ ] ... Let us know!

![Darcula theme](documentation/darcula.png)
![Light theme](documentation/light.png)

## Requirements

This plugin is dependent on https://github.com/earthly/earthfile-grammar for syntax.

## Building
The following command generates a `earthly-intellij-plugin-<version>.zip` package in the current directory:
```
earthly +dist [--version=<version>]
```

For local development, this will generate a gradle wrapper (`gradle/`) corresponding to the gradle version used in the build itself:
```
earthly +generate-gradle-wrapper
```

## Signing (requires `earthly-technologies` org membership)
The following command generates a `earthly-intellij-plugin-signed-<version>.zip` package in the current directory:
```
earthly +sign [--version=<version>]
```

## Publishing (requires `earthly-technologies` org membership)
The following command builds, signs and publishes the plugin to the [IntelliJ Marketplace](https://plugins.jetbrains.com/plugin/20392-earthly):
```
earthly --push +publish --version=<version>
```

## Testing
```
earthly +ide
```
