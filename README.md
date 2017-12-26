# Subtract Square 
[Subtract Square](https://drive.google.com/file/d/0BwLvf73ym-VgVlk5NXprMU5NRWM/view?usp=sharing) is a two-player strategy game. A positive whole number is randomly generated as the starting value. The player whose turn it is chooses some square of a positive whole number (such as 1, 4, 9, 16 , ...) to subtract from the value, provided the chosen square is not larger. After subtracting, we have a new value and the next player chooses a square to subtract from it. The game play continues to alternate between the two players until no moves are possible. Whoever is about to play at that point loses! 

## Features
* Two-player mode
* LED scoreboard
* Timer
	* 30-second timer with 10-second warning flash countdown 
	* comes in various speeds
* player’s input is “locked” when timer hits zero (which simulates the “load” key)
* randomly generated starting game state when “start” key is pressed
* “forced move” is chosen when an invalid move is made (please read the documentation for "forced move" in LUTs.v)

## Built with 
* Verilog :trollface:

## Progress
Please read our [proposal](proposal.md), [motivations](motivations.md), and [updates](updates.md) for details on our progress. 

## Authors
* [Jaya Thirugnanasampanthan](https://github.com/jayaJT)

* Perrin Le

* Tianhao (Leo) Yao

* Wesley Ma

## Acknowledgements
* Diane Horton and Danny Heap for game instructions
* Professor Harrington and our TA, Vlad, for helping us through the process 
* [LFSR](http://www.asic-world.com/examples/verilog/lfsr.html)





