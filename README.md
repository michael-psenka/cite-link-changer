# Citelink

*Cite Link Changer* (`citelink`) is a simple command-line tool that takes academic papers and turns the bibliography citation links into direct web links to the referenced paper. Since academic papers can be packed with outside references, this can speed up background reading tremendously.

## Demo

<p align="center">
  <img src="https://media.giphy.com/media/ycxxEan3ii6bCsY8Ys/giphy.gif" alt="animated" />
</p>

## Installation

Clone the repository locally, then depending on your OS:

### Windows

1. Launch Powershell as an admin.
2. Navigate to this repository's location, then run `.\install_windows.ps1`.

### Mac/Linux
1. <a href="https://www.mono-project.com/download/stable/" target="_blank">Install mono</a>. Make sure you can run mono in your terminal by running `mono --version`; note this may need a restart.
2. In your terminal, navigate to this repository's location, then run `sudo ./install_mono.sh`.

### Additional installation options

If you would like to change either the installation location or the name of the command, you can change these at the top of the appropriate installation script.

## Usage

To convert a PDF, navigate to its directory in your terminal and run the following command:

```sh
citelink
```
This will take the most recently modified PDF in the working directory and convert all citation links in the PDF that point to the bibliography into URLs that take you straight to the paper (Google search `→` click first link).

If you want to convert a different PDF in the working directory, say `mypaper.pdf`, you can pass in a PDF name as an argument:

```sh
citelink mypaper.pdf
```

## Updating
Running the appropriate install script again will simply copy over the contents of either `cite_link_changer_dotnet` or `cite_link_changer_mono` (whichever is appropriate), so simply clone the repository again and run the appropriate installation script. If you changed the command name or install directory, make sure you change back to the same one!
## Editing the code

If you would like to tinker with the main program, I've included both the C# source code and .csproj descriptor for the .NET project. You can build/compile with either `dotnet` or Mono's `mcs`, as long as you've installed the only outside dependency, `itextsharp --version=5.5.13.3`.

Enjoy!

