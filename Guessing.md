flowchart TD
    A(("The Guessing Game")) --> n8(("Guess A Number 1 to 1000"))
    n8 --> bB["Computer Generates Number"]
    bB --> np("You Will Have 10 Guesses. Enter Your First Guess.")
    np --> n20{"Game Evaluates Answer?"}
    n20 --> n7(("Incorrect Answer")) & kw("Correct Answer. End Game")
    n7 ---> 10{"You Have Guessed Too Low"}
    10 --> nq("Game Displays Number of Guesses Remaining")
    by(("Game Evaluates Number of Guesses")) --> x(("If Number of Guesses > 0")) & IQ(("If Number of Guesses = 0"))
    x ---> sky(("Enter Next Guess"))
    sky --> ncn{{"Game Evaluates Answer"}}
    n7 --> n10(("You Have Guessed Too High"))
    n10 --> nq
    ncn --> zzz(("Incorrect Answer, Loop To N7")) & JJ(("Correct Answer. End Game."))
    zzz --> n20
    IQ --> s(("End Game."))
    nq --> by
    subgraph extra_text[ ]
    direction RL
    n10
    d(Steps For Each Block: 
     1. Game Title Provided
     2. Rules of Game Provided
     3. Game Generates Random Number to Be Guessed
     4. Game Discloses Number of Guesses
     5. Player Enters Guess
     6. Game Evaulates Player's Guess and Decides if the Guess is Correct
     7. If the Guess Is Correct, the Game Ends
     8. If the Guess in Incorrect, the Game Loops Until the Player Guesses correctly or Guesses 10 Times
     )
    end
    style A fill:#C8E6C9,stroke-width:4px,stroke-dasharray: 0,stroke:#00C853
    style n8 stroke-width:4px,stroke-dasharray: 0,fill:#C8E6C9,stroke:#00C853
    style np stroke:#00C853,stroke-width:4px,stroke-dasharray: 0
    style n7 stroke-width:4px,stroke-dasharray: 0,fill:#BBDEFB,stroke:#2962FF
    style nq stroke-width:4px,stroke-dasharray: 0,stroke:#FF6D00,fill:#FFE0B2
    style d stroke-width:none,stroke-dasharray: none, fill:#FFFFFF, fill:#Ffffff