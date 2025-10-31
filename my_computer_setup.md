# my computer setup

I wanted to write a few notes on how my computer is set up

I have a MacBook running MacOS Sequoia on an Apple M1 chip

I have a folder in my home directory called "Github" where I store my Github code

The path to the folder is ~/Github

To reach my diary, in Terminal, I type the command "cd ~/Github/Diary"

I also have a bin folder in my home directory

The path to the folder is ~/bin

In my bin folder, I store aliases and binaries

Here is a listing of my bin folder

    % ls -l | awk '{print $9, $10, $11}' | awk 'NF'
    chat -> ~/Github/chat/client.py
    decrypt -> ~/Github/rsa/decrypt.py
    encrypt -> ~/Github/rsa/encrypt.py
    homepage -> ~/Github/homepage/main.py
    paint -> ~/Github/Paint/run.sh
    rot13 -> ~/Github/rot13/rot13.py
    rot88 -> ~/Github/rot88/rot88.py
    sigcont  
    sigstop  
    sigterm  
    wordprocessor -> ~/Github/WordProcessor/run.sh
    wp -> ~/Github/WordProcessor/run.sh
    xor -> ~/Github/xor/xor.py

You can see that, at the present moment, I have three binaries in my bin folder (sigcont, sigstop, sigterm)

Also, at the present moment, I have ten aliases in my bin folder (chat, decrypt, encrypt, homepage, paint, rot13, rot88, wordprocessor, wp, and xor)

I wanted to share this computer wisdom... the wisdom of having a Github folder and a bin folder in a home directory

Honestly, it gives me a lot of joy, and it really enriched my life

It's very easy to navigate to ~/bin or ~/Github

Oh -- there's one more thing

I added ~/bin to my PATH variable by adding this line to ~/.zshrc

    export PATH="/Users/myusername/bin:$PATH"

It takes effect when we start a new Terminal session

It also takes effect if we source the file in the current Terminal session (by means of the command `. ~/.zshrc`)

Having done this -- having updated my PATH variable -- I can now call my programs from any directory

For example

    % cd ~
    % rot13 "hello world"
    uryyb jbeyq%
    % cd /tmp
    % rot13 "today is friday october 31 2025"
    gbqnl vf sevqnl bpgbore 31 2025%

You can see that I am able to call my rot13 program (which has an alias in ~/bin) from any directory

Before I wrap this up, I would like to point out that my aliases point to executable scripts

The rot13 alias points to ~/Github/rot13/rot13.py

The file ~/Github/rot13/rot13.py is executable

We can see this by doing a listing of my ~/Github/rot13 folder

    % ls -l ~/Github/rot13/ | awk '{print $1, $9}'  
    total 
    -rw-r--r-- cipher.txt
    -rw-r--r-- message.txt
    -rw-r--r-- README.md
    -rwxr-xr-x rot13.py

You can see that rot13.py is executable

Here is the code in rot13.py

    #!/usr/bin/env python3

    import argparse

    table = {}

    for i in range(0, 26):
        table[chr(ord("a") + i)] = chr(ord("a") + (i + 13) % 26)
        table[chr(ord("A") + i)] = chr(ord("A") + (i + 13) % 26)

    def rot13(message):
        result = ""
        for letter in message:
            substitution = table[letter] if letter in table else letter
            result += substitution
        return result

    if __name__ == "__main__":
        parser = argparse.ArgumentParser(prog="rot13.py", description="Encrypt or decrypt a message using rot13")
        group = parser.add_mutually_exclusive_group(required=True)
        group.add_argument("message", type=str, nargs="?")
        group.add_argument("-m", "--msgfile", type=str)
        parser.add_argument("-o", "--output", type=str)
        args = parser.parse_args()
        if args.msgfile:
            with open(args.msgfile, "r") as msgfile:
                message = msgfile.read()
        else:
            message = args.message
        output = rot13(message)
        if args.output:
            with open(args.output, "w") as outputfile:
                outputfile.write(output)
        else:
            print(output, end="")

I added the line #!/usr/bin/env python3 to the top of the rot13.py file

What does it mean?

The program /usr/bin/env is a utility that searches the PATH variable for the first occurrence of a file (like python3), and then executes that file

So the directive `#!/usr/bin/env python3` is telling my shell (zsh) which Python interpeter to use

This is often preferable to writing a harcoded path, like /usr/bin/python3

I wanted to explain that one thing, the presence of the `#!/usr/bin/env python3` directive at the top of my rot13.py file

Now, I think it's time to wrap things up

In this document, I shared some computer wisdom that I learned from my family

First, I can put my Github code in a ~/Github folder

Second, I can put my aliases and binaries in a ~/bin folder

Third, I can update my PATH variable to include my ~/bin folder

After all is said and done, I can run my aliases and binaries from any directory

For example, I can run my rot13.py script from my home directory, from my ~/Documents directory, or from the /tmp directory

I can even run my rot13.py script from the root directory

    % cd /
    % rot13 "i'm running this from the root directory"
    v'z ehaavat guvf sebz gur ebbg qverpgbel%

I think that's all for now

Today is Friday, October 31, 2025

As my mom would say, TGIF

Thanks for reading,
Andrew
