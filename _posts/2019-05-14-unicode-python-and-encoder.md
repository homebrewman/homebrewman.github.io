---
layout: post
title: Unicode, Python and Encoder
subtitle: Each post also has a subtitle
#gh-badge: [star, fork, follow]
tags: [Bug, IT, Unicode, NLP ]
comments: true
---
## Problems of Encoder in MeCab and Japanese

Today, I have received a crazy requirement from my boss: separate the Japanese contents in parentheses, translate them and insert them back in correct positions.
{: style="text-align: justify;"}

Basically, this requirement is not so difficult, just 40 minutes to draft a scheme to satisfy it. However, it took me 4 hours to debug why my program is incorrect for many tests. And what I found is crazy also - Mecab and Unicode Encoder.

Some of you may ask what [Mecab](https://taku910.github.io/mecab) is and why we have to care about [Unicode Encoder](https://unicode.org/faq/normalization.html). Therefore, I will present a little thing about them.

First, [Mecab](https://taku910.github.io/mecab) is a tool for segmenting text to assist Natural Language Processing applications for specific purpose. To be more specific, just make an imagination that you are making a command (in Japanese) for your robot. Your robot will initial convert your voice command into text and using some tool (such as Mecab) for separate parts of this text to recognize what your purpose is, what the object in your command is, etc. 
{: style="text-align: justify;"}

Second, you may want to know why we care about Unicode and Encoder. These terms, at the beginning or computer, does not exist since ASCII - a encoding standard of American - is enough for writing and displaying English - the most popular language. However, when computer raises, people also want to display many other languages such as French, Japanese, Chinese, etc. These languages, of course, can be displayed by ASCII, but believe me, you can only see the square like 🔳 for every non-latin character. Hence, you are not able to know whether they are blaming you or not. For these reasons, they invent a new encoding call Unicode to make sure that every computer displays correct characters (to trace who are defacing you in non-English language). Unfortunately, Seagate, Toshiba and other hard-drive manufactories increased their price (I guess so), so they have to limit the number of bits for representing one characters. That a reason why we have unicode 8bit (utf-8), 16 bit (utf-16), 32 bit (utf-32) or even 64 bit (for rich guys - I guess).
It seems these 2 terms are enough for you to understand the context, but actually NOT. Some crazy guys proposed a method of using two separated characters to represent one characters (for example he want to use `ê` and `~` to display `ễ`) while other rich guy say just simple create a new character for each combination. And then, we have two new term `decomposed` and `composed`. I suggest you to read [wiki](https://en.wikipedia.org/wiki/Unicode_equivalence) for more detail and exact information :D.

Come back to my problem, (It is too late, I'll write on tomorrow)


