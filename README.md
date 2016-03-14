# Keyboard Layout Converter
A simple python script to convert a Windows .klc keyboard layout to a Linux .xkb file

The python file converts a Windows .klc file (which can be created using the [Microsoft Keyboard Layout Creator](http://msdn.microsoft.com/en-us/goglobal/bb964665.aspx) or [KbdEdit](http://www.kbdedit.com/)) to a .xkb file, which can be used under Linux. Please note that you have to merge the generated content into your /usr/share/X11/xkb/symbols/us file.

I have included an example input file ("US - international - custom - nodeadkeys - greek.klc"), which is a US keyboard layout with German special characters (ä, ö, ü, ß), as well as useful special characters for science (these include mathematical symbols and Greek letters). The symbols that can be accessed with the right-Alt (AltGr) and Shift-right-Alt keys are shown here:

![Keyboard Layout AltGr](LayoutAltGr.png?raw=true)
![Keyboard Layout AltGr Shift](LayoutShftAltGr.png?raw=true)

Further information about linux keymaps can be found here:
* [Karol Stasiak's Blog](https://karols.github.io/blog/2013/11/18/creating-custom-keyboard-layouts-for-linux/)
* [LSDevLinux Wiki](http://linux.lsdev.sil.org/wiki/index.php/Building_an_XKB_Keyboard) - thanks also for some ideas for [regular expressions](http://linux.lsdev.sil.org/wiki/index.php/Conversion_from_Microsoft_KLC).

