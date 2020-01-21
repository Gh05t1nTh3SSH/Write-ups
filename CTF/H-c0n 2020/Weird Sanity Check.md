# Welcome

## 🧠 Weird Sanity Check 🧠

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Weird%20Sanity%20Check/welcome_title.png)

After trying to convert the word "weird" to MD5 and submit the flag without success, I've took a look at the source code finding a hidden div, which contains a string without display:

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Weird%20Sanity%20Check/source_code.png)

~~~
FMVSWKZLFMVSWKZLLM7CWPRLFMVT4KZLFMVSWKZLHYVSWKZLFMVSWKZLFM6DYPB4FVOT4PR6FMVS4PBLFMVSWKZLFMVSWKZLFMVSWKZOHY7C2LR4HQVSWKZOHY7CWKZLFMVSWKZLFMVSWLRLFMVSWKZLFMVSWKZLFMVS4PB4FMVSWKZLFMVSWLRNFUWS2LJOFUXC2LRLFMVSWKZLFMXD4KZLFMVSWKZLFMVSWKZLFMVSWKZLFMVSWKZLFMVSWLRLFMXDYLJNFUWS2LRLFY7C4PBNFUWS4KZLFMVSWKZLFYWS2LJNFUXCWLR6FY6C2LJOFMVSWKZOFMXCWLRNFUWS2LJNFUXD4KZLFMXC2LR4FMVSWLR6FUWS2LRLFMXCWLR4FMVSWKZLFYWS2LJNFUWS2LJOFMVSWKZLFMVS4PROFY6C2LJNFUXD4PRLFMXA====
~~~

As per termination with characters "==" and the capital strings, we can assume that this can be a [Base32](https://en.wikipedia.org/wiki/Base32).

Once decoded we see a the following weird string: 

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Weird%20Sanity%20Check/base32_d.png)

~~~
++++++++++[>+>+++>+++++++>++++++++++<<<<-]>>>++.<+++++++++++++++.>>-.<<+++.>>+++++++++++.+++++++++++++.<<++++++++.-----.-.-.+++++++.>+++++++++++++++++++++++++.++.<-----.+.>.<---.+++++++.-----.+.>.<--.++++.+.+.-------.>+++.-.<+++.>---.++.+.<+++++.--------.+++++++.>..<----.>>++.
~~~
This string have a similar format as one of the [Esoteric Programming Lenguage](https://en.wikipedia.org/wiki/Esoteric_programming_language) called 🧠 [Brainfuck](https://en.wikipedia.org/wiki/Brainfuck). 🧠

The next step was visit the online tool called [Dcode](https://www.dcode.fr/brainfuck-language), where there is a feature to translate this code to text.

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Weird%20Sanity%20Check/dcode_brain.png)

## Flag 

H-c0n{83218ac34c1834c26781fe4bde918ee4}

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Weird%20Sanity%20Check/welcome_comlpete.png)

