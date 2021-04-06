[Back to Portfolio](./)

Blackjack Playing Program
===============

-   **Class:** CSCI 325 Object-Oriented Programming
-   **Grade:** 95
-   **Language(s):** Java
-   **Source Code Repository:** [features/mastering-markdown](https://guides.github.com/features/mastering-markdown/)  
    (Please [email me](mailto:cjcain1@csustudent.net?subject=GitHub%20Access) to request access.)

## Project description

This is a program which is capable of playing the game Blackjack. The program uses a method called general strategy which is a mathematical approach to playing which gives the highest possible chance of winning any given hand. However, regardless of strategy winning each hand is impossible and the best odds against the dealer is about 50/50. In order to overcome this the program is able to adjust its betting amount based on whether the likelihood of winning the current hand is high or low. This likelihood is determined by counting cards to determine if the odds are in the favor of the dealer or player at that time. Success is not measured by total wins but by an increase of money over time. In order to track this increase, the program uses a virtual dealer to simulate thousands of hands at once. 

This was a group project by Myself, Justin Kizer, Lucas Neidlinger, and Steven Colo. I was the project lead. I designed the project and wrote the sections of code controlling the program’s decision making, the gameplay, the interaction between different classes, and the user interface. Justin Kizer wrote the code for the automated dealer, and Lucas Neidlinger wrote the code for the money tracking and the class for setting house rules.


## How to compiles / run the program

How to compile (if applicable) and run the project.

```bash
cd ./project
python setup.py
```

## UI Design

When the program first runs the user is greeted by a welcome message and is asked if they wish to play with custom rules (see Fig 1). Beyond the simple rules of how to play, there are many rules which are left up to the house such as how many decks to use and how often to shuffle. This allows the user to change the program to mirror the exact table they wish to simulate. If the user chooses to input custom rules, they are asked to input the rules they wish to use (see Fig 2). If not, the program uses the default rules which are the most commonly used house rules and skips to the next step. The user is asked if they wish to simulate multiple hands or play them manually. If the user selects 2 for simulate, they are asked how many rounds (see Fig 3). Once the user enters the number of rounds the program begins simulating. For each hand the program outputs the result as either won or lost. If the player was dealt 21 on the first hand it is considered a Blackjack and this is marked accordingly (see Fig 4). At the end of the simulation the program displays the full results (see Fig 5). The number of hands won, lost, or pushed are roughly the same as real world expectations proving the accuracy of the simulation. The increase in money however is nearly 200%. This is due to counting cards and adjusting the amount of money bet each hand to account for the probability of that hand being a win. The user is then prompted if they wish to continue the simulation. If they choose yes, the simulation runs the same number of hands as before but continues the count and money from the previous iteration. Otherwise, the program ends. The second mode of operation is manual mode. This is accessed by selecting 1 for Dealer at the beginning of the program’s runtime. In this mode the program plays against the user instead of the virtual dealer. The user deals cards to themselves and to the virtual player. The user is then asked to input the value of the cards into the program. After this the user inputs the dealers face up card (see Fig 6). Once the values are entered the program makes a decision and the user deals cards accordingly and inputs their value (see Fig 7). This continues until the player busts or decides to stand. Once the players turn is complete play moves to the dealer. The user is instructed to flip over the dealers face down card and input its value (see Fig 8). If the dealer has less than 17 they must hit and the user is instructed to enter a new card (see Fig 9). This continues until the dealer busts or has more than 17. Once the round is over the results are displayed to the screen (see Fig 10). The user is asked to play again. If they enter yes the loop repeats, otherwise the program ends.

![screenshot](images/dummy_thumbnail.jpg)
Fig 1. The launch screen

![screenshot](images/dummy_thumbnail.jpg)
Fig 2. Example output after input is processed.

![screenshot](images/dummy_thumbnail.jpg)
Fig 3. Feedback when an error occurs.

## Additional Considerations

The program assumes that the user understands the rules of Blackjack. In the manual mode the program tells the user what move to make, and the user is expected to know how to make that move. It is not meant to teach the user how to play.

[Back to Portfolio](./)
