# FixWeave patch for "Oreo the Hamster"
- Game location: https://museumofzzt.com/file/o/oreo/
- Requires: FixWeave v1.0e or later

This is a patch collection which, while maintaining the appearance and dialog of the original game, makes an extensive number of changes and bugfixes:

* The standard enemy characters will not place red fakes during their deaths in any direction where they are blocked, preventing them from destroying the environment and each other.
* The cutscenes' "skip movie" objects will disappear automatically once the cutscenes are complete, rather than waiting for the player to touch them.
* The cutscenes that feature multiple lines in a sequence are slowed down so the player can more easily read them.
* The player can no longer collect an infinite number of "5 pennies" from under the bed. (You never use them during the game, but still.)
* The mice at the furthest end of the bed who die on touch will now also die when shot like the others.
* The final boss has been refactored to be fairer to the player, prevent turrets from shooting one another, and add a proper death sequence on par with the rest of the game.
* The intended last lines of the game, hidden by a programming mistake, are now shown.
* The ending board now properly ends the game after it finishes.

There are some additional patches made due to fixes within the Weave engine itself:

* The "#become yellow fake" command in the opening scroll that crashes ZZT 3.2 does not crash Weave, but Weave's improved parser, which accepts numbers in commands and labels, will interpret the "#1", "#2", etc. as sends to ":1", ":2", etc. labels and flash an error message as a result. This is fixed by removing the hashes to make the text display the way it does in ZZT 3.2.
* The game's numerous "#put <dir> red fake" commands were changed to "#put <dir> red black fake" commands to emulate ZZT 3.2 behavior. By default, in Weave, placing a fake without a background color will inherit it from the tile it's placed on, which, while having better-looking results, would look strikingly out of place in this game. :)

Finally, there is an optional "challenge" config file (in the "challenge" folder) which prevents the object enemies from shooting and hurting one another, potentially making it harder to defeat them.

Some caveats with the patch as of this writing:
* Sometimes, the enemies' hurt messages when initially shot will display in a text window with their roaming messages. I do not yet know how to fix this.
* Some boards have obvious "load times" due to how many objects with their own individual code need to have that code replaced (mostly boards with lots of enemies).

\- The Green Herring  
April 28, 2022 (patch originally published on Discord of ZZT on April 27, 2022)