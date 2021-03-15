# Pre-work - _Memory Game_

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program.

Submitted by: **Max Zhou**

Time spent: **1.5** hours spent in total

Link to project: https://glitch.com/edit/#!/helpful-wood-taker?path=README.md%3A9%3A20

## Required Functionality

The following **required** functionality is complete:

- [ ] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
- [ ] "Start" button toggles between "Start" and "Stop" when clicked.
- [ ] Game buttons each light up and play a sound when clicked.
- [ ] Computer plays back sequence of clues including sound and visual cue for each button
- [ ] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess.
- [ ] User wins the game after guessing a complete pattern
- [ ] User loses the game after an incorrect guess

The following **optional** features are implemented:

- [ ] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
- [ ] Buttons use a pitch (frequency) other than the ones in the tutorial
- [ ] More than 4 functional game buttons
- [ ] Playback speeds up on each turn
- [ ] Computer picks a different pattern each time the game is played
- [ ] Player only loses after 3 mistakes (instead of on the first mistake)
- [ ] Game button appearance change goes beyond color (e.g. add an image)
- [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
- [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough

Here's a walkthrough of implemented user stories:
![](http://g.recordit.co/lpJ5yfsNO9.gif)

## Reflection Questions

1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here.

I used the W3 Schools website for their list of color codes.

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words)

One of the main issues I faced while working on this project was the guess() function in script.js. I first figured that there would be two scenarios:

1. a correct sequence would allow you to continue.
2. a wrong answer would result in an instant loseGame().

My first code structure involved nested conditional loops that would check for these two conditions. However, I set the conditional to return winGame() whenever the guessCount matched the progress count. Essentially, this would set off the alert whenever the user picked the correct answer. When I tested the guess() function, it would instantly end the game upon clicking the first correct button on the first round. I made this mistake because I intended the round to continue upon a correct guess choice. However, I ended up triggering the winGame() event. To fix this, I split the conditional into a nested conditional. The fist would check if the guessCounter matched or exceeded the total number of rounds (in this case, the array length). If it did, the game would end with winGame(). If it did not match, the round would continue on to the next stage. Upon fixing this issue, the project worked as expected.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words)
   
   One question I have is: what other technologies would be useful in creating a full-stack application? HTML, CSS and JavaScript are useful for the front-end aspects of an application. However, there are many more technologies/tech stacks that are needed for a well-rounded application.

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words)
   
   If I had more time to work on this project, I would make different difficulty modes (e.g. easy, medium, hard). The easier difficulty modes would allow for a slower pace game while the harder difficulties would allow for faster paced gameplay. The harder difficulty would also require better memorization, since the lights would switch faster. The harder difficulty modes could also have more buttons, resulting in more things to think about.

## License

    Copyright [YOUR NAME]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
