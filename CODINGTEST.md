# Circle Programming Exercise

For this coding test, you may use your desired technology stack

## Aim of test

1) First on the home page you will notice 2 buttons under the circle logo
    - Only the "Play Local Game" button should be displayed if the user is not signed in
    - Both buttons should be displayed when a user is signed in

2) Notice there are 2 sets of tables on the home screen
    - If the user is NOT signed in, only the "Leaderboard" and "Games In Progress" should be shown
    - If the user IS signed in the "Leaderboard", "Open Games" and "Games in Progress" tables should be shown

3) Click the "Play Local Game" button, your goal here is to implement a `checkForWinner()` function that checks for a tic-tac-toe winner by using a [Magic Square](http://mathworld.wolfram.com/MagicSquare.html)
    - These games will NOT be saved on the server
    - These games will NOT be posted to the leaderboard
    - These games CANNOT be spectated
    - Users do not need to be logged in to be able to create a local game

4) Now that you have finished the preliminary task, we can get to the meat of this problem which is
    - Allow 2 logged in players to play online, this will involve
    - Creating a lobby when a logged in player clicks 'Create Online Game'
    - After this lobby is created, its information should appear in the 'Open games' List on the home page
    - When the info appears, another logged in player should click the join button, should then go from a lobby to a 'Game in Progress' and this information should appear in the appropriate list
    - Any user should be able to click 'spectate' a game in the 'Games in Progress' list and they should be able to view the game live. Spectators do not need to be able to interact.
    - When a game ends, all users should be transported back to the home page and the players game record should be saved to the leaderboard and updated live

## TECHNICAL DETAILS

1) *ALL* network communication must occur using **Websockets**

2) You will need to define database models for any persistent data i.e the **Leaderboard**, **Lobby** etc.

3) Signed in users must have the results of their games SAVED and POSTED to the home page **Leaderboard**
    -  Leaderboard must be sortable by *wins*, *losses* and *draws*
    -  Leaderboard must be filtered down to the top 4 users by number of wins

4) A *spectated* game is the same as a normal game except a spectator cannot interact with the game, they can only receive game updates

5) A *lobby* is a game with a single player, in a lobby the sole user cannot interact with the Leaderboard until another *player* joins.
    - When a user joins a *lobby*, there should be a notification to the other members in the *lobby*

6) All games in progress must be updated On the **Games in Progress** list
    - it must be sortable by *Created* time

7) All games in progress must be updated On the **Open Games** list
    - it must be sortable by *Created* time

8) All content between the double curly braces `{{Example}}` is dynamic content that is based on the current state

9) There is some `dummy` data hardcoded into the html e.g for the leaderboard list, open games etc. These must be replaced with data from the database

10) There are many object fragments that are being displayed beside each other e.g the `Sign In`, `Sign Up`  is displayed beside the `displayName` object as this does not make stateful sense, you should add conditional statements for these kinds of issues.

11) You **MUST** include Instructions on how setup and run your preferred technology stack.
 
## HINTS

1) This program uses [Bootstrap 4.0](https://getbootstrap.com/docs/4.0/getting-started/introduction/)
