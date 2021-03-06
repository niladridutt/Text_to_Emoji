Source of emojis : https://pypi.org/project/emoji/

```
$ pip install emoji --upgrade

```
The models use 100d and 300d Glove vectors trained on the Wikipedia corpus as word embeddings.

Get it from - https://nlp.stanford.edu/projects/glove/

----

# Text_to_Emoji

Convert your text to emoji

I have created 2 seperate ways to convert your text to emoji

* Word to emoji
* Sentence to emoji

# Word to Emoji 

(https://github.com/niladridutt/Text_to_Emoji/blob/master/word_to_emoji.ipynb)

Number of emojis = 3415

The word to emoji model converts each and every word to an emoji if it crosses a certain threshold (cosine similarity). The emoji descriptions are mapped with 300 dimensional glove vectors and conditioned on it. Each word is then compared to this map and the emoji with the highest cosine similarity is printed.

# Output:

star boy - ⭐ 👦

i love you - 🆔 💌 🙅

the pizza is great - the 🍕 🅰 great

chicken lays eggs - 🐔 lays 🍳

i have scored hundred in maths - 🆔 have 🥅 💯 in maths

She is the queen of hearts - 👩 🅰 the 👸 of ♥

messi is the king of soccer - messi 🅰 the 🤴 of ⚽

lets build a rocket - lets 🏗 🅰 🚀

----

# Sentence to Emoji

https://github.com/niladridutt/Text_to_Emoji/blob/master/sentence_to_emoji.ipynb

Number of emojis = 5

It uses 2 layers of LSTMs with dropout. The model has been trained on less than 200 sentences and it only has a range of 5 emojis to choose from as I was not able to get a suitable dataset but still it performs considerably well owing to the generalisation power of 100d Glove vectors (word embeddings). The source of this dataset is Coursera.


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

# Dependencies:
* emoji (https://pypi.org/project/emoji/)
* Keras
* Glove vectors (100d and 300d)
* numpy

# Issues
* Word to emoji has high bias towards America and its culture and certain words like 'is' is displayed as 🅰. Better word embeddings with a larger corpus should be able to contain it.
* I have kept the threshold as 0.115. I'm not sure if this is the best number.
* Sentence to emoji can be greatly improved if it has a much larger dataset and a larger emoji count.
