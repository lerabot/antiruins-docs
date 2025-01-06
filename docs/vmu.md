## 💾 VMU

- *save*
    
    ```lua
    Keep these in mind when you create a new savefile:
    	gameName  - 16 character long.
    	saveName  - 26 character long.
    	descShort - 16 character long.
    	descLong  - 32 character long.
    	saveID    - from 1 to 3.
    	
    You should be able to save just about any Lua table on the VMU.
    ```
    
- *vmu animation*
    
    ```lua
      -- To display images on the VMU, you need to create “animations”. 
      -- These animations can be 1 frame long (static). 
      -- To load multiple frames, they need a number suffix (frame1.bin, frame2.bin, frame3.bin, etc)
      
      local animatation = {
        icon      = {},  -- image data
        cFrame    = 1,   -- current frame displayed
        length    = frameNum or 1,
        speed     = speed or 1,
        priority  = priority or 1,
        active    = false,
        filename  = filename,
    }
    ```
    

| **vmu.checkForVMU()** | Check if there is a valid VMU present. |
| --- | --- |
| **vmu.initSavefile(gameName, saveName, descLong, descShort, saveID)** | [Read the save notes.](https://www.notion.so/ANTIRUINS-Documentation-157fdbfe0b3180b6a7c4d0560fb84742?pvs=21) |
| **vmu.checkForSave(saveID)** | Check if a save file exists with the gameName and saveName specified in the saveID. |
| **vmu.saveGame(saveID, data)** | Save the *data* table in specified saveID. *data* can be any valid Lua Table. |
| **vmu.loadGame(saveID)** | Returns a *data* table from  |
| **vmu.deleteGame(saveID)** |  |
| **vmu.createAnimation(filename, frameNum, speed, priority)** | Returns an *animation*. [Read the vmu animation notes](https://www.notion.so/ANTIRUINS-Documentation-157fdbfe0b3180b6a7c4d0560fb84742?pvs=21). |
| **vmu.setScreen(animation, frame)** | Displays the *frame* (integer) of specified *animation*. |
| **vmu.playAnimation(animation, repeats, clearAfter)** | Displays an animation for repeat number of time. If clearAfter is true, the VMU image will be cleared once the animation is done. |
| **vmu.clearScreen()** | Clears the VMU screen. |
| **vmu.freeAnimation(animation)** | Frees the memory of the animation. |