
# Basics

We're all familiar with using a Computer that has a GUI, but GUIs are not really the programs that we're using the programs are running in the background and they just use GUIs to show us information and to allow us to interact with them. In a lot of cases that is exactly what we want for photo editting, document layout, browsing the web, graphic design, watching movies and
playing games. In the world of Software Development and System Administration most of the programs that we use don't have or need a GUI. Servers, Utilities and other programs usually only need some text based information to do what they do. Many of these programs run on a server somewhere in a data center without a monitor so the overhead of GUI is completely unnessecarry. One way we interact with these programs that don't have a GUI is throught the Command Line. The Command Line is a text based interface where we type commands and direct text based inputs and outputs to screens, files of other programs. The enviroment we use is called a shell of a Command-line interpreter. The Command-line interpreter was one of the earliest ways of interacting with a General Purpose Computer. The are many shells out there the common ones are:

* 1971 &mdash; Thompson Shell for Unix
* Bash

There are a few terms and ideas that you need to be familiar with to really be productive using the command line before we jump into using commands let's have a look at how command line statements are structured. The general pattern you will see is

```bash
**command** **option(s)** **argument(s)**
ls -lh /usr/bin
sort -u users.txt
grep -i "needle" haystack
```

The command is the program that we're invoking or running.

Everything apart from the command name is mostly optional. You could have a valid command with just the arguments without any options and vice versa.

`ls` which is short for list it lists the files in the specified directory.

Options the command how to operate i.e changing the behaviour of the command or telling it to perform different actions. A few points about options:

* Start with a dash
* Usually one letter
* More then one offered by most commands

```bash
ls -l -a -h /var/log
```

Most of times instead of listing each of the option individually we can combine them right after one dash

```bash
ls -lah /var/log
```

The order of the options usually does not matter.

Some options have a longer syntax and they start with 2 dashes

```bash
ls --group-directories-first --human-readable /var/log
```

The last portion of a statement is the argument(s) or argument this is where you tell the command what thing to operate on.

```bash
ls Desktop
```

In this example we're tellinf the ls command to show us the contents of the Desktop.

## Write commands in a shell prompt

Now we will learn that how can we issue those commands to the system. I will open up a new terminal by pressing `Ctrl + alt + T`. In a graphical enviroment we use the terminal application to work at the command line. The terminal application runs a shell program (which is a text based interface where we can interact with the system). The first thing we see in the terminal is the prompt and it's the place where we enter the commands. The prompt shows a little bit information such as computer name and the user name and maybe the name of the folder where i'm currently working.

### Terminal Navigation Shortcuts

| Key Combination | Result |
|-------|:------|
|Ctrl-A(^A)|Move to the begining of the line.|
|Ctrl-E(^E)|Move to the end of the line.|
|Ctrl-Left arrow|Move backward a word.|
|Ctrl-Right arrow|Move forward a word.|
|Ctrl-U|Deletes from cursor from the begining of the line.|
|Ctrl-K|Deletes from cursor to end of line.|
|Ctrl-Shift-C|Copy to clipboard.|
|Ctrl-Shift-V|Paste from Clipboard.|

## Find help for commands

### man

View the reference manual or man page for a specified command. You can think of **man** pages as a technical reference book for your linux distribution. If you know the name of a command you can find out a wealth of information about it i.e what options it provides and what arguments it takes. To look up something in the man pages type:

```bash
man ls
```

![man](../cli-basics/resources/man.png)

As shown in the screenshot above via `man` we can see some inforrmation about the ls command. We can see that it's for listing directory contents. It also gives an overview of how to use the command in the synopsis section.
