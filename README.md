# rai.tv-bash-dl
Rai.tv bash download script.

Created by [Daniil Gentili](http://daniil.eu.org), this script uses [Andrea Lazzarotto](http://andrealazzarotto.com/)'s [server](http://video.lazza.dk) to decode URLs.

This script can be used to download videos from the Italian [Rai](http://rai.tv) Television website.

This script can be installed on [any Linux/Unix system](#Any-Linux/Unix-system-(Ubuntu,-Debian,-Fedora-Redhat,-openBSD,-Mac OS X)) including [Android](#android), [Mac OS X](#Any-Linux/Unix-system-(Ubuntu,-Debian,-Fedora-Redhat,-openBSD,-Mac OS X)) or [iOS](#iOS)) and even on [Windows](#Windows)!
And for every other platform there's the [web version](http://daniil.eu.org/rai.php) that you can use directly from [here](http://daniil.eu.org/rai.php) or [install on your own server](#installation-on-a-web-server).

## Usage:
```
rai.sh [ -af [ urls.txt ] ] URL URL2 URL3 ...
```

Options:

-a	Automatic mode: quietly downloads every video in maximum mp4 quality.

-f	Reads URLs from specified text file(s).

--help	Shows this extremely helpful message.

## Installation instructions:

### Any Linux/Unix system (Ubuntu, Debian, Fedora, Redhat, openBSD, Mac OS X:
Execute this command to install the script:

```
wget https://github.com/danog/rai-bash-dl/raw/master/rai.sh -O rai.sh && chmod +x rai.sh
```

Run with 
```
./rai.sh URL
```
In the directory where you downloaded it.

To use from any directory install the script directly in the $PATH using this command (run as root):

```
wget https://github.com/danog/rai-bash-dl/raw/master/rai.sh -O /usr/bin/rai.sh && chmod +x /usr/bin/rai.sh
```

Now you should be able to run the script simply with:
```
rai.sh URL
```



### Android:
#### 1. Install [Busybox](https://play.google.com/store/apps/details?id=stericson.busybox), [Jackpal's Terminal emulator](https://play.google.com/store/apps/details?id=jackpal.androidterm) and [Bash](https://play.google.com/store/apps/details?id=com.bitcubate.android.bash.installer). Root is not mandatory.

#### 2. Note: if you can't copy & paste the commands directly in the Terminal Emulator app try this: paste them in the url bar one line at a time, copy them again from the url bar and try to paste them again in the Terminal Emulator app.
Run these commands:
```
cd sdcard && wget http://daniilgentili.magix.net/android/rai.sh 
```

Run with:
```
bash /sdcard/rai.sh URL
```

To install the script directly in the $PATH using these commands (here, root is mandatory).


```
su
mount -o rw,remount /system && wget http://daniilgentili.magix.net/android/rai.sh -O /system/bin/rai.sh && chmod 755 /system/bin/rai.sh
```

And run with:
```
rai.sh URL
```

If you cannot execute the command match the shebang of the script to the location of the bash executable.

### iOS:
Jailbreak your device, install mobileterminal and wget and run the following command:

```
wget http://daniilgentili.magix.net/rai.sh -O rai.sh && chmod 777 rai.sh
```

Run with:
```
./rai.sh URL
```
In the directory where you downloaded it.

To view the downloaded video use iFile. 

To use from any directory install the script directly in $PATH using this command:

```
su -c "wget http://daniilgentili.magix.net/rai.sh -O /usr/bin/rai.sh && chmod 777 /usr/bin/rai.sh"
```

And run with:
```
rai.sh URL
```


### Windows:
Install [Unxutils](http://unxutils.sourceforge.net/) and [win-bash](http://win-bash.sourceforge.net/), open up the command prompt and type:

```
wget http://daniilgentili.magix.net/win/rai.sh -O rai.sh
```

Run with:
```
bash rai.sh
```
In the directory where you downloaded it.

To run the script from any directory run the following commands:

```
bash
cd / && echo "export PATH="$PATH:/rai/"" >>.bashrc && mkdir rai && cd rai && wget http://daniilgentili.magix.net/win/rai.sh -O rai.sh
```


And run with:
```
bash
rai.sh URL
```

### Installation on a web server.
To use this script from any platform you can use the web version that you can find [here](http://daniil.eu.org/rai.php) or install it on your own Linux/Unix web server.
To do this, install php, download [this file](https://github.com/danog/rai.tv-bash-dl/rai.php) and place it in any subdirectory of the www directory. Then navigate to the appropriate page and download away!
Note that shell_exec must be enabled in order for this script to work.

That's it!

Enjoy!

[Daniil Gentili](http://daniil.eu.org/lol)
