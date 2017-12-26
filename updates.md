# Updates

## WEEK 1: 

Team A debugged the modules that implement Subtract Square as a single-player game, and Team B debugged the code for the timer, pseudo-random number generator, and LUT. The milestone for this week was to debug a two-player implementation of Subtract Square. Our attempt to do this was not futile as we realized too late that we misused the FSM and the datapath that it controls: our datapath should have initially been designed to compute the next game state and next player, and the FSM should output the values that the various control signals should have cycle by cycle. 

We believe though that implementing the two-player feature is a relatively straightforward task: we intend to implement a T flip flop that flips its output (1-bit output represents a player) when it receives a signal that a move has been made by a player (regardless of whether this move is "valid" since  we have decided on "forcing" the player to input a specific move). Our explanation of the overlap between the project and the course material has been modified under the 'motivations' section to reflect our new understanding of how a FSM is used to control a datapath. 

Next week we plan to debug our new implementation of the FSM and datapath modules, which unfortunately means that the AI feature will not be implemented as planned. Our project description and proposal have also been updated to reflect this change. 


## WEEK 2:

Team A (and Team B) began debugging the modules implementing Subtract Square as a two-player game, and Team B debugged the score feature and tested the LFSR. We had intended to use the LCD screen on the DE2 board to display the timer (which frees up HEX6 & HEX7 to display the score). However, a decision was made towards the end of the lab session to use a shift register wired to some LEDs for the score feature. We are happy with this choice since we showcase course material and we move up the project on the difficulty scale. 

Our deliverable for the second week was to have finished a bulk of the project, which resulted in us having prepared nearly complete (and huge) modules to debug in lab. We initially thought this would be a straightforward task since we tested the individual features beforehand. Unfortunately, debugging was difficult during the lab session since we had trouble tracing the source to our problems and we felt overwhelmed with the size of our modules. Consequently, more successful debugging was done outside of lab time. 

In the lab, we worked on downsizing our modules (which we have submitted on MarkUs). In the process of testing, we discovered some neat debugging tricks and tools. For example, when debugging the FSM, we used a rate divider to slow down the clock speed so that we could observe the LEDs flash (which were wired to the outputs for debugging) as the FSM transitioned from state to state. This helped us tremendously since we were able to conclude that the datapath module was actually the root of our problems. Note: this particular test is implemented in control.v. 

This experience has equipped us to become better at debugging, and we hope that debugging and testing in the final week goes more smoothly. Our plans for week 3 have been updated with our new milestones. 


## WEEK 3:

During the last lab session, Team A continued debugging a simplified version of the datapath and FSM. As we spent time outside of this lab unsuccessfully fixing this code, we spoke with Vlad ASAP to discuss our problem. Fortunately, using Vlad’s suggestion to redesign our datapath by removing unnecessary registers, our code worked. Then for the rest of the lab session, we added and debugged features that interact with our datapath and FSM (eg. “forced move” feature, pseudo-random generator). This was a relatively straightforward task because we submitted code in week 2 that implemented most our desired features, and so we simply had to make minor changes in those files to reflect our newly designed datapath and FSM. 

Team B also spoke with Vlad while debugging the shift register (which is used to keep track of the players’ scores). Once the shift register was properly implemented, we brainstormed and coded a 10-second warning feature that interacts with the timer module. Team B also helped Team A in updating the week 2 test files. 

Outside of lab time, we worked on putting the project together and adding documentation to our code. 


## BRIEF REFLECTION:

Although the AI made was not implemented, we are pleased with the final result. Working on this assignment has solidify our understanding of control paths and datapaths, and made us look at the lab 5 starter code in a different way. We also learned about (and addressed in week 3) propagation timing issues when implementing our FSM and datapath. This problem raises many questions about how large-scale circuits deal with timing delays. 

