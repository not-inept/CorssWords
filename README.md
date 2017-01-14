CorssWords
===========

A multi-user crossword puzzle app leveraging firebase.

# Dev_Notes
I'll formalize things and cleanup code once I figure everything out, but for now I've added basic firebase integration for free multiplayer (with one live game that can have as many users as firebase supports). My intent is to add a launch display with the ability to load puzzles from xwords/latimes/etc (I'll find others later) and allow you to create and share a new game with others. Currently I plan on just generating a game key/link, but in the future I might add accounts (as firebas makes that pretty easy).

#History of jsCrossword

1. [Jesse Weisbeck](http://www.jesseweisbeck.com/) has built this crossword puzzle to provide an enhanced, more intuitive user experience with javascript.
1. [Ash Kyd](http://ash.ms/) did bug fixes and added cool features (e.g. the "reveal a random letter" cheat).
1. [The Dod](http://thedod.github.io) added rot13 (against accidental peeking) and an example puzzle that uses it (EFF's [Xmas 2013 NSA puzzle](https://www.eff.org/deeplinks/2013/12/crossword-what-did-we-learn-about-nsa-year)).
1. [Mason Cooper](github.com/not-inept) in the process of adding firebase integration for cooperative/multidevice puzzles, removing the fixed sample, and adding xwords/latimes xml support.

Your turn :)

#About puzzleData or entryData

The data used to generate the crossword is the main input and is located in js/script.js file.

For particular purposes I use [HartasCuerdas/puzzleData-generator](https://github.com/HartasCuerdas/puzzleData-generator). This generator uses the output produced by [HartasCuerdas/binarify](https://github.com/HartasCuerdas/xwbinarify) that extracts dark and light squares and numbers (clue references) from a digital image of a crossword.
