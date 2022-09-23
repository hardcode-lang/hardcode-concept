Quoted scripting
================

The ability to implement quoted scripting is built on top of [analyzable sandboxing](analyzable_sanboxing.md) of <b>HardCode</b> programming language.

Mose uses cases are about third party scripts execution.

Here we'll consider quoted scripting application at cybersports, specifically at RTS (Real Time Strategy) genre.

## RTS with quoted scripting

Let us consider the story around StarCraft 2 - undeniable leader of the genre:
1. The game provides a whole lot of ways to both microcontrol units and take advantange of macromechanics.
2. Currently there a lot of hype surrounding games involving bots including neural network based bots.
   Those bots regularly suprise viewers with effective unusual human-inaccessible techniques both at microcontrol and at macromechanics.
3. Some players don't even hesitate to use cheats. But despite the unethicality of using cheats unlike 3D shooter cheats the StarCraft 2 cheats are interresting.

So the gamers would gladly have some sophisticated yet convenient ways to control army and economics.
The primary way to give this flexibility to games would be internal game scripts.
But today there's no programming language capable of providing such things.

Lets consider issues with scripting in Lua (the best language for the task today):
1. There's no way to guarantee that a callback function won't just get stuck.
   One can simply write:
   ```lua
   while true do
   end
   ```
   And that's it. Such a function can't be terminated without killing host process.
2. But even if the function won't stuck there's no way figure out how long will it execute and what resources will that take.
   Will the function mine bitcoins? Will it use some neural network model thus replacing human player with a robot.
3. Functions written in Lua are generally several times slower than in statically typed languages.

The <b>HardCode</b> programming language solve those issues brilliantly:
1. Built-in analyzer will show computational complexity of any compilable function.
2. Not only the function won't be able to execute for too long.
   It just have to comply (at linkage time) quotes declared by the cybersports discipline.
   Those quotes aren't dependent on hardware where the game is executed but are logical metrics made out of a programming language semantics.
3. Performance of such functions may in some cases even beat C.

Thus adding callback scripts is possible for:
- orders to units and buildings
- global orders
- regular events at each frame
- event handlers

Let's consider some scripting applications:
- controlling attack priorities
- controlling army formation while moving and attacking
- splitting heterogeneous army with specified proportions
- controlling workers and army production and building buildings
- switching priorities between building workers and army units
- switching unit formation at zonal attacks (<i>say, splitting marines against fungal growth and psionic storms</i>)
- controlling spellcasters
- controlling run-by's
