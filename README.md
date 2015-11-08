Here you can download a GTK+ 2 bundle retaining the comaptibility with Windows XP, built with Visual Studio 2013.

It is nothing more than a patched version of the excellent work done by the HexChat team and living at https://github.com/hexchat/gtk-win32

Interesting reading:
* http://blogs.msdn.com/b/vcblog/archive/2012/10/08/windows-xp-targeting-with-c-in-visual-studio-2012.aspx

## Notes
* For the VS solutions, pretty much all that has to be done is changing the platform toolchain to v120_xp
* Only Win32 is addressed, in case you need a 64 bit build, you will at least need to create an equivalent of vcvars32-v120_xp.bat (Based on vcvars64 from your VisualStudio installation)

## GTK+ Bundle

This is the bundle built by us containing all the GTK+ binaries, headers and import libraries. If you just want to use GTK+ for your application and don't want to build it yourself, download this. You will also need the Visual C++ redistributable to be able to run applications that use this bundle.

<table>
    <tr>
        <td>GTK+ bundle</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/vc12/x86/gtk-Win32.7z">32-bit</a></td>
        <td><a href="https://dl.hexchat.net/gtk-win32/vc12/x64/gtk-x64.7z">64-bit</a></td>
    </tr>
    <tr>
        <td><a href="https://www.microsoft.com/en-us/download/details.aspx?id=48145">Microsoft Visual C++ Redistributable Package for Visual Studio 2015</a></td>
        <td>vcredist_x86.exe - 32-bit</a></td>
        <td>vcredist_x64.exe - 64-bit</a></td>
    </tr>
</table>

These are the libraries in the bundle:

<table>
    <tr>
        <td>ATK</td>
        <td>2.18.0</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/atk-2.18.0.tar.xz">Source</a></td>
    </tr>
    <tr>
        <td>Cairo</td>
        <td>1.14.2</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/cairo-1.14.2.tar.xz">Source</a></td>
    </tr>
    <tr>
        <td>Enchant</td>
        <td>1.6.0</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/enchant-1.6.0.tar.gz">Source</a></td>
    </tr>
    <tr>
        <td>Fontconfig</td>
        <td>2.8.0</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/fontconfig-2.8.0.tar.gz">Source</a></td>
    </tr>
    <tr>
        <td>FreeType</td>
        <td>2.6.1</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/freetype-2.6.1.tar.bz2">Source</a></td>
    </tr>
    <tr>
        <td>GDK-PixBuf</td>
        <td>2.32.1</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/gdk-pixbuf-2.32.1.tar.xz">Source</a></td>
    </tr>
    <tr>
        <td>gettext-runtime</td>
        <td>0.18</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/gettext-vc100-0.18-src.tar.bz2">Source</a></td>
    </tr>
    <tr>
        <td>GLib</td>
        <td>2.46.0</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/glib-2.46.0.tar.xz">Source</a></td>
    </tr>
    <tr>
        <td>GTK+</td>
        <td>2.24.28</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/gtk+-2.24.28.tar.xz">Source</a></td>
    </tr>
    <tr>
        <td>HarfBuzz</td>
        <td>1.0.4</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/harfbuzz-1.0.4.tar.bz2">Source</a></td>
    </tr>
    <tr>
        <td>libffi</td>
        <td>3.2.1</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/libffi-3.2.1.tar.gz">Source</a></td>
    </tr>
    <tr>
        <td>libpng</td>
        <td>1.6.18</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/libpng-1.6.18.tar.xz">Source</a></td>
    </tr>
    <tr>
        <td>libxml2</td>
        <td>2.9.2</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/libxml2-2.9.2.tar.gz">Source</a></td>
    </tr>
    <tr>
        <td>OpenSSL</td>
        <td>1.0.2d</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/openssl-1.0.2d.tar.gz">Source</a></td>
    </tr>
    <tr>
        <td>Pango</td>
        <td>1.38.0</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/pango-1.38.0.tar.xz">Source</a></td>
    </tr>
    <tr>
        <td>Pixman</td>
        <td>0.32.8</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/pixman-0.32.8.tar.gz">Source</a></td>
    </tr>
    <tr>
        <td>win-iconv</td>
        <td>0.0.6</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/win-iconv-0.0.6.tar.bz2">Source</a></td>
    </tr>
    <tr>
        <td>zlib</td>
        <td>1.2.8</td>
        <td><a href="https://dl.hexchat.net/gtk-win32/src/zlib-1.2.8.tar.xz">Source</a></td>
    </tr>
</table>


## Building from Source

If you want to build the bundle from source yourself, we have a PowerShell script that will download the sources, apply some patches and run the build. It is largely based on Fan Chun-wei's [Compiling the GTK+ (and Clutter) stack using Visual C++ 2008 and later](https://wiki.gnome.org/action/show/Projects/GTK+/Win32/MSVCCompilationOfGTKStack).

1. Install the following build tools and dependencies:

    * [Visual Studio 2015 Community](http://www.visualstudio.com/downloads/download-visual-studio-vs) - Any version of VS apart from 2015 is not supported.
    * [Windows Management Framework 4.0](https://www.microsoft.com/en-us/download/details.aspx?id=40855) - Not needed for Windows 8.1 and above
    * [CMake 3.0.2](http://www.cmake.org/download/)
    * [msys2](https://msys2.github.io/)
    * Perl 5.20 [x86](https://dl.hexchat.net/misc/perl/perl-5.20.0-x86.7z) or [x64](https://dl.hexchat.net/misc/perl/perl-5.20.0-x64.7z) (extract to _C:\gtk-build\perl-5.20\Win32_ or _C:\gtk-build\perl-5.20\x64_)
    * [Python 2.7](https://www.python.org/downloads/windows/) (install to _C:\gtk-build\python-2.7\Win32_ or _C:\gtk-build\python-2.7\x64_)
    * [msgfmt](https://dl.hexchat.net/gtk-win32/msgfmt-0.18.1.7z) (extract to _C:\gtk-build_ so you have _C:\gtk-build\msgfmt\msgfmt.exe_)
    * [Ragel](https://dl.hexchat.net/gtk-win32/ragel-6.8.7z) (extract to _C:\gtk-build_ so you have _C:\gtk-build\ragel\ragel.exe_)

1. Follow the instructions on the msys2 page to update the core packages.

1. Install needed packages in the msys2 shell

    ```bash
    pacman -S gzip nasm patch tar xz
    ```

1. Clone [this repository](https://github.com/hexchat/gtk-win32) to _C:\gtk-build\github\gtk-win32_ It contains the build script, project files and patches.

1. Now you have to allow PowerShell scripts to be run on your system. Open a PowerShell prompt **as Administrator** and run the following command:

    ```powershell
    Set-ExecutionPolicy RemoteSigned
    ```

1. Now start a new PowerShell window as a regular user. Go to the _gtk-win32_ directory and start building with the script. For example, to build the 32-bit bundle, run:

    ```powershell
    cd C:\gtk-build\github\gtk-win32
    .\build.ps1
    ```

    To build the 64-bit bundle instead, run:

    ```powershell
    cd C:\gtk-build\github\gtk-win32
    .\build.ps1 -Configuration x64
    ```

    The script has some parameters you can pass in. Run

    ```powershell
    Get-Help -Full .\build.ps1
    ```

    to see the help for the parameters and examples.

1. When the script is done, your GTK+ stack will be found under _C:\gtk-build\gtk_. Enjoy!

![GTK+ 2 dependency graph](https://hexchat.github.io/gtk-win32/img/dependency-graph.png)
