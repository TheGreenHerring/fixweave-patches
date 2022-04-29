# FixWeave patch for "Sivion" v2.00g by Monthigos
- Game location: https://museumofzzt.com/file/s/sivion/
- Requires: FixWeave v1.0c or later

This fixes three notable programming glitches that render the game unwinnable by mistake without cheating, and which exist in the game despite the author's infamous claim (in a hidden board) that "it has been fully beta tested and has no errors":

1. In Rook's encounter with the snake (board 47), attempting to "Give all of [your] gems" will result in its programming halting with "ERR: Bad direction", because it attempts to jump to a ":go" label by using "#go", which is a reserved word in ZZT that requires a (valid) direction to be given. (Ironically, the longer command "#send go" would have worked.) The patch renames both of them to "do", which is the same length and *not* a reserved word. The patch files to fix this also fix a text error in which an idle command sequence is missing a slash at the start and thus combines two lines intended to be separate in one box.
2. In the King's throne room (board 51), when Rook tells the Captain what the prisoner said, the Captain reveals the hidden passage and clears the related flag, but doesn't zap his initial touch label, so he cannot then check if Rook is carrying garlic before letting him through even though he's supposed to. This is fixed to work as intended.
3. In the bank's vault (board 53), the door will never open even if you enter the correct combination, because the code for the final component of the locking mechanism *also* attempts to use "#go" to jump to a ":go" label and thus halts execution with ""ERR: Bad direction". This patch applies the same fix as in the other case.

This patch also includes an optional patch file (SIVION.76) which completely eliminates the initial password requirement to start the game, making it more accessible.

\- The Green Herring  
April 28, 2022 (patch originally published on Discord of ZZT on April 22, 2022)