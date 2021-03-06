
# event-generator
> Generate a variety of suspect actions that are detected by Falco rulesets.

[![Release](https://img.shields.io/github/release/falcosecurity/event-generator.svg?style=flat-square)](https://github.com/falcosecurity/event-generator/releases/latest)
[![License](https://img.shields.io/github/license/falcosecurity/event-generator?style=flat-square)](LICENSE)
[![Go Report Card](https://goreportcard.com/badge/github.com/falcosecurity/event-generator?style=flat-square)](https://goreportcard.com/report/github.com/falcosecurity/event-generator)
<!-- [![Docker pulls](https://img.shields.io/docker/pulls/falcosecurity/event-generator?style=flat-square)](https://hub.docker.com/r/falcosecurity/event-generator) -->

**Status**: Under development

**Warning** — We strongly recommend that you run the program within Docker (see below), as it modifies files and directories below /bin, /etc, /dev, etc.

## Usage
```
$ make
$ ./event-generator run [regexp]
```
Without arguments it runs all actions, otherwise only those actions matching the given regular expression.

The full command line documentation is [here](./docs/event-generator.md).

## Docker
TODO

## FAQ

### What sample events can be generated by this tool?
See the [events registry](https://github.com/falcosecurity/event-generator/tree/master/events).

### Can I contribute by adding new events?
Sure! 

Check out the [events registry](https://github.com/falcosecurity/event-generator/tree/master/events) conventions, then feel free to open a PR.
Your contribution is highly appreciated.

### Can I use this project as a library?
This project provides three main packages that can be imported and used separately:

- `/cmd` contains the CLI implementation
- `/events` contains the events registry
- `/pkg/runner` contains the actions runner implementations

Feel free to use them as you like on your projects.

## Acknowledgments

Special thanks to @mstemm — the author of the [first event generator](https://github.com/falcosecurity/falco/tree/2126616529e7015ff88653b7491dc1937d7e54e5/docker/event-generator).
