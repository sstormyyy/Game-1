#The game "Escape from the Dark Tower"
Legend:
You find yourself in the ancient Tower of Chaos. The architecture of this place
is insane: the floors hang in the void, the corridors are narrowed to a crawl, and
they expand into huge halls.
You have a burning torch in your hand. Your goal is to climb to the top and find
an exit before the light goes out.
The path to freedom is blocked by the Barrier Guardian (X), which can only be
overcome using the unique skill of your class.

Symbols (Map Legend):
• P — Player (Player). Your current position.
• _ — Floor. A free cell where you can take a step.
• # — Wall. An impassable obstacle.
• U (Up) — Entrance to the upper floor. A staircase leading to the next floor. To use it, you need to approach it and interact with it.
• D (Down) — Entrance to the lower floor. A staircase leading to the previous floor. Also is the point of appearance when climbing from below.
• + — Oil. Bonus, restoring the torch charge (+10).
• F — Finish. Exit point (victory).
• X — Barrier. A special obstacle before the exit (Castle / Blockage / Abyss — depends on the option).

Resource "Torch":
• Enter the variable int torch = 30;.
• Any normal step or staircase (special skills consume more) reduces the charge by 1.
• If the charge is 0 - the game ends with a message that you will have in the option.
• On the map there are symbols + (Oil). If you step on such symbol: torch += 10, and the symbol itself disappears from the map.

Navigation:
• Commands: w, a, s, d (north, west, south, east).
• Stairs (U/D): moving up or down the stairs does not happen automatically. When standing on a stair (U) tile, the player must press the E keyto move to the next floor. The x, y coordinates are saved.
• Interaction (E):
o Moving between floors does not happen automatically when stepping on them.
o To use the stairs, you need to stand next to it (on the neighboring square).
o Enter the command e (enter), then specify the direction to
the stairs.
• Input mode: The game is strictly step-by-step.
• Information panel (HUD): after each step, before the map is drawn, the program must display the status:
o The current floor (for example: Floor 1: Tunnel).
o The player's coordinates (for example: [Y: 2, X: 4]).
o The current torch charge.

Option A: "The Rogue" (The Locksmith)
For you, X is a complex lock that requires fine work.
1. Inventory: your character has lockpicks (boolean hasLockpick =
true) by default.
2. Mechanics:
• Added command K (key/lockpick) + direction.
• If there is an X in the specified direction, you can pick it.
• Cost: picking requires time. The action consumes 5 torch units.
• Result: X turns into a floor, and the path is open.
