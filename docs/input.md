# 🎮 INPUT

## Button names
    
        local buttons = {"A", "B", "X", "Y", "UP", "DOWN", "LEFT", "RIGHT", "START"}

---

        input.getButton(button, controllerNumber)
Returns true/false if *button* has been pressed.


---
`input.getButtonDown(button, *controllerNumber*)`
: Returns true/false if *button* is being held.
---
`input.getJoystick(*controllerNumber*)`
: Returns the joystick position as a *vector.*
---
`input.getTriggers(*controllerNumber*)`
: Returns both triggers as a *vector.*