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

Basically, this requirement is not so difficult, just 40 minutes to draft a scheme to satisfy it. However, it took me 4 hours to debug why my program is incorrect for many tests. And what I found is crazy also - Mecab and Unicode Encoder.

Some of you may ask what [Mecab](https://taku910.github.io/mecab) is and why we have to care about [Unicode Encoder](https://unicode.org/faq/normalization.html). Therefore, I will present a little thing about them.

First, [Mecab](https://taku910.github.io/mecab)



