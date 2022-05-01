# FixWeave patch for _Tomato Man Versus Viper Man_ by Greg Gilbert
- Version 2
- Game location: https://museumofzzt.com/file/t/tomato/
- Requires: FixWeave v1.0f or later

This is a replacement for my previous patch for _Tomato Man Versus Viper Man_. It fixes not just the one bug that the previous patch fixed, but at least one bug on all but one board of the game. Among the fixes in this version:

* The title screen is reinitialized to compensate for the fact that the author had opened the editor from the title screen, stopping it in mid-animation, and thus saving the world file would save the title screen at that stage.
* Various objects you must touch, including "scrolls" and doors, are fixed so that you can't activate them over and over again; and bosses cannot be shot over and over again to repeat their hit/death animations.
* "Multiple bosses" scenes will require you to kill all of them to proceed as (likely) intended, rather than just the one specific enemy that calls the door object.
* Some additional ammo is given at various points to compensate for the likelihood of running out of ammo at those points.
* The cyan "ladder" on one board has normals added in place of fakes to prevent wandering away from where you're supposed to walk to enter the next board.
* A board connection issue that prevents completion of the game, caused by a glaring design error, is fixed by opening up a path on the destination board for the player to enter.
* The boss life meters are fixed so that, among other things, you can't break them by shooting the bosses too much.
* The driving battle is made fairer by not activating the enemies until you're actually at the controls, preventing cheap hits. (Alas, not much can be done about your vehicle breaking apart while moving because of how ZZT 3.2 works, but at least every component can shoot--which actually works in your favor since it effectively increases your firing range. :) )
* A possible performance issue on the final board is fixed by removing a fade effect object that does nothing other than run a no-idle loop from not finding any green normals to affect (suggesting the design at the end was originally drawn with them).

Unlike the previous patch, all of the OBJ files that are loaded use code that will work in ZZT 3.2, meaning that any future tool to create patched versions of world files using FixWeave files will produce a world file that works in ZZT 3.2.

\- The Green Herring  
April 30, 2022
