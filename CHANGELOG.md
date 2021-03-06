# Change Log
This project adheres to [Semantic Versioning](http://semver.org/).

This CHANGELOG follows the format listed [here](https://github.com/sensu-plugins/community/blob/master/HOW_WE_CHANGELOG.md)

## [Unreleased]
### Breaking Changes
- Bump `sensu-plugin` dependency from `~> 1.2` to `~> 4.0` you can read the changelog entries for [4.0](https://github.com/sensu-plugins/sensu-plugin/blob/master/CHANGELOG.md#400---2018-02-17), [3.0](https://github.com/sensu-plugins/sensu-plugin/blob/master/CHANGELOG.md#300---2018-12-04), and [2.0](https://github.com/sensu-plugins/sensu-plugin/blob/master/CHANGELOG.md#v200---2017-03-29)

### Added
- Travis build automation to generate Sensu Asset tarballs that can be used n conjunction with Sensu provided ruby runtime assets and the Bonsai Asset Index
- Require latest sensu-plugin for [Sensu Go support](https://github.com/sensu-plugins/sensu-plugin#sensu-go-enablement)

## [2.1.1] - 2018-05-03
### Fixed
- check-puppet-last-run.rb: fixed issue where `failures` and `restart_failures` were `nil` when `--ignore-failures` was passed by ensuring that they were defined as `0` so that they could be compared. (@bovy89)

## [2.1.0] - 2018-02-16
### Added
- Added options to allow for different age limits when the agent is disabled
- Added a switch to use the new limits so as not to impact current functionality

## [2.0.0] - 2018-01-31
### Security
- updated `rubocop` dependency to `~> 0.51.0` per: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-8418. (@jaredledvina)

### Breaking Changes
- in order to bring in new rubocop dependency we need to drop ruby 2.0 support as it is EOL and aligns with out support policy. (@jaredledvina)

### Changed
- updated changelog guidelines location (@majormoses)

## [1.3.0] - 2017-11-09
### Added
- Testing for Ruby 2.4.1
- `check-puppet-errors.rb`: Added check for Puppet failures (@grem11n)
- `check-puppet-last-run.rb`: Added option for ignoring Puppet failure (@grem11n)

## [1.2.0] - 2017-05-30
### Added
- `check-puppet-last-run.rb`: Added option for reporting failed restarts (@antonidabek)

## [1.1.0] - 2017-01-30
### Added
- `check-puppet-last-run.rb`: Added critical alerting on failures during summary file processing (@grem11n)

### Fixed
- `check-puppet-last-run.rb`: Corrected failure count hash key (@eahola)

## [1.0.0] - 2016-06-21
### Changed
- check-puppet-last-run.rb: Added a formatter method to display time in a more human friendly format. (d m s) ago
- check-puppet-last-run.rb: if the agent is disabled via lock file, display reason (if available)
- Loosened dependency on sensu-plugin from `= 1.2.0` to `~> 1.2.0`
- Updated Rubocop to 0.40, applied auto-correct
- check-puppet-last-run.rb: now returns critical when errors are found in the puppet run

### Removed
- Remove Ruby 1.9.3 support; add Ruby 2.2.0 and 2.3.0 support to test matrix.

## [0.0.2] - 2015-07-14
### Changed
- updated sensu-plugin gem to 1.2.0

## [0.0.1] - 2015-07-04
### Added
- initial release

[Unreleased]: https://github.com/sensu-plugins/sensu-plugins-puppet/compare/2.1.1...HEAD
[2.1.1]: https://github.com/sensu-plugins/sensu-plugins-puppet/compare/2.1.0...2.1.1
[2.1.0]: https://github.com/sensu-plugins/sensu-plugins-puppet/compare/2.0.0...2.1.0
[2.0.0]: https://github.com/sensu-plugins/sensu-plugins-puppet/compare/1.3.0...2.0.0
[1.3.0]: https://github.com/sensu-plugins/sensu-plugins-puppet/compare/1.2.0...1.3.0
[1.2.0]: https://github.com/sensu-plugins/sensu-plugins-puppet/compare/1.1.0...1.2.0
[1.1.0]: https://github.com/sensu-plugins/sensu-plugins-puppet/compare/1.0.0...1.1.0
[1.0.0]: https://github.com/sensu-plugins/sensu-plugins-puppet/compare/0.0.2...1.0.0
[0.0.2]: https://github.com/sensu-plugins/sensu-plugins-puppet/compare/0.0.1...0.0.2
