# Wordle Clone

- Go play the real Wordle [here](https://www.powerlanguage.co.uk/wordle/)
- Read the story behind it [here](https://www.nytimes.com/2022/01/03/technology/wordle-word-game-creator.html)
- Try a demo of this clone project [here](https://wordle-using-react.vercel.app/)

_Inspiration:_
This game is an open source clone of the immensely popular online word guessing game Wordle. Like many others all over the world, I saw the signature pattern of green, yellow, and white squares popping up all over social media and the web and had to check it out. After a few days of play, I decided it would be great for my learning to try to rebuild Wordle in React!

_Design Decisions:_
I used a combination of React, Typescript, and Tailwind to build this Wordle Clone. When examining the original Wordle, I assumed the list might come from an external API or database, but after investigating in chrome dev tools I found that the list of words is simply stored in an array on the front end. I'm using the same list as the OG Wordle uses, but watch out for spoilers if you go find the file in this repo! The word match functionality is simple: the word array index increments each day from a fixed game epoch timestamp (only one puzzle per day!) roughly like so:

```
WORDS[Math.floor((NOW_IN_MS - GAME_EPOCH_IN_MS) / ONE_DAY_IN_MS)]
```

_To Run Locally:_
Clone the repository and perform the following command line actions:

- npm init
- npm run start

