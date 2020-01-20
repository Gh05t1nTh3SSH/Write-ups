# Welcome :D

## Weird Sanity Check

Imagen1 (title)

After trying to convert the word "weird" to MD5, I've took a look at the source code finding the following:

'''
FMVSWKZLFMVSWKZLLM7CWPRLFMVT4KZLFMVSWKZLHYVSWKZLFMVSWKZLFM6DYPB4FVOT4PR6FMVS4PBLFMVSWKZLFMVSWKZLFMVSWKZOHY7C2LR4HQVSWKZOHY7CWKZLFMVSWKZLFMVSWLRLFMVSWKZLFMVSWKZLFMVS4PB4FMVSWKZLFMVSWLRNFUWS2LJOFUXC2LRLFMVSWKZLFMXD4KZLFMVSWKZLFMVSWKZLFMVSWKZLFMVSWKZLFMVSWLRLFMXDYLJNFUWS2LRLFY7C4PBNFUWS4KZLFMVSWKZLFYWS2LJNFUXCWLR6FY6C2LJOFMVSWKZOFMXCWLRNFUWS2LJNFUXD4KZLFMXC2LR4FMVSWLR6FUWS2LRLFMXCWLR4FMVSWKZLFYWS2LJNFUWS2LJOFMVSWKZLFMVS4PROFY6C2LJNFUXD4PRLFMXA====
'''

For the termination with the characters "==" and the mayus strings, we can assume that is a Base32:

1st

Once we decode the Base32 it appears a weird string:

Brain_image

This weird string it's part from one of the [Esoteric Programming Lenguage](https://en.wikipedia.org/wiki/Esoteric_programming_language) called [Brainfuck](https://en.wikipedia.org/wiki/Brainfuck), and we can find an online tool to decode it: 

Using [Dcode](https://www.dcode.fr/brainfuck-language)

dcode

## Flag 

H-c0n{83218ac34c1834c26781fe4bde918ee4}

Welcome

