<!-- Autogenerated from composer.json - All changes will be overridden if generated again! -->

# srag/auto_version_tag_ci Library

Auto create version tag gitlab ci on merge `develop` to `master`, among other things

This is an OpenSource project by studer + raimann ag, CH-Burgdorf (https://studer-raimann.ch)

This project is licensed under the GPL-3.0-only license

## Description

Auto run the follow tasks on merge `develop` to `master` (gitlab ci)

- Auto create version tag
    - Version from `composer.json`|`package.json` > `version`
    - Changelog from `CHANGELOG.md`
- Auto update gitlab and github project description, topics and homepage
    - Short description from `composer.json`|`package.json` > `description`
    - Topics from `composer.json`|`package.json` > `keywords`
    - Homepage from `composer.json`|`package.json` > `homepage`
- Auto recreate gitlab pull request `develop` to `master`
    - Assigned user is first maintainer in gitlab project members

## Usage

### `.gitlab-ci.yml`

```yaml
include:
  - https://plugins.studer-raimann.ch/Customizing/global/auto_version_tag_ci/build/auto_version_tag_ci.yml
```

### CI variables

Set `AUTO_VERSION_TAG_TOKEN` ci variable, protected and masked

Set `AUTO_VERSION_TAG_TOKEN_GITHUB` ci variable (`user:token`), protected and masked

## Requirements

* PHP >=7.4

## Adjustment suggestions

You can report bugs or suggestions at https://plugins.studer-raimann.ch/goto.php?target=uihk_srsu_LAVTCI

There is no guarantee this can be fixed or implemented
