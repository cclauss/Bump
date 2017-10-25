SublimeBump
=============

A package allows to manage [npm](https://npmjs.com) and [yarn](https://yarnpkg.com) dependencies easily.
Inspired by the vscode feature, but was rethought and enhanced.

For now, it allows:

- Show **latest** released package version.

- Show **next** (alpha, beta, etc) package version.

- Format to **latest** or **next** version from the editor view.

- Use custom registries.

- Customize tooltip for your needs and taste.


![Demo of latest usage](https://raw.githubusercontent.com/yavorsky/SublimeBump/master/img/next-demo.png)

  ​
## Installation

The easiest and recommended way to install JsPrettier is using [Package Control](https://packagecontrol.io/packages/JsPrettier).

From the **main application menu**, navigate to:

`Tools` -> `Command Palette...` -> `Package Control: Install Package`, type the word **SublimeBump**, then select it to complete the installation.


## Usage

Just install the package and focus the line with dependency in `package.json`. SublimeBump will preview latest or next version (according to the distribution mode) of the package in the bottombar or with the tooltip.


## Settings

Many options are customizable from the **Command Palette** (super + shift + p) and type **SublimeBump**.

#### distribution_mode

Type: *String*, Default: `latest`

Command: `Choose distribution mode`.

Currently, SublimeBump supports `latest` and `next` distribution tags. By default, the `latest` tag is used by npm to identify the current version of a package. The `next` tag is used by some projects to identify the upcoming version (alpha, beta, etc). 

With `next` mode, package trying to fetch latest version, and if no one was registered, it fallbacks to the `latest` version.


#### tooltip

Type: *Boolean*, Default: `true`

Whether or not show tooltip near the cursor. If tooltip is disabled, the version would be displayed in the botombar.


#### dependency_fields

Type: *Array*, Default: `["dependencies", "devDependencies", "peerDependencies"]`

Field name, where SublimeBump will search and show latest version for current package.


#### supported_filenames

Type: *Array*, Default: `["package.json"]`

Name of the files when SublimeBump will watch out for your cursor. We haven't universal parser for all formats, but with json files it does its work.


## Key Bindings

SublimeBump has pre-defined keyboard shortcuts. For now, it format package value on the line with the cursor.

| Command          | Linux & Windows | MacOS          |
| ---------------- | --------------- | -------------- |
| Format to latest | CTRL + K + ,    | CTRL + CMD + , |
| Format to next   | CTRL + K + .    | CTRL + CMD + . |


## License

SublimeBump is released under the MIT License.

Copyright (c) 2017 Artem Yavorsky.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
