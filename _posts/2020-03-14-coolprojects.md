---
layout: post
title: "5 Software-Related Projects For High School Computer Nerds"
author: "Peter Ye"
---
After looking through the project pages of four Canadian high school computer science (CS) and computer engineering (CE) nerds ([Tudor Brindus](https://tbrindus.ca/projects/), [Evan Zhang](https://evanzhang.me/projects/), [Ava Pun](https://avapun.com/coding), and [Guanzhong Chen](https://guanzhong.ca/projects/)) and one WLMCI ‘23 CS-nerd ([Paul Lee](https://paullee.dev/)), I have come up with a list of five fun project ideas for high school CS/CE nerds.

# 1. Build an Online Judge
***Requirements: web development knowledge, OS-knowledge, knowledge of multiple programming languages, a server***

In competitive programming, contestants write computer programs to solve math and computer science problems. The programs are graded by an **online judge**, which for each problem runs a contestant's program with a secret set of input data and checks if it matches the secret precomputed set of output data. Building an online judge is a great way to help competitive programmers get more practice. Online judges built by Canadian high school students include the [PEG Judge](https://wcipeg.com/), [DMOJ](https://dmoj.ca/), and [PNOJ](https://oj.paullee.dev/).

## Languages
An online judge should support multiple versions of multiple programming languages. For example, the DMOJ supports *Ada, AWK, Brain\*\*\*\*, C, C11, COBOL, Clang, Clang++, CoffeeScript, C++03, C++11, C++14, C++17, D, Dart, Fortran, Forth, Assembly (x86), Assembly (x64), Go, Groovy, Haskell, INTERCAL, Java 11, Java 8, Kotlin, Lua, C#, F#, Visual Basic, NASM, NASM64, OCaml, Pascal, Perl, PHP, Pike, Prolog, Python 2, Python 3, PyPy 2, PyPy 3, Racket, Ruby 2, Rust, Lisp, Scala, Scheme, Sed, Swift, TCL, Text, Turing, and V8 JavaScript*.

## Sandboxing
When you're running other people's code on your server, you should definitely have a [sandbox](https://en.wikipedia.org/wiki/Sandbox_(computer_security)). Without a sandbox, anyone can easily shutdown your server or wipe your database (also why you should regularly perform a database backup). To sandbox a program, you can use a syscall interception tool such as `ptrace(2)` (more about that [here](https://tbrindus.ca/on-online-judging-part-1/)), or you can run the program on a virtual machine. Using a virtual machine is the most secure option but isn't the most efficient.

![DMOJ](/iii/2020/03/14/dmoj.jpg)

# 2. Make Something Related to Music
***Requirement: knowledge of MIDI***

Making a music-related software project is a unique experience because you will actually be able to *hear* what you have created at the end. You can create a program which ties music together with computer science, like Ava Pun's [Sort to MIDI](https://github.com/AvaLovelace1/sort-to-midi). Or you can create a digital music tool, like Guanzhong Chen's [Music Keyboard](https://github.com/quantum5/MusicKeyboard). The possibilities are endless.

![Sort to MIDI](/iii/2020/03/14/sort_to_midi.png)

# 3. Write an Emulator
***Requirements: depend on what type of emulator you're writing***

Have you ever wanted to play a Game Boy Color game but didn't happen to have a 20-year-old console lying around? That's not a problem, because you can use an **emulator**. An emulator is a computer program which can run software designed for different hardware. For example, you can play the Game Boy Color version of *Super Mario Bros. Deluxe* on your PC using [Nitrous](https://github.com/Xyene/Nitrous-Emulator), an emulator developed by Tudor Brindus and Guanzhong Chen.

## LLE vs HLE
There are two different approaches to emulation: *Low-Level Emulation* (LLE) and *High-Level Emulation* (HLE). LLE emulators need to be able to interpret the machine language of the emulated hardware. They need to reimplement all of the hardware components, including the CPU, memory, and [MMIO](https://en.wikipedia.org/wiki/Memory-mapped_I/O) using software. HLE emulators do not reimplement the hardware but instead reimplement the [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)). They need to handle operating system requests such as opening files and creating threads. You can read [Alexandro Sanchez's article](https://alexaltea.github.io/blog/posts/2018-04-18-lle-vs-hle/) for more information on LLE and HLE.

## Should I Write an Emulator?
Writing an emulator is a great learning experience, though it can be very challenging. If you're interested in computer engineering, writing an LLE emulator (like Nitrous) is one of the best ways to learn how a CPU works. [Emulator 101](http://www.emulator101.com/) is an amazing tutorial about low-level emulation.

<img src="/iii/2020/03/14/mario.png" alt="Super Mario Bros. Deluxe running on Nitrous" width="400"/>

# 4. Recreate a Popular Game
***Requirement: knowledge of the game you're recreating***

Are you an extremely uncreative person? Are you struggling to think of something original to make? If so, you can recreate a popular game such as chess ([version by Evan Zhang](https://github.com/Ninjaclasher/Chess-Program)) or 2048 ([version by Guanzhong Chen](https://github.com/quantum5/2048)). Recreating a game which you've played before can help you gain a better understanding of the game and also refine your programming skills.

<img src="/iii/2020/03/14/2048.png" alt="2048 by Guanzhong Chen" width="300"/>

# 5. Create a Discord Bot
***Requirements: web development knowledge, knowledge of the Discord API, a server***

[Discord](https://discordapp.com/) is a messaging and [VoIP](https://en.wikipedia.org/wiki/Voice_over_IP) application designed for gamers. It has an [API](https://en.wikipedia.org/wiki/Application_programming_interface), which allows developers to create bots. Evan Zhang has created two Discord bots, [DMOB](https://github.com/Ninjaclasher/DMOB-Modern-Online-Bot) and [Ninjabot](https://github.com/Ninjaclasher/Ninjabot).

## Should I Create a Discord Bot?
Discord bots can be very useful ... *to people who use Discord*. If you don't use Discord, *too bad!* I think you should only make Discord bots for tasks related to Discord — moderating chat, welcoming users, managing emojis, file sharing, etc. For things unrelated to Discord such as games and image filters, you should probably make a separate website or application so that people who don't use Discord can also enjoy them.

<img src="/iii/2020/03/14/discord.jpg" alt="Discord" width="600"/>
<hr>
<br>
***Thanks for reading, and happy Pi Day!***
