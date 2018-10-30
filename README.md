Compiled version of book "500 Lines or less".

Source code is located in repository https://github.com/aosabook/500lines.git

I had big problems trying to build it under Windows. So I hope you don't need to follow my way.

## How to build PDF on Windows

0. First install [Python 2.7](https://www.python.org/downloads/release/python-2714/) (not the latest Python 3.x, but old version Python 2.7), [MikTex](https://miktex.org/);
1. Make sure folder with `pdflatex.exe` is added to `PATH` variable;
2. Clone repository https://github.com/aosabook/500lines.git;
3. Patch `build.py` script:
    * replace `envy.run` method with `subprocess.call`;
    * replace `cp` command line with Windows analog `copy`;
    * make sure that slash symbols '/' are replaced with backslash '\\' for Windows folders;

  You can take `build_win.py` file from this repo as an example. But I can't guarantee it's 100% working.

4. Run build script with command:
```
python build.py --pdf
```

In the end you'll find result file `output\500L.pdf`.
