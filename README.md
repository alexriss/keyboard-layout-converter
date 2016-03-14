# Keyboard Layout Converter
A simple python script to convert a Windows .klc keyboard layout to a Linux .xkb file

The python file converts a Windows .klc file (which can be created using the [Microsoft Keyboard Layout Creator](http://msdn.microsoft.com/en-us/goglobal/bb964665.aspx) or [KbdEdit](http://www.kbdedit.com/)) to a .xkb file, which can be used under Linux. Please note that you have to merge the generated content into your /usr/share/X11/xkb/symbols/us file.

Released under the GNU General Public License version 3.

I have included an example input file ("US - international - custom - nodeadkeys - greek.klc"), which is a US keyboard layout with German special characters (ä, ö, ü, ß), as well as useful special characters for science (these include mathematical symbols and Greek letters). The symbols that can be accessed with the right-Alt (AltGr) and Shift-right-Alt keys are shown here:

![Keyboard Layout AltGr](LayoutAltGr.png?raw=true)
![Keyboard Layout AltGr Shift](LayoutShftAltGr.png?raw=true)


## Usage

1. (optional) Generate your own keymap using [Microsoft Keyboard Layout Creator](http://msdn.microsoft.com/en-us/goglobal/bb964665.aspx) or [KbdEdit](http://www.kbdedit.com/)).
2. Edit the script "convert_to_xkb.py": the variables "input" and "ouptout" reflect the filenames of the input .klc and output .xkb files, respectively.
3. Run the script.
4. Merge the generated output (which is in the output file) into your /usr/share/X11/xkb/symbols/us file (see links below for more info).
5. Adjust the /usr/share/xkb/rules/evdev.xml file accordingly (see links below for more info).
6. Use your new keymap and enjoy your new level of productivity.

Further information about linux keymaps can be found here:
* [Karol Stasiak's Blog](https://karols.github.io/blog/2013/11/18/creating-custom-keyboard-layouts-for-linux/)
* [LSDevLinux Wiki](http://linux.lsdev.sil.org/wiki/index.php/Building_an_XKB_Keyboard) - thanks also for some ideas for [regular expressions](http://linux.lsdev.sil.org/wiki/index.php/Conversion_from_Microsoft_KLC).


## Alternative Usage

As an alternative - if you do not want to mess around with the script and just want to use my keyboard map under Linux - I have uploaded my /usr/share/X11/xkb/symbols/us (usr_share_X11_xkb_symbols_us) and /usr/share/xkb/rules/evdev.xml (usr_share_X11_xkb_rules_evdev.xml) files. You can just copy these to make the keyboard layout "English (US) (English (US, symbols and Greek letters))" available.



