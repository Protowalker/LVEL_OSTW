# LiveVarEditLib (LVEL) for ItsDeltin's Overwatch Script To Workshop
This is a library that makes it incredibly simple to add a menu for changing variables in-game.

To use it in your code, simply drop it into the same folder as your other files and import it in! VariableMenuExample.del shows all of the functions and how to use them.

## How To Use
In your code, you'll have to set up the toggle action yourself; in the VariableMenu example, for instance, the menu is set to toggle on and off when the host presses crouch and interact:

```//Create a rule to define when the UI will turn on and off.
rule:"Toggle UI"
Event.OngoingPlayer
if(EventPlayer() == HostPlayer())
if(IsButtonHeld(EventPlayer(), Button.Crouch) && IsButtonHeld(EventPlayer(), Button.Interact)){
    //Call the ToggleUI function in order to open or close the UI
    ToggleUI();
}
```


(This has been made open-ended so that the user can define their own combinations so as not to conflict with any existing custom code.)

When in the menu, however, the controls are always the same: move up and down with whatever you have mapped to forward and backward, and change the value with whatever you have mapped to left and right.

The value will change by the small interval you set in the CreateMenuOption function by default, and when holding Ability 1 it will change by the big interval.


## Roadmap
- [ ] Vector Editing Support
- [ ] Support for multiple admins
- [ ] Support for pre-set lists, such as of strings, heroes or icons