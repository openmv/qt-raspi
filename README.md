[![GitHub build](https://github.com/openmv/qt-raspi/actions/workflows/main.yml/badge.svg)](https://github.com/openmv/qt-raspi/actions/workflows/main.yml)
[![GitHub license](https://img.shields.io/github/license/openmv/qt-raspi?label=license%20%E2%9A%96)](https://github.com/openmv/qt-raspi/blob/master/LICENSE)
![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/openmv/qt-raspi?sort=semver)
[![GitHub forks](https://img.shields.io/github/forks/openmv/qt-raspi?color=green)](https://github.com/openmv/qt-raspi/network)
[![GitHub stars](https://img.shields.io/github/stars/openmv/qt-raspi?color=yellow)](https://github.com/openmv/qt-raspi/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/openmv/qt-raspi?color=orange)](https://github.com/openmv/qt-raspi/issues)

<img  width="480" src="https://raw.githubusercontent.com/openmv/openmv-media/master/logos/openmv-logo/logo.png">

# Qt 6 Cross-Compile for Raspberry Pi

This repo contains Qt cross compiled for the Raspberry Pi (64-bit) which you can use to build a Qt application for the Rasberry Pi.

https://wiki.qt.io/Cross-Compile_Qt_6_for_Raspberry_Pi

Note that you need to use:

    wget https://raw.githubusercontent.com/riscv/riscv-poky/master/scripts/sysroot-relativelinks.py
    chmod +x sysroot-relativelinks.py 
    python3 sysroot-relativelinks.py $TARGET_SYSROOT

To fix the symlinks instead of what the guide says for the sysroot image. This repo includes a valid sysroot image that is already fixed.

## Contributing to the project

Contributions are most welcome. If you are interested in contributing to the project, start by creating a fork:

* https://github.com/openmv/qt-raspi.git

Clone the forked qt-raspi repository, and add a remote to the main qt-raspi repository:
```bash
git clone --recursive https://github.com/<username>/qt-raspi.git
git -C qt-raspi remote add upstream https://github.com/openmv/qt-raspi.git
```

Now the repository is ready for pull requests. To send a pull request, create a new feature branch and push it to origin, and use Github to create the pull request from the forked repository to the upstream openmv/qt-raspi repository. For example:
```bash
git checkout -b <some_branch_name>
<commit changes>
git push origin -u <some_branch_name>
```

### Contribution guidelines
Please follow the [best practices](https://developers.google.com/blockly/guides/modify/contribute/write_a_good_pr) when sending pull requests upstream. In general, the pull request should:
* Fix one problem. Don't try to tackle multiple issues at once.
* Split the changes into logical groups using git commits.
* Pull request title should be less than 78 characters, and match this pattern:
  * `<scope>:<1 space><description><.>`
* Commit subject line should be less than 78 characters, and match this pattern:
  * `<scope>:<1 space><description><.>`
