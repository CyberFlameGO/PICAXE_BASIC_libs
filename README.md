# My PICAXE BASIC headerfile libraries

## Instructions for using this
If your project __doesn't__ use Git, clone the repository with `git clone https://github.com/CyberFlameGO/PICAXE_BASIC_libs.git` (HTTPS cloning) or `git clone git@github.com:CyberFlameGO/PICAXE_BASIC_libs.git` (SSH cloning) in your project's directory.
If your project *does* use Git, add this repository as a submodule with `git submodule add https://github.com/CyberFlameGO/PICAXE_BASIC_libs.git` (HTTPS) or `git submodule add git@github.com:CyberFlameGO/PICAXE_BASIC_libs.git` (SSH) in your project root directory.

Once you've done that, include the headerfile/s you're using into your code. You do this by putting this at the top of your BASIC code file:
```basic
#include "<FILE LOCATION EXCLUDING ANGLE BRACKETS>"
```

### Example
#### Scenario
I have a file called `main.bas` in working directory `/Users/cyberflame/Documents/PICAXE/main.bas` and I've run `git submodule add https://github.com/CyberFlameGO/PICAXE_BASIC_libs.git` in `/Users/cyberflame/Documents/PICAXE/`, and I wanted to use `dice_gen(w1, 5, b4)` in my `main.bas` file.

#### How I do this:
```basic
#include "./PICAXE_BASIC_libs/rand_logic.basinc"
;The ./ signifies that the location I'm referencing is relative to where this file's location is

main:
      dice_gen(w1, 6, b4)
      ;w1 is where we store the original random number, 6 is for a number including and between 0 - 5, and b4 is for the new number
      goto main
```
## Confused?
Please submit an [issue](https://github.com/CyberFlameGO/PICAXE_BASIC_libs/issues/new?assignees=CyberFlameGO&labels=question&template=question.yml) outlining what you need clarification on, or drop me an email at [cyberflameu@gmail.com](mailto:cyberflameu@gmail.com). You can take a look at my GitHub profile for other mediums in which you can contact me if none of these satisfy your needs for a means of contact
