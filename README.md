# android-studio-gradle-test
A test project with a structure to stress test and find out issues in Android Studio and Gradle

Also provides an alternative build path using [Buck](https://buckbuild.com/) to compare. For more details on how the buck build path is setup, please see [OkBuck](https://github.com/uber/okbuck)

[![Master branch build status](https://travis-ci.org/kageiit/android-studio-gradle-test.svg?branch=master)](https://travis-ci.org/kageiit/android-studio-gradle-test)

## Setup

Run `./gradlew addSources` to generate source code for all subprojects.

## To build all apps with gradle:
```bash
./buildWithGradle
```

## To build all apps with buck

### Setup
#### Mac OS X
```bash
brew update
brew install ant watchman
```

#### Linux
Installation instructions for: [Ant](http://ant.apache.org/), [Watchman](https://facebook.github.io/watchman/docs/install.html)

### Build
```bash
./buildWithBuck
```

## Benchmarking and profiling (Experimental)

Run `./gradlew addSources` to generate source code for all subprojects.

Use the Gradle profiler to `--benchmark` or `--profile` scenarios. The available scenarios are defined in `performance.scenarios`

Example usage: `./gradle-profiler --profile chrome-trace upToDateSingleVariant`
