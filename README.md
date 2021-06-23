# About

**Level Designer Toolkit** (*LDtk*) is a **modern**, **efficient** and **open-source** 2D level editor with a strong focus on user-friendliness.

Links: [Official website](https://ldtk.io/) | [Haxe API (on GitHub)](https://github.com/deepnight/ldtk-haxe-api)

[![GitHub Repo stars](https://img.shields.io/github/stars/deepnight/ldtk?color=%23dca&label=%E2%AD%90)](https://github.com/deepnight/ldtk)
[![GitHub All Releases](https://img.shields.io/github/downloads/deepnight/ldtk/total?color=%2389b&label=Downloads)](https://github.com/deepnight/ldtk/releases/latest)
[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/deepnight/ldtk/test-windows?label=LDtk%20build)](https://github.com/deepnight/ldtk/actions/workflows/test-windows.yml)
[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/deepnight/ldtk-haxe-api/Unit%20tests?label=API%20unit%20tests)](https://github.com/deepnight/ldtk-haxe-api/actions/workflows/unitTests.yml)

# Getting LDtk latest version

Visit [LDtk.io](https://ldtk.io) to get latest version.

# Building from source

## Requirements

 - **[Haxe compiler](https://haxe.org)**: you need an up-to-date and working Haxe install to build LDtk. (Installed manually or using Lix with npm)
 - **[NPM](https://www.npmjs.com/)**: this package manager is used for various install and packaging scripts.

### Installing Haxe libs

Install required haxe libs:
```
haxelib git heaps https://github.com/deepnight/heaps.git

haxelib git hxnodejs https://github.com/HaxeFoundation/hxnodejs.git

haxelib git electron https://github.com/tong/hxelectron.git

haxelib git deepnightLibs https://github.com/deepnight/deepnightLibs.git

haxelib git ldtk-haxe-api https://github.com/deepnight/ldtk-haxe-api.git

haxelib git castle https://github.com/ncannasse/castle.git
```

### Installing Node dependencies

Run the following command in the `app` folder:
```
npm i
```

## Compiling *master* branch

First, from the root of the repo, build the electron **Main**:

```
haxe main.debug.hxml
```

This should create a `app/assets/main.js` file.

Then, build the electron **Renderer**:

```
haxe renderer.debug.hxml
```

This should create `app/assets/js/renderer.js`.

## Compiling another branch

If you want to try a future version of LDtk, you can checkout branches named `dev-x.y.z` where x.y.z is version number.

**IMPORTANT**:
 - these *dev* branches might be unstables, or even broken. Therefore, it's not recommended to use, unless you plan to add or fix something on LDtk.
 - because *dev* branches might change quickly, you will need to update haxelibs often, or run `lix download` for new branches.
 - you will need to switch the *LDtk haxe API* to the **same** branch as LDtk repo. (adapt the branch name below accordingly):

```
haxelib git ldtk-haxe-api https://github.com/deepnight/ldtk-haxe-api.git dev-0.6.0
```

## Running

From a command line in the `app` folder, run:

```
npm run start
```

# Related tools & licences

 - Tileset images: see [README](app/samples/README.md) in samples
 - Haxe: https://haxe.org/
 - Heaps.io: https://heaps.io/
 - Electron: https://www.electronjs.org/
 - JQuery: https://jquery.com
 - MarkedJS: https://github.com/markedjs/marked
 - SVG icons from https://material.io