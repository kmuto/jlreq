# jlreq

## What is this?
This package provides the class file and JFM (Japanese font metric) files for LuaTeX-ja / pLaTeX / upLaTeX. This aims to implement [Requirements for Japanese Text Layout](https://www.w3.org/TR/jlreq/).

## Installation
Run `make`, then JFM files are created. Move the files as follows:

* *.tfm -> $TEXMF/fonts/tfm/public/jlreq
* *.vf -> $TEXMF/fonts/vf/public/jlreq
* jfm-jlreq.lua jfm-jlreqv.lua -> $TEXMF/tex/luatex/jlreq
* jlreq.cls -> $TEXMF/tex/latex/jlreq

`make install` will do this where $TEXMF=$TEXMFHOME

## Usage
See [README-ja.md](README-ja.md) (in Japanese).

## LICENSE
This package is distributed under the BSD 2-Clause License. See [LICENSE](LICENSE).

## CHANGELOG
* 2017-02-08
    - First release.
* 2017-02-17
    - Fixed bugs.
    - Implement `abstract` environment.
    - Changed/Added some keys to class option/`\jlreqsetup`
    - Stopped to load `pxrubirica`, `luatexja-ruby` and `nidanfloat`.
* 2017-03-14
    - Fixed bugs.
    - `\sffamily` etc. also change the Japanese font family.
    - Added many options to `\DeclareBlockHeading`.
    - Some options related to `quote` environment etc.
* 2017-03-20
    - Fixed bugs.
    - Insert some spaces around `\footnote / \sidenote / \endnote`.
* 2017-04-04
    - Fixed a bug.
    - Added options `tate` and `font` to `\DeclarePageStyle`.
* 2017-04-29
    - Fixed bugs.
    - Added `jafontsize` and `jafontscale` options and `\jafontsize`.
    - Added `\tatechuyoko`.
    - `jlreq_warnings` -> `jlreq_notes` (class option).
    - Moved some class options to `\jlreqsetup`.
    - Added some options to `\jlreqsetup`.
    - `paper={<height>,<width>}` -> `paper={<width>,<height>}`.
* 2017-06-11
    - Stopped to load `plext` and `lltjext`.
    - Added `align` to `\DeclareBlockHeading` and delete `indent=center`, `end_indent=center`.
    - Changed `\kcatcode` for some characters (upLaTeX).
* 2017-08-13
    - Added `column_spanning` to `\DeclareBlockHeading`.
    - Sidenotes are a part of the main text now.
    - Changed the default length of sidenotes to 0.
    - jlreq does not define `\sidenote` if the length for sidenotes is zero.
    - Added a command for the full-width ideographic space.
* 2017-08-29
    - Fixed a bug.
* 2017-11-23
    - Fixed bugs.
    - Added `\SetBlockHeadingSpaces`.
    - Removed a space from `\contentsname` and `\indexname`.
* 2017-12-02
    - Fixed bugs.
* 2017-12-22
    - Improved JFM.
    - Change the way to detect `\label` between block headings.
    - Added chapter number to `\theequation`，`\thefigure`，`\thetable`.



--------------
Noriyuki Abe
https://github.com/abenori/jlreq
