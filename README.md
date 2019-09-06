# Guardians_of_Sunshine
Recreation of the Guardians of Sunshine game from Adventure Time
Created by Jamal Ra Davis: https://github.com/Jamal-Ra-Davis/

Note: this is meant to compile for Linux, the Windows Version available here:
https://github.com/Jamal-Ra-Davis/Guardians-of-Sunshine---Win-exe

Adapted to be used on Gameboy Zero and similar projects


### Installation

Update libraries (skip this to save time if yours are up-to-date)
```

sudo apt-get update -y && sudo apt-get upgrade -y

```

Install required support library
```

sudo apt-get install libsdl2-mixer-dev -y

```

Download the game
```

cd ~ && sudo git clone https://github.com/infinitLoop/Guardians_of_Sunshine

```

Install the game
```

cd Guardians_of_Sunshine && sudo make

```

To start/run the game
```

~/Guardians_of_Sunshine/./GuardiansOfSunshine

```

### Installing into EmulationStation

First we need to create a new ROMs folder and a Shell Script inside it that will execute the game:
```
sudo mkdir /home/pi/RetroPie/roms/adventuretime

sudo nano /home/pi/RetroPie/roms/adventuretime/GuardiansOfSunshine.sh

```
Paste the commands to execute into the new file and save it:
```

cd /home/pi/Guardians_of_Sunshine/
sudo ./GuardiansOfSunshine

```

Backup the config so that updates to ES do not overwrite the changes:
```

sudo cp /etc/emulationstation/es_systems.cfg /opt/retropie/configs/all/emulationstation/es_systems.cfg

```

Next we need to add a custom system for the new ROM to the EmulationStation config.
Edit the file:
```

sudo nano ~/.emulationstation/es_systems.cfg

```
and add in the configuration info after the SYSTEMS tag and before the first, existing SYSTEM block:
```

<system>
    <name>adventuretime</name>
    <fullname>Adventure Time Games</fullname>
    <path>/home/pi/RetroPie/roms/adventuretime</path>
    <extension>.sh .SH</extension>
    <command>%ROM%</command>
    <theme>adventuretime</theme>
</system>

```


Note: You will need to add the "adventuretime" System folder to any ES Theme for it to show the System's logo and background.  I've added a theme.xml and gamelist.xml here as examples, along with a background.png, system.png, and a jpg to display for boxart.



In the case of a permissions error on the folder, access to the folder/files may need to get set:
```

sudo chmod -R 777 /home/pi/RetroPie/roms/adventuretime
sudo chmod -R 777 /home/pi/Guardians_of_Sunshine

```


### Game Controls

<b>LEFT|RIGHT|UP|DOWN</b>: Move

<b>A</b>: Jump

<b>B</b>: Spin Kick

<b>X</b>: Take out/throw bomba

<b>Enter/Start</b>: Show Menu

<b>L/Left Bumper</b>: Quit Game

<b>R/Right Bumper</b>: Reset Game

### Combo Move

UP, DOWN, LEFT, LEFT, RIGHT, RIGHT, DOWN, SPIN, DOWN, UP, LEFT, RIGHT, LEFT, DOWN, SPIN, UP, DOWN, JUMP
