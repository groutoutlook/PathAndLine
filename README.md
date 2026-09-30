# Copy Path and Line

Visual Studio extension with editor commands to copy a file's full or solution-relative path and location.

## Output

Right-click in a saved file and choose **Copy full path and line number** or **Copy relative path and line number**.

Default output:

```text
C:/project/src/File.cs:14
```

In **Tools > Options > Copy Path and Line > General**, enable **Include column number** for `path:line:column` output. Markdown links and backslash paths are optional settings. Relative paths fall back to the filename when no solution is open or the file is outside the solution.

Default shortcut for **Copy full path and line number**: `Ctrl+W`, then `Ctrl+P`. Change it under **Tools > Options > Environment > Keyboard**.

## Install or update

Build `PathAndLine/PathAndLine.csproj` in Release configuration, then open `PathAndLine/bin/Release/PathAndLine.vsix`. Close Visual Studio before installing. The VSIX Installer offers **Update** when an older version is installed. Increment the manifest version before building a new release.

## Build and debug

Open `PathAndLine.slnx` in Visual Studio 2026 or a supported Visual Studio 2022 release. Build with:

```powershell
msbuild PathAndLine.slnx /restore /p:Configuration=Release
```

Press **F5** in Visual Studio to launch an Experimental Instance for testing. This extension uses .NET Framework 4.7.2 and the classic AsyncPackage/DTE model; command behavior requires a live Visual Studio instance to test.
