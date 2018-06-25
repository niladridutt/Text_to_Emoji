I have got the emojis from https://pypi.org/project/emoji/

```
$ pip install emoji --upgrade

```
Get the Glove vectors from https://nlp.stanford.edu/projects/glove/

----

# Text_to_Emoji

Convert your text to emoji

I have created 2 seperate ways to convert your text to emoji

* Word to emoji
* Sentence to emoji

# Word to Emoji

Number of emojis = 3415

The word to emoji model converts each and every word to an emoji if it crosses a certain threshold (cosine similarity). The emoji descriptions are mapped with 300 dimensional glove vectors and conditioned on it. Each word is then compared to this map and the emoji with the highest cosine similarity is printed.

# Output:

star boy

⭐ 👦

i love you

🆔 💌 🙅

the pizza is great

the 🍕 🅰 great

chicken lays eggs

🐔 lays 🍳

i have scored hundred in maths

🆔 have 🥅 💯 in maths

She is the queen of hearts

👩 🅰 the 👸 of ♥

messi is the king of soccer

messi 🅰 the 🤴 of ⚽

lets build a rocket

lets 🏗 🅰 🚀


----

# Sentence to Emoji

Number of emois = 5

It uses 2 layers of LSTMs with dropout. The model has been trained on less than 200 sentences and it only has a range of 5 emojis to choose from as I was not able to get a suitable dataset but still it performs considerably well owing to the generalisation power of Glove vectors (word embeddings). The source of this dataset is Coursera.


Model architecture
![Screenshot](architecture.png)

# Output:

I do not like movies 😞

I feel lonely 😞

Let us go and watch football world cup tonight ⚾

Honey lets go out for a date 🍴

She is the most amazing girl ❤️

Happy birthday Raj 😄

This is the best day of my life 😄

My mom is the best ❤️

----
# Dependencies:
* emoji (https://pypi.org/project/emoji/)
* Keras
* Glove vectors (100d and 300d)
* numpy
