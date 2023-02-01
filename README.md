# df-roleplay-events
Idea for a dfhack+lua mod: roleplay events in fortress mode. It should work as follows:

1. Player selects a dwarf(source dwarf). His id is persistently saved somewhere.
2. Huge JSON with random events is loaded. (./event-list.json)
3. Every N days we find a random dwarf in the source dwarf proximity (target dwarf)
4. Every event has a list of conditions (expressions with predefined lua functions). Script randomly shuffles events then finds first event with every condition met for the source and target.
5. before_event lua functions are called.
6. Option window is shown to the player. Some options lead to new events, some options do nothing, some options make skill checks against other dwarves.
