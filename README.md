# Rock Paper Scissors Game
A simple Rock Paper Scissors web game written in vanilla JS for JavaScript practice.

<img src="https://github.com/aeonoki/rock-paper-scissors/raw/main/img/game-screenshot.jpg" width="500">

### <img src="https://emojis.slackmojis.com/emojis/images/1643514066/219/bmo.gif?1643514066" width="25"/> How to play?

* Rock beats Scissors
* Scissors beats Paper
* Paper beats Rock

### <img src="https://emojis.slackmojis.com/emojis/images/1643514276/2453/alert.gif?1643514276" width="25"> How to start?

* Download the project
* Extract files
* Open **index.html**

### <img src="https://emojis.slackmojis.com/emojis/images/1643514974/10003/catjam.gif?1643514974" width="25"> How to use?

* Make your move by clicking on the image
* View the result
* Continue playing!
* If you want to reset your score -> click "Reset Score" button

## WARNING

Right now this project has some mistakes that were made on **purpose** for my university practice.

Here these mistakes:

1. ```
    // Changed >= in scissors to <= in paper

    else if (randomNumber >= 1 / 3 && randomNumber <= 2 / 3) {
    computerMove = 'paper';
    } else if (randomNumber > 2/3 && randomNumber < 1) {
    computerMove = 'scissors';
    }
2. ```
    // Changed result

    if(playerMove === 'scissors') {
      if (computerMove === 'rock') {
        result = '?.';
      }
3. ```
    //Commented this line so score won't be saved after f5 page

    //localStorage.setItem('score', JSON.stringify(score));
4. ```
    // Added ++ to wins so after f5 wins will always be 1 at the beginning

    let score = JSON.parse(localStorage.getItem('score')) || {
        wins: 1,
        losses: 0,
        ties: 0
      };
5. ```
    // Swap playerMove and computerMove for showing wrong images
    
      document.querySelector('.js-moves').innerHTML = `You
    <img src="img/${computerMove}-emoji.png" class="move-icon">
    <img src="img/${playerMove}-emoji.png" class="move-icon">
    Computer`;
    }
