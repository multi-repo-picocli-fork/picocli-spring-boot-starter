# picocli-spring-boot-starter

A subset of [picocli](https://github.com/remkop/picocli),
forked from upstream commit `10509c0af89aa3254ca14ba90d9b3b7168e57994`. The Git history of retained files is
preserved; filtering rewrites commit IDs.

## Build

This repository depends on [picocli-core](https://github.com/multi-repo-picocli-fork/picocli-core).
Check out each dependency next to this repository:

```text
workspace/
  picocli-core/
  picocli-spring-boot-starter/
```

Install JDK 17 and run from this repository:

```bash
./gradlew clean build --no-daemon
```

On Windows, run `gradlew.bat clean build --no-daemon`.
The checked-in Gradle wrapper downloads Gradle and dependencies on first use.
`settings.gradle` includes each sibling as a Gradle composite build, so Gradle
compiles it from source and uses it in place of its published artifact. Source
changes there are visible here on the next build without publishing anything.
To use checkouts in other locations, pass `-PpicocliCoreDir=<path>`.

The build compiles this repository's modules and the production classes they
depend on, runs this repository's tests, and builds JARs. Core tests run in
picocli-core. Java 17 is the version verified locally and used by CI.
See [build-verification.json](build-verification.json) for the local build results.

## Included source

This repository includes:

- `picocli-spring-boot-starter/`

These modules depend on `info.picocli:picocli`.
Picocli core is not copied here. Build artifacts are in each module's `build/libs/`.

## Documentation and origin

Upstream documentation is in picocli-core's `docs/`.
See [UPSTREAM-README.md](UPSTREAM-README.md) for the original project overview
and [subset.json](subset.json) for the extraction manifest and dependencies.

## License

Apache License 2.0; see [LICENSE](LICENSE). Upstream copyright notices are retained.
