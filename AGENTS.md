# Project Notes

- Open `PathAndLine.slnx` in Visual Studio, or build with `msbuild PathAndLine.slnx /restore /p:Configuration=Release`.
- The VSIX is `PathAndLine/bin/Release/PathAndLine.vsix`. Increment `Version` in `PathAndLine/source.extension.vsixmanifest` before publishing an update.
- The extension targets .NET Framework 4.7.2 and uses Visual Studio's classic AsyncPackage/DTE APIs.
- DTE and clipboard calls must stay on the Visual Studio UI thread. Reset command visibility before checking the active document.
- There are no automated tests; use F5 in Visual Studio to test in an Experimental Instance.