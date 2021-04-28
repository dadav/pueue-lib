# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

- Moved into a stand-alone repository for better maintainability.

## [0.12.3] - 28-04-2021

## Added

- Expand the tilde to the home directory

## [0.12.2] - 30-03-2021

## Changed

- Clippy adjustment: Transform `&PathBuf` to `&Path` in function parameter types.
    This should be reverse-compatible, since `&PathBuf` dereferences to `&Path`.

## [0.12.1] - 09-02-2021

### Added

- `dark_mode` client configuration flag by [Mephistophiles](https://github.com/Mephistophiles)

## [0.12.0] - 04-02-2021

Moved into a stand-alone repository for better maintainability.

### Changed

- Change the packet size from 1.5 Kbyte to 1.4 Kbyte to prevent packet splitting on smaller MTUs.
- Add LOTS of documentation.
- Hide modules that aren't intended for public use.
- Rename `GenericListener` to `Listener` and vice versa.

### Removed

- Remove unused `group_or_default` function.

## [0.11.2] - 01-02-2021

### Changed

- Use `127.0.0.1` instead of `localhost` as default host.
    This prevents any unforseen consequences if somebody deletes the default `localhost` entry from their `/etc/hosts` file.

## [0.11.0] - 18-01-2020

### Fixed

- Don't parse config path, if it's a directory.
- Error with "Couldn't find config at path {:?}" when passing a directory via `--config`.
- Fixed missing newline between tasks in `log` output.
