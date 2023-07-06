# Fallout_quiz
_A fallout based quiz game_

This is a JS based browser game. It stores a JSON list of many quiz questions and answers based on quests, places, people and items that my girlfriend and I have encountered when we played the Fallout games together.
To be sure neither of us knows the exact questions and answers from the beginning, we have gathered data from relevant pages of the [Fallout wiki](https://fallout.fandom.com/wiki/Fallout_Wiki) and used API calls to openAI's GPT to generate quiz questions.

To have the questions shuffled differently each time but ensure that we get the same questions in the same session, I enable us to use a code word, used to shuffle the order.
1. I use a hash function on the code. This way, a little change in the code, will create a completely different shuffle.
2. I use the hash as a seed for a random number generator (RNG).
3. I use the generated numbers in a Fisher-Yates shuffle of the questions.
