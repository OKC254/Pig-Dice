Pig Dice
===================

- - - - 
By Oscar Kiplimo
## Brief description ##
Pig Dice is a web application that tries to simulate the physical world pig dice game.
Each turn, a player repeatedly rolls a die until either a 1 is rolled or the player decides to "hold".
For instance if person one rolls a dice it will show the random number from 1 to 6 but if you are unfortunate and get a 1 you are awarded a 0 and the chance given to the second player:
A player can also chose to compete against the computer

## Pig Dice Rules ##
+ Two  players or human and computer will compete. The first player to reach an agreed win score or more is  the winner.

+ When it is your turn, you roll. If you get a one, the game is passed to the other player.
+ If you get anything else, you may decide to roll again or pass the pigs.

+ If you keep rolling again, you accumulate points to add to your session score but if you get a one, then all your points accumulated in that turn are nullified.
+ The same rules apply when playing against the computer

## Setup/Installation ##
* Git clone https://github.com/OKC254/Pig-Dice.git or download and unzip the repository from github.

 `git clone https://github.com/OKC254/Pig-Dice.git`
* Open index.html via your web browser.

### Live demo ###
To view the page click on the link below
* https://OKC254.github.io/Pig-Dice/

## Specifications ##
* Player(s) registration section.
	* **Example Input** :  Player's name
    * **Example Output** : Displayed in the game window
    * We use an html input form to get the username
    * `<input type="text" id="player_one" placeholder="player one name" class="form-control">`
    * Then use JS to get the username 
    * `var playerOneName=$("#player_one").val();`
 * Player(s) specifies the winning score
 	* `<input type="number" placeholder="Win score" id="winscore" class="form-control" required>`
 	* `var winscore=parseInt($("#winscore").val());`
 	
* Program will store multiple player(s) details.
	* **Example Input** [Lana Masters, turnscore, totalscore]
	* **Example Output** player.name, player.turnscore, player.totalscore
	* Every player has an instance in the object player with the specified methods and behaviours
	* `function player(name,{this.name=name;this.score=0;this.turnscore=0}`

* Program will return total of round scores as total score.
	* **Example Input1** : [3, 6, 5, 2].
	* **Example Output1** : 15.

* Player rolls a dice if its 1 the player's turn score is initialized to zero and turn passed.
	* **Example Input2** : [3, 6, 5, 2, 1].
	* **Example Output2** : 0.

* Program will end user turn if hold.
	* **Example Input** : hold()
	* **Example Output** : switchPlayers()
	* `player.prototype.hold=function(){this.score+=this.turnscore;this.turnscore=0}`

* Program will determine user wins if total score is equal to or more than the specified win score,say winscore is 110.
	* **Example Input** : 115
	* **Example Output** : return winner
	* `if(score>=winScore){return winner}`

* Program impelements a 1 player mode to compete with computer in two mode recruit(easy) and veteran(hard).
	* **Example Input** : recruit
	* **Example Output** :Computer plays a maximum of two times in each turn.

	* **Example Input** : veteran
	* **Example Output**: computer plays upto 5 times depending on some mathematical constraints on the players and its currents score, recurssion is used in this case

## Technology used ##

* HTML
* CSS
* Bootstrap
* Javascript
* Jquery

## Known Bugs ##

There are no known bugs. If you find any be sure to create an issue and I will respond to it.

## Contributing ##
pull requests are encouraged


## License ##
This project is licensed under the MIT Open Source license, (c) Oscar Kiplimo
