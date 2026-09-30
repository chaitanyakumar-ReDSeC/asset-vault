<h1 align="center"> PyInstaller Commands </h1>

## Base Command
```bash
pyinstaller -{flags} {script.py}
```

## Flags
### Basic Bundling
- Create a single executable file (dist/app.exe)
```bash
--onefile
```
```bash
-F
```

- Create a folder with an exe and dependencies (Default)
```bash
--onedir
```
```bash
-D
```

- Rename the output executable and .spec file
```bash
--name "App Name"
```
```bash
-n
```

### Windows / GUI Options
- Hide the terminal/command prompt window on launch
```bash
--noconsole 
```
```bash
-w
```

- Apply a custom .ico file to the executable
```bash
--icon="icon.ico"
```
```bash
-i
```

- Add Windows File Properties (Version, Company, etc.)
```bash
--version-file="v.txt"
```

### Include External Files
- Include extra files (e.g., "ffmpeg.exe;.") 
> Note: Use ";" on Windows, ":" on Linux/Mac
```bash
--add-data "src;dest"
```

### Cleanup and Overwriting
- Clear PyInstaller cache and remove temporary files
```bash
--clean
```

- Overwrite the 'dist' and 'build' folders without asking
```bash
--noconfirm
```
```bash
-y
```

- Where to put temporary 'build' files
```bash
--workpath "path"
```

- Where to put the final 'dist' executable
```bash
--distpath "path"
```

### Advanced and Debugging
- Force include a module PyInstaller missed
```bash
--hidden-import "mod"
```

- Grab all data/metadata for a specific package
```bash
--collect-all "pkg" 
```

- See exactly what's happening if the build fails
```bash
--log-level "DEBUG"
```