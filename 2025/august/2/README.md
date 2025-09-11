# diary

## Thursday August 21 2025

The first journal from this month was written on the days of Tuesday August 19 and Wednesday August 20

I stayed up late last night... really late... like 4am...

I try to go to sleep at 8pm every day

I think that 8pm is the best bedtime

Listen

I'm going to take it easy today

I'm watching a movie and programming

I'm working on a project of mine called terminal

## Thursday August 21 2025

I have a passion for math that goes back many years

When I was a child my mom and I used to do arithmetic problems in our spare time

I got a deeper understanding of mathematics in high school when I became friends with people on the math team

I also had a really good teacher in high school who taught me mathematics

She is more than a good teacher... she is one of my best teachers

She helped me become more confident

She raised my self esteem

She gave our class a final exam and I got the highest score on the final exam

She is actually my 11th grade precalculus teacher

I got an A in her class and I'm really proud of it

She taught me algebra, geometry, trigonometry, probability, and calculus

Let's proceed by giving a lesson on mathematics

We will start the lesson with a question:

How many number systems do you know?

## Thursday August 21 2025

I know four number systems

The number systems I know and use are called decimal, hexadecimal, binary, and tally

The tally number system is an early number system that predates positional number systems like decimal

My name is Andrew Taylor

There are twelve letters in my name

We can write the number twelve in tally like this:

||||| ||||| ||

The tally number system works very well for small numbers like twelve

But what if we want to write the number nine hundred sixty in tally?

The number nine hundred sixty is actually the Unicode code point for the Greek letter Pi

We can verify this by opening the Python shell

In order to open the Python shell, first we can open the Terminal application under Applications>Utilities

(I am using a MacBook so these references are based on the MacOS operating system)

We can open the Finder application, which might be in your dock, and then open Terminal by navigating to Applications and Utilities

Once we have opened Terminal, we can check whether Python is installed with the command

    % python --version

The output (for me) looks like this

    % python --version
    Python 3.11.3

We have verified that Python is installed

The word "python" is an alias for the program /usr/bin/python3

If you don't have the alias set up, you can try this command:

    % /usr/bin/python3 --version
    Python 3.9.6

You might wonder... why does the python alias point to a different version than /usr/bin/python3?

It's because there is a directory in my path that contains a later version of Python

It's because of these lines in my ~/.zprofile configuration file

    PATH="/Library/Frameworks/Python.framework/Versions/3.11/bin:${PATH}"
    export PATH

You can see that it adds the 3.11 Python framework to the path, and that it takes precedence over other directores in my path

So zsh is is able to find Python 3.11 because of those lines in my ~/.zprofile configuration file

If your Python alias is not set up, then you can add the following lines to your ~/.zprofile config file:

    # Setting up an alias for python
    alias python="/usr/bin/python3"

After you append those lines to ~/.zprofile, the alias should be setup.

I think that the file ~/.zprofile is run every time you log in, whereas the file ~/.zshrc is run every time you start a new shell.

So you have to source the file with the command

    % . ~/.zprofile

By sourcing the file, you run every command contained in the shell script ~/.zprofile

Hopefully, this succeeds in setting up the Python alias

Let's try the command again

    % python --version
    Python 3.11.3

If you're able to confirm that the Python alias is configured, then we can open the Python shell by using the python command

If the Python alias is still not configured, then we can open the shell by using the full program path /usr/bin/python3

This is a lot of information, so I'll stop here and pick up later

We originally were talking about the numbers twelve and nine hundred sixty

It is easy to write the number twelve in tally

It is difficult to write the number nine hundred sixty in tally

The number nine hundred sixty is interesting because it's the Unicode code point for the Greek letter Pi

In the next diary entry we can confirm this by opening the Python shell and looking up the Unicode character for the code point 960

## Thursday August 21 2025

It's 4:07pm and my birthday is April 7

It's a special time

Listen

We can write the number twelve in tally

||||| ||||| ||

But it's difficult to write the number nine hundred sixty in tally

Instead, we can use a positional number system like decimal

The number nine hundred sixty in decimal is 960

There are other positional number systems that I use

I also use hexadecimal and binary

The number nine hundred sixty in hexadecimal is 3c0

The number nine hundred sixty in binary is 1111000000

We can confirm this by opening the Python shell

    % python
    >>> print("hello world")
    hello world
    >>> print("we are going to write the number nine hundred sixty in decimal, hexadecimal, and binary")
    we are going to write the number nine hundred sixty in decimal, hexadecimal, and binary
    >>> 960
    960
    >>> hex(960)
    '0x3c0'
    >>> bin(960)
    '0b1111000000'

We said earlier that the Greek letter pi corresponds to the Unicode code point 960

Let's confirm that too

    % python
    >>> chr(960)
    'π'
    >>> chr(0x3c0)
    'π'
    >>> chr(0b1111000000)
    'π'

You can see that 960, 0x3c0, and 0b1111000000 all correspond to the same value (number)

When we lookup this number in our Unicode code table, we get the Greek letter π

You might wonder, "What is Unicode?"

Unicode is a character encoding system

ASCII is also a character encoding system

ASCII has 128 characters, and it makes up the first 128 characters of Unicode

ASCII is a subset of Unicode

ASCII supports the English language but it doesn't support other world languages like Mandarin or Arabic

Unicode supports almost every world language, including Mandarin and Arabic

ASCII has 128 characters

Unicode has over 1 million characters

So you can see that Unicode is a very big character set

UTF-8 is one of many Unicode formats (the other formats I'm aware of are UTF-16 and UTF-32)

UTF-8 is the default charset for HTML5

UTF-8 is the default charset for MacOS files

So listen

Unicode supports almost every world language, including Greek

The Unicode charset contains the Greek letter π

The ASCII charset does not contain the Greek letter π

The Greek letter π corresponds to the Unicode code point 960

We are able to confirm this in the Python shell

    % python
    >>> chr(960)
    'π'

## Friday August 22 2025

So listen

What's the plan for today?

I'm going to take a minimum break of one movie

I learned this language from my family

We can measure breaks in terms of movies

Remember

A measurement is a number accompanied by a unit of measurement

The minimum break is one movie

The number in our measurement is one

The unit in our measurement is movie

So the measurement is 1 movie

The minimum break is 1 movie

Listen

I might program during my break but I've been writing so much I'm going to take a minimum break of 1 movie

I might watch Transformers: Age of Extinction

I might watch X-Men: Apocalypse

There are so many movies

There are more movies than you can shake a stick at

I learned that expression from my friend many years ago

Listen

The minimum break is 1 movie

The magnitude is 1

The unit of measurement (uom) is movie

1 movie

Listen

I'm going to put on a movie

I'm working on my chat application
