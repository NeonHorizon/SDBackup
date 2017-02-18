SDBackup
========

- **Description:** SDBackup is a utility for backing up devices such as flash memory cards and hard drives
- **Project Website:** [GitHub](https://github.com/NeonHorizon/SDBackup)
- **Requirements:** An Ubuntu Linux installation or equivalent
- **License:** GPL Version 3

![example](https://raw.githubusercontent.com/NeonHorizon/SDBackup/master/pics/example.png)

###Features
- Simple user interface which negates the need to know which /dev device you are backing up
- Automatically unmounts any filesystems on the device before backing up or restoring
- Visable indication of progress and speed
- Automatically decompresses images when restoring (including support for multiple compression types)
- Automatically compresses images when backing up
- Basic protection against mistakes such as overwriting existing backups, backing up and restoring to the same card at the same time, etc
- Sudo is not needed on the command line, it will request sudo rights when necessary

==

###Installation instructions

Execute the following commands:
```
sudo wget https://raw.githubusercontent.com/NeonHorizon/SDBackup/master/sdbackup -O /usr/bin/sdbackup
sudo wget https://raw.githubusercontent.com/NeonHorizon/SDBackup/master/sdrestore -O /usr/bin/sdrestore
sudo chmod +x /usr/bin/sdbackup /usr/bin/sdrestore
```

(The first time you run sdbackup or sdrestore it will ask to install the extra packages you need)

==

###Usage

Simply type sdbackup followed by a filename to make a backup:
```
sdbackup my_backup
```

Or to make a restore type sdrestore followed by the file you want to restore:
```
sdrestore my_backup.gz
```

For those that know their systems you can also optionally specify the device directly to save waiting for the drive scan:
```
sdbackup my_backup /dev/sdc
sdrestore my_backup.gz /dev/sdc
```

==

###Important

As with any software of this nature, these scripts are capable of causing damage to your data. Please use carefully, the responsibility is yours.

==

###License Information

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program.  If not, see [http://www.gnu.org/licenses/](http://www.gnu.org/licenses/).

==

###Credits
[Daniel Bull](https://google.com/+DanielBull)

