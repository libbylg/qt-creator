Qt Creator 4.15
===============

Qt Creator version 4.15 contains bug fixes and new features.

The most important changes are listed in this document. For a complete list of
changes, see the Git log for the Qt Creator sources that you can check out from
the public Git repository. For example:

    git clone git://code.qt.io/qt-creator/qt-creator.git
    git log --cherry-pick --pretty=oneline origin/4.14..v4.15.0

General
-------

* Added locator filter for global file index on Linux (`locate`) and Windows
  (`Everything`)
* Added option for globally changing base environment for running tools
  (QTCREATORBUG-24852)
* Fixed that `General Messages` pane popped up too often (QTCREATORBUG-24667)

Help
----

* Added shared `Zoom` setting (QTCREATORBUG-23731, QTCREATORBUG-25109,
  QTCREATORBUG-25230)

Editing
-------

* Added action for pasting without auto-formatting (QTCREATORBUG-20887)

### C++

* Added options for generation of getters and setters (QTCREATORBUG-1532)
* Added `Create Constructor` refactoring operation
* Added filtering of `Find Usages` based on access type (QTCREATORBUG-19373)
* Added `Open in Editor` and `Open Type Hierarchy` to context menu on items in
  type hierarchy
* Added highlighting of previous class when navigating in type hierarchy
* Fixed type hierarchy with templates classes and typedefs
* Fixed that `-include` compile option was ignored by code model
  (QTCREATORBUG-20602)
* Fixed highlighting of raw string literals (QTCREATORBUG-16183)
* Fixed issue with declaration and definition matching in presence of macros
  (QTCREATORBUG-24739)
* Fixed issue with struct type alias (QTCREATORBUG-24875)
* Fixed issue with function attributes (QTCREATORBUG-24650, QTCREATORBUG-24636)
* Fixed highlighting in macros with indirection (QTCREATORBUG-21522)
* Fixed highlighting in multi-dimensional arrays (QTCREATORBUG-21534)
* Fixed switching between declaration and definition for custom conversion
  operators (QTCREATORBUG-21168)
* Fixed that fix-its with outdated information could be applied
  (QTCREATORBUG-21818)
* Fixed tooltip for some include directives (QTCREATORBUG-21194)
* Fixed include completion for files with non-standard file extensions
  (QTCREATORBUG-25154)
* Fixed highlighting of comments with continuation lines (QTCREATORBUG-23297)

### QML

* Fixed issues with multiple import paths (QTCREATORBUG-24405)

Projects
--------

* Added `Open Terminal Here` for project nodes (QTCREATORBUG-25107)

### qmake

* Fixed freeze when executable run with `system` call waits for input
  (QTCREATORBUG-25194)

### CMake

* Added support for multiconfig generators (QTCREATORBUG-24984)
* Added filesystem node to project tree (QTCREATORBUG-24677)
* Added `install/strip` and `package` targets (QTCREATORBUG-22047,
  QTCREATORBUG-22620)
* Removed utility targets from CMake target locator filters (QTCREATORBUG-24718)
* Fixed Qt detection when importing builds of Qt6-based projects
  (QTCREATORBUG-25100)
* Fixed importing builds of Qt6 tests (QTBUG-88776)
* Fixed which file is opened for `Open CMake target` locator filter
  (QTCREATORBUG-25166)

### Qbs

* Added Android target ABI selection

### Meson

* Added support for `extra_files` (QTCREATORBUG-24824)
* Added support for custom Meson parameters

Debugging
---------

* Added option to show simple values as text annotations
* Added option to copy selected items from stack view (QTCREATORBUG-24701)
* Added visualization of hit breakpoint in `Breakpoints` view
  (QTCREATORBUG-6999)

Analyzer
--------

### Clang

* Added option for disabling diagnostic types from result list
  (QTCREATORBUG-24852)
* Added support for individual `clazy` check options (QTCREATORBUG-24977)
* Added help link to diagnostic tooltip (QTCREATORBUG-25163)

Version Control Systems
-----------------------

* Added simple commit message verification

Test Integration
----------------

* Added basic support for `ctest` (QTCREATORBUG-23332)

Platforms
---------

### WASM

* Improved handling of Emscripten detection and setup (QTCREATORBUG-23126,
  QTCREATORBUG-23160, QTCREATORBUG-23561, QTCREATORBUG-23741,
  QTCREATORBUG-24814, QTCREATORBUG-24822)
* Fixed ABI detection for Qt 5.15 (QTCREATORBUG-24891)

Credits for these changes go to:
--------------------------------
