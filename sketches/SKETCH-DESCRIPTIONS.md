## Sketch Descriptions
- What did you sketch, which sketches correspond to which part of the sketching process?

1) Design Challenge:
    How can two people play chess on the computer using a single offline program without sacrificing fairness for both players?

    (E.g., if the board stays still for every turn, one player gets a better view of the game because it stays in their
    perspective the entire game. This ultimately gives them an unfair advantage over the other player.)

2) Generate 5 **Different** Designs 
Sketch 1: 3D Chess
    Using a 3D plane model for the chess board, so that each player can freely move the board (by clicking-and dragging the cursor)
    in any viewing angle as they please during their respective turns.

Sketch 2: Split-Screen Chess
    In this model, there are two separate views for each player, so that they can view the board from their own perspective
    at any point in the game.

Sketch 3: Rotate Chess
    In this sketch, it is showed that by rotating the screen after each turn, players can view their own perspective 
    of the board during their respective turns.

Sketch 4: Sideways Chess
    Fairness can be achieved by obstructing the perspective of both players. This is demonstrated in the Sideways Chess
    sketch, where the perspective of the board is at the side of the board, so neither player gets an advantage via a 
    better point-of-view.

Sketch 5: All-Direction Chess
    The standard rules of chess are thrown out in this model, and pieces start out in unorthodox positions of the board.
    Again, neither player has the advantage here because both kings start at the side of the board, and the pieces are 
    evenly distributed across the board so neither player has a viewing advantage.

3) Reduce the number of design concepts:
    After careful consideration, I have chosen to discard Sketch 1 because of its complexity along with its inability to
    stay true to the materials learned in class. I have also decided to throw out Sketch 4 because it sacrifices usability, 
    and also sketch 5 because its model deviates too much from the standard rules of Chess, which is far from my intentions.

4) Choose the most promising designs as a starting point
    That leaves us with Sketch 2 and Sketch 3.

5) Sketch 10 details and/or variations of design concepts

#
Details of Rotate Chess:

Sketch 3.1 - This sketch demonstrates the starting point of Rotation Chess, which is just a standard view of the Chess game.
Sketch 3.2 - The diagram here simply paints the process of rotating the window; this rotation animation shall be
                visible to players.
Sketch 3.3 - This demonstrates the inherent flaw in simply rotating the board or window 180 degrees after each turn. While 
all the squares are in the correct positions, the pieces are flipped in the opposite direction of the screen. As the game is 
unplayable while the board is flipped, the application needs to perform a 180 degree flip of every individual square, with 
the goal of flipping the piece icon inside each square. 

Sketch 3.4 - This sketch of Rotate chess shows the final result of performing all required rotations. 


#
Variation of Split Screen Chess: Dual-Monitor Chess

Sketch 2.1 - This sketch includes two windows in two separate monitors, one in the perspective of the player with white
                pieces, and black pieces for the other.
Sketch 2.2 - The screen is slightly blurred out and the cursor is unresponsive, as shown in the sketch, which helps indicate
                to the player in white that it is not currently their turn. The screen may be blurred out completely to avoid
                any unnecessary advantage.


#
Combination of Split-Screen Chess & Rotate Screen Chess

Sketch (2+3).1 - This sketch demonstrates two separate threads running in the background, each of which is running a board
                    of its own, representing the perspective of one of the players. These boards are correlated in the sense
                    that they are running the same game, but have different renders because of the nature of each perspective.

Sketch (2+3).2 - Eyes are used in this sketch to demonstrate that one thread is visible (thread 1), while the other (thread) 2
                    is not. (I.e., in black's turn, it shows the thread containing the black perspective of the board in the app 
                    window).

Sketch (2+3).3 - In here, we can see that only one application window exists, which shows the board of the current player
                    at play. The users do not know that two separate boards are running (via their own thread); they just see
                    the board flipped after each turn. 


##
- Which one did you end up choosing and why?
  - I ended up choosing sketch 3 (described in detail via sketches 3.1 to 3.4) for my own application design. I decided that 
    this option was the best because it stays loyal to the standard rules of chess, and seems the most practical out of all 
    the other options. For instance, the combination of 2 & 3 felt like it would run into issues like race conditions and 
    efficiency problems that may cause headaches in the long run, and all the other options seemed to deviate away from the 
    concepts learned in class. Moreover, I believe sketch 3 is a relatively imaginative solution, and is an adequately complex
    design to pull off.
     