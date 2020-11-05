# Week-10
The goal of this weeks assignment is to create a "Bop It" game in javascript.

You'll need to come up with 3 different keys that you want to represent "twist it", "pull it", and "bop it"
Examples would be "t", "p", "b", "spacebar", "control", "up arrow", etc 
However, we don't want to store the actual keys, we'll store the key code
The keycode is a value that is tied to a key but is the same across ALL keyboards (including international keyboards)
Remember, computer are also better at dealing with numbers so it makes sense that our keyboard would be letters for us but numbers for the computer
Check out https://keycode.info/ (Links to an external site.)to translate keyboard keys to their keycodes
We'll call these our "commands", and we'll save them in an array 
The users will have a score which is the number of correct responses in a row
Initially set to 0
Updated on the page
Display the high score for the game, pulled from local storage on game start
When the game starts, we need to pick a random command and display it to the user
We'll store this command as a variable called "current_command" 
We also need to start a timer for 2 seconds using setTimeout() (Links to an external site.)
We need to add an event listener to the body of our HTML page that listens for any .keypress() (Links to an external site.) event
In the documentation on the above link, each keypress will call a function called "checkKeypress()"
In that function, we'll compare the keycode of the key that was pressed (using the "event" variable that is passed to the function) with our current_command
Make sure you have keycode saved in current_command and we're comparing keycode to keycode
If they pressed the correct key, we need to restart the whole process
Randomly select a new command
Update the UI (user interface)
Restart the 2 second timer
Increase their "score" by 1
If they got the command wrong
Check to see if this is a high score and if it is, save it to local storage
Remove event listeners from the <body> element
This code also needs to run if the timer runs out
