<p align="center">
    <a href="https://github.com/win98and95/xenia/tree/master-custom/assets/icon">
        <img height="120px" src="https://raw.githubusercontent.com/win98and95/xenia/master-custom/assets/icon/128x128.png" />
    </a>
</p>

<h1 align="center">Xenia - Xbox 360 Emulator</h1>

Xenia is an experimental emulator for the Xbox 360. For more information, see the
[main xenia website](https://xenia.jp/).

**Interested in supporting the core contributors?** Visit
[Xenia Project on Patreon](https://www.patreon.com/xenia_project).

Come chat with us about **emulator-related topics** on [Discord](https://discord.gg/Q9mxZf9).
For developer chat join `#dev` but stay on topic. Lurking is not only fine, but encouraged!
Please check the [frequently asked questions](https://xenia.jp/faq/) page before
asking questions. We've got jobs/lives/etc, so don't expect instant answers.

Discussing illegal activities will get you banned.

## Status

Buildbot | Status
-------- | ------
[Windows](https://dev.azure.com/windows98and95/xenia/_build) | [![Build Status](https://dev.azure.com/windows98and95/xenia/_apis/build/status/illusion98.xenia?branchName=d3d12_custom)](https://dev.azure.com/windows98and95/xenia/_build/latest?definitionId=1&branchName=d3d12_custom) [![Build status](https://ci.appveyor.com/api/projects/status/n3h76k1mik1a8hfo?svg=true)](https://ci.appveyor.com/project/win98and95/xenia)

## Changes

Use BT.709 as the default gamma

Restored old icon

New gflags added:

* `--signin_state` - User profile signed in
  * Values:
    * `1` = Signed in *(default)*
    * `0` = Signed out

* `--license_mask` - Set license for XBLA games.
  * Values:
    * `0` = Trial/demo *(default)*
    * `1` = Activated/full

* `--language` - Changes language
  <details><summary>Values (click to expand list)</summary>
  <p>

  * `1` = ENGLISH *(default)*
  * `2` = JAPANESE
  * `3` = GERMAN
  * `4` = FRENCH
  * `5` = SPANISH
  * `6` = ITALIAN
  * `7` = KOREAN
  * `8` = TCHINESE
  * `9`= PORTUGUESE
  * `10` = SCHINESE
  * `11` = TCHINESE
  * `12` = POLISH
  * `13` = RUSSIAN
  * `14` = CZECH
  * `15` = DUTCH
  * `16` = NORWEGIAN
  </p>
  </details>

Thanks to [theTwist84](https://github.com/theTwist84) and [Prism019](https://github.com/Prism019) for the help!

## Compatibility

Quite a few real games run. Quite a few don't.
See the [Game compatibility list](https://github.com/xenia-project/game-compatibility/issues)
for currently tracked games, and feel free to contribute your own updates,
screenshots, and information there following the [existing conventions](https://github.com/xenia-project/game-compatibility/blob/master/README.md).

## Disclaimer

The goal of this project is to experiment, research, and educate on the topic
of emulation of modern devices and operating systems. **It is not for enabling
illegal activity**. All information is obtained via reverse engineering of
legally purchased devices and games and information made public on the internet
(you'd be surprised what's indexed on Google...).

## Quickstart

With Windows 8+, Python 3.4+, and [Visual Studio 2017 or 2019](https://www.visualstudio.com/downloads/) and the Windows SDKs installed:

    > git clone https://github.com/xenia-project/xenia.git
    > cd xenia
    > xb setup

    # Pull latest changes, rebase, and update submodules and premake:
    > xb pull

    # Build on command line:
    > xb build

    # Run premake and open Visual Studio (run the 'xenia-app' project):
    > xb devenv

    # Run premake to update the sln/vcproj's:
    > xb premake

    # Format code to the style guide:
    > xb format

When fetching updates use `xb pull` to automatically fetch everything and
run premake for project files/etc.

## Building

See [building.md](docs/building.md) for setup and information about the
`xb` script. When writing code, check the [style guide](docs/style_guide.md)
and be sure to run clang-format!

## Contributors Wanted!

Have some spare time, know advanced C++, and want to write an emulator?
Contribute! There's a ton of work that needs to be done, a lot of which
is wide open greenfield fun.

**For general rules and guidelines please see [CONTRIBUTING.md](.github/CONTRIBUTING.md).**

Fixes and optimizations are always welcome (please!), but in addition to
that there are some major work areas still untouched:

* Help work through [missing functionality/bugs in games](https://github.com/xenia-project/xenia/labels/compat)
* Add input drivers for [DualShock4 (PS4) controllers](https://github.com/xenia-project/xenia/issues/60) (or anything else)
* Skilled with Linux? A strong contributor is needed to [help with porting](https://github.com/xenia-project/xenia/labels/cross%20platform)

See more projects [good for contributors](https://github.com/xenia-project/xenia/labels/good%20first%20issue). It's a good idea to ask on Discord and check the issues page before beginning work on
something.

## FAQ

For more see the main [frequently asked questions](https://xenia.jp/faq/) page.

### Can I get an exe?

Check [AppVeyor's artifacts](https://ci.appveyor.com/project/win98and95/xenia/history) to see
what's there.
