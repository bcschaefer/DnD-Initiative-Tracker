# D&D Combat Tracker (First Project)

This was my **first ever coding project**, written in **November 2021**.

The goal was to build an **terminal-based Combat Tracker** for *Dungeons & Dragons*.  
I created it because most existing initiative trackers lacked features I wanted.

---

## Features

The tracker includes:

- Initiative order  
- Player and monster HP  
- Buffs, debuffs, and conditions  
- AOE and single-target actions  
- XP calculation based on CR  
- Full round-by-round combat rotation  

---

## File Overview

### **main.py**
Handles:
- Loading character data  
- User prompts  
- Constructing the `Tracker` object  
- Calculating total + individual XP  
- Running the main combat loop  

### **InitiativeTracker.py**
Contains the **`Tracker` class**, which manages:
- Ordering initiative  
- Displaying turn information  
- All combat actions (attacks, heals, adding/removing conditions)  
- AOE vs single-target handling  
- Turn rotation until all monsters are defeated  

---

## Running the Program

Make sure both files are in the same directory:

Run the program from the terminal:

```
python3 main.py
```

Follow the on-screen prompts to:
- Load or manually enter players
- Load or manually enter monsters
- Proceed through combat, round by round
When all monsters are defeated, the program prints:
- Total encounter XP
- XP per player

If you load players/monsters from external files, use the following structure line by line:

Players:
```
Name,Initiative,HP,MaxHP
```
Monsters
```
Name,Initiative,HP,MaxHP,CR
```

## Limitations
As my first project, the code has several heavy errors: 
- Uses global variables
- Heavy reliance on terminal clearing 
- No input validation for certain edge cases
- No persistent saving between sessions

Future Improvements 
- GUI interface and seperating display/logic components 
- File export for combat logs 
- Condition duration tracking 
- Advantage/disadvantage rolls 
- General refactoring 
- Robust error handling 
- Replacing several lists with more applicable data structures
