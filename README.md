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

### Controls

[LEFT/RIGHT/UP/DOWN]: Move
[A]: Jump
[B]: Spin Kick
[X]: Take out/throw bomba

[Enter]: Show Menu
[L]: Quit Game
[R]: Reset Game

Controls(Combo Move):

Combo Move Sequence: UP, DOWN, LEFT, LEFT, RIGHT, RIGHT, DOWN, SPIN, DOWN, UP, LEFT, RIGHT, LEFT, DOWN, SPIN, UP, DOWN, JUMP
