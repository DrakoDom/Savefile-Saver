# Savefile Saver

I created this project as a solution to a simple, but annoying problem: Backing up my game savefiles. I wanted to be able to copy all of my saved data from a game, into a folder, where I could then put it onto a USB as a backup. It's certainly possible to do manually, but all of that becomes tedious after a while. So, Savefile Saver was born.

### Currently Supported Titles

* Crusader Kings III
* Cyberpunk 2077
* DARK SOULS III
* DARK SOULS: REMASTERED
* DOOM (2016)
* DOOM Eternal
* Hearts of Iron IV
* Minecraft
* Sekiro: Shadows Die Twice
* The Witcher 3

### Usage Requirements

* Windows 7 =<

*It may be possible to use Windows versions lower than 7, but lesser versions haven't been tested. This may introduce critical bugs that can cause data loss.*

### Development Requirements

* A compiler that supports the Windows API and C++20.

### Installation

You can either download a binary release from the [release](https://github.com/DrakoDom/Savefile-Saver/releases/ "Releases") page, or compile from source.

To compile from source, all you need is the `main.cpp` file, and any compiler that supports the Windows API and C++20. There is no required IDE. You can also use the included `CMakeLists.txt` file if needed.

Now, it is possible to modify this source for use on Linux. This program requires the Windows API so that the %USER% environment variable can be fetched and unicode can be displayed properly. So, to get this program running on a Linux machine, you would need to remove `SetConsoleOutputCP(CP_UTF8)` then modify the use of `std::getenv("USERPROFILE")`, and locate where all of your savefile folders are located.

This would require a lot of work for a very small amount of users. I use Linux myself, but not for gaming. That's why I have Windows. So, I have not explored this route yet. But feel free to do so yourself in a fork of this project.

### Usage

After either downloading the binary release or compiling from source, run the program in the command line with the `--save` command. You should be greeted with some ASCII art, a version number, and a place to input your desired game.

You should then see a confirmation in the terminal saying that your files are now being copied to the `Saved` folder in the program's source directory.

Afterwards, always make sure that the `Saved` folder has been backed up to some sort of USB or external drive. This cannot guarantee that your data won't be lost or stolen. But if your main machine fails, you'll have an external backup of your savefiles.