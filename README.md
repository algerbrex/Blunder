Overview
--------

[Blunder](http://ccrl.chessdom.com/ccrl/404/cgi/compare_engines.cgi?family=Blunder&print=Rating+list&print=Results+table&print=LOS+table&print=Ponder+hit+table&print=Eval+difference+table&print=Comopp+gamenum+table&print=Overlap+table&print=Score+with+common+opponents) is an open-source UCI compatible chess engine. The philosophy behind Blunder's design is for the code to 
straightforward and easy to read, so that others can benefit from the project.

| Version     | Estimated Rating (Elo) | CCRL Rating (Elo) | WAC<sup>1</sup>     | IQ6 <sup>2</sup>
| ----------- | -----------------------|-------------------|---------------------|-----------------
| 1.0.0       | 1400                   | N/A               | N/A                 | N/A
| 2.0.0       | 1570                   | N/A               | N/A                 | N/A
| 3.0.0       | 1782                   | N/A               | N/A                 | N/A
| 4.0.0       | 1832                   | 1734              | N/A                 | N/A
| 5.0.0       | 2000                   | 2080              | N/A                 | N/A
| 6.0.0       | 2200                   | N/A               | N/A                 | N/A
| 6.1.0       | 2200                   | N/A               | N/A                 | N/A
| 7.0.0       | 2280                   | ??                | 279                 | 2477

<sup>1 [Win At Chess](https://www.chessprogramming.org/Win_at_Chess)</sup>

<sup>2 [IQ6 Test](http://www.talkchess.com/forum3/viewtopic.php?f=7&t=77427&p=895799#p895799)</sup>

Installation
-----

Compiling Blunder is fairly simple.

All that is needed is to visit [Golang download page](https://golang.org/dl/), and install Golang using the download
package appropriate for your machine. To make using the Golang compiler easier, make sure that if the installer asks,
you let it add the Golang compiler command to your path.

Your installation should be up and running in about 5-7 minutes, and from there, you need to open up a terminal/powershell/
command line, navigate to `blunder/blunder`, and run `go build`. This will create an executable for your computer, which you
should then able to run.

Usage
-----

Blunder, like many chess engines, does not include its own GUI for chess playing, but supports something
known as the [UCI protocol](http://wbec-ridderkerk.nl/html/UCIProtocol.html). This protocol allows chess engines, like Blunder, 
to communicate with different chess GUI programs.

So to use Blunder, it's reccomend you install one of these programs. Popular free ones include:

* [Arena](http://www.playwitharena.de/)
* [Scid](http://scidvspc.sourceforge.net/)
* [Cute-chess](https://cutechess.com/) 

Once you have a program downloaded, you'll need to follow that specfic programs guide on how to install a chess engine. When prompted 
for a command or executable, direct the GUI to the Golang exectuable you built.

Features
--------

* Engine
    - [Bitboards representation](https://www.chessprogramming.org/Bitboards)
    - [Magic bitboards for slider move generation](https://www.chessprogramming.org/Magic_Bitboards)
    - [Zobrist hashing](https://www.chessprogramming.org/Zobrist_Hashing)
* Search
    - [Negamax search framework](https://www.chessprogramming.org/Negamax)
    - [Alpha-Beta pruning](https://en.wikipedia.org/wiki/Alpha%E2%80%93beta_pruning)
    - [MVV-LVA move ordering](https://www.chessprogramming.org/MVV-LVA)
    - [Quiescence search](https://www.chessprogramming.org/Quiescence_Search)
    - [Time-control logic supporting classical, rapid, bullet, and ultra-bullet time formats](https://www.chessprogramming.org/Time_Management).
    - [Repition detection](https://www.chessprogramming.org/Repetitions)
    - [Killer moves](https://www.chessprogramming.org/Killer_Move)
    - [Transposition table](https://www.chessprogramming.org/Transposition_Table)
    - [Null-move pruning](https://www.chessprogramming.org/Null_Move_Pruning)
    - [Reverse futility pruning](https://www.chessprogramming.org/Reverse_Futility_Pruning)
    - [History Heuristics](https://www.chessprogramming.org/History_Heuristic)
    - [Principal Variation Search](https://www.chessprogramming.org/Principal_Variation_Search)
    - [Fail-Soft](https://www.ics.uci.edu/~eppstein/180a/990202b.html)
* Evaluation
    - [Material evaluation](https://www.chessprogramming.org/Material)
    - [Tuned piece-square tables](https://www.chessprogramming.org/Piece-Square_Tables)
    - [Tapered evaluation](https://www.chessprogramming.org/Tapered_Eval)
    - [Mobility](https://www.chessprogramming.org/Mobility)
    - [Texel Tuner](https://www.chessprogramming.org/Texel%27s_Tuning_Method)
    
 Changelog
 ---------
 
 The changelog of features for Blunder can be found in the `docs/changelog.md`.
 
 Credits
 -------
 
 Although Blunder is an orginal project, there are many people without whom Blunder would not have been finished. 
 The brief listing is included here (in no particular order). For the full listing, with elaborations, 
 see `docs/credits.md`:
 
 ```
 My girlfriend, Marcel Vanthoor, Hart Gert Muller, Sven Schüle, J.V. Merlino, Niels Abildskov, 
 Maksim Korzh, Erik Madsen, Pedro Duran, Nihar Karve, Rhys Rustad Elliott, Lithander, 
 Jonatan Pettersson, Rein Halbersma, Tony Mokonen, SmallChess, Richard Allbert, Spirch, and
 the Stockfish Developers.
 ```
 
 These credits will be updated from time to time as a remember or encounter more people who have helped me
 in Blunder's development.

 License
 -------
 
 Blunder is licensed under the [MIT license](https://opensource.org/licenses/MIT).
