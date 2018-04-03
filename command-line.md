# Command Line Interface!

### Learning Objectives

- Articulate the difference between the command line and the GUI
- Analyze the benefits of using the CLI over the GUI
- Navigate file structure using the command line
- Create new files and directories without using the GUI

## Leaving the GUI behind

Now that we're all about to become super awesome developers, it's time to leave the GUI behind. GUI stands for **G**raphic **U**ser **I**nterface, and it refers to the visual layer over the computer's actual core. Instead, we'll be using the **C**ommand **L**ine **I**nterface and telling the computer exactly what to do. (_Commanding_ it, as it were... 🤔)

Some benefits of using the CLI:

- **Speed** -- it's much faster to type `touch hello.txt` than it is to make a new text file using the GUI.
- **Precision** -- We're able to look at the commands we're about to enter and see exactly what they're about to do.
- **Tools** -- There are a number of tools we can use in the command line to make our work easier to do.
    - Let's install one now. Try running this command: `brew install tree`.  Then, type `tree` into the command line. What do you see?
    - Tools built for the command line usually follow something called the 'Unix philosophy', meaning each tool should do one thing and do it well. Complex tasks can be achieved by chaining tools together.
    - When we get to later units, you'll see just how fast and easy command line tools can make complex tasks.
- **Debugging** -- Whenever we get an error in the CLI, it will often come with a lot of information that we can use to then debug it.


## Common CLI commands

Commands fall largely into two categories: commands that have **output** and commands that have **side effects**.
- Commands with output generally just tell you about files, directories, or the computer in general.
    - `echo`
    - `ls`
    - `pwd`
    - `[thing] -v` -- for example, `node -v`.
- Commands with side effects make changes to the environment.
    - `touch [filename]`
    - `mkdir [directory name]`.

Commands can often be modified using **flags**. For example, `ls` lists all the un-hidden files in a directory, while `ls -A` lists _every_ file, even the hidden ones. To see what options are available for a command, you can run `man [command]` -- for example, `man ls` (`man` is short for "manual") -- or `[command] --help`.

Here are the commands you'll use most frequently:

- `ls` & `ls -A` -- lists all files in a directory
- `cd [somewhere]` -- changes directories to the specified location. The "somewhere" is usually either the name of a directory or `..`, which refers to the parent directory.
- `pwd` -- print working directory. Prints the current directory to the terminal.
- `mkdir [directory name]` -- creates a directory with the specified name
- `touch [file name]` -- creates a file with the specified name

And, of course, the git commands, which you would have used in the prework and which we'll go over again tomorrow.

Some commands you'll also see frequently:

- `mv [path/to/source] [path/to/destination]` -- moves the material at the source path to the destination path
- `cp [path/to/source] [path/to/destination]` -- copies the material at the source path to the destination path

## Mini Lab

- navigate to the desktop via the terminal.
- create a directory called test
- create a text file called hello_world.txt within the test folder.
- add the string "hello world" to the txt file using a command.
- view the contents of the hello world file from the terminal.

**Bonus:**
- rename the ```test``` folder to ```wdi_test```



## ⛔️🙅 Unsafe Commands 🚫🚨

There are some commands that you should try to avoid using.

### `sudo [command]`

`sudo [command]`,  or "super user do [a command]" -- runs the command that follows as the super user (i.e., 'root' or 'admin'). That means your computer will not prevent you from running the command and may not even confirm if this is what you actually want to do. This is of particular concern when the command may have destructive effects.

### `rm [-rf] [a file or folder]`

`rm [-rf] [a file or folder]`, or "remove [recursively by force] [a file or folder]", removes files without any kind of prompt or confirmation. **YOU SHOULD ALMOST NEVER USE THIS COMMAND**. There is **no way** to recover files that have been removed in this way. They do not go in the trash. They are _instantly obliterated from the face of the earth_. Think of `rm -rf` as the fastest way to totally fuck up your entire machine if you run it wrong, or in the wrong place. I have nightmares about students using `rm -rf` and deleting their entire operating system or some shit. _Don't use `rm -rf`._
  - There is one use case where we might tell you to use `rm -rf`, which is if you create a git repository within a git repository. (We will talk more about this tomorrow but it is also something you should _never_ do.) If you're about to run `rm -rf` and the next thing isn't `.git`, rethink your life.
  - Please don't delete your operating system. This is the reason I don't sleep at night.
  
  ## Reference
  
- **Opening Terminal for Mac**: <kbd>Cmd</kbd> + <kbd>Shift</kbd>, then start typing "Terminal"
- **Opening Command Prompt for Windows**: In your application search, start typing "Command" or "CMD".

|                             | Mac / Linux                                            | Windows                                          | Notes                                                                                                         |
|-----------------------------|------------------------------------------------|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Change Directory            | `cd [directory to change to]`                  | `cd [directory to change to]`                    | `cd ..` will go to the directory one above the current directory. `cd .` would stay in the current directory. |
| List All Files              | `ls`                                           | `dir`                                            |                                                                                                               |
| Make a New Directory        | `mkdir`                                        | `mkdir`                                          |                                                                                                               |
| Make a New File             | `touch [filename]`, for ex. `touch index.html` | `NULL > [filename]`, for ex. `NULL > index.html` |                                                                                                               |
| Print the Current Directory | `pwd`                                          | `cd` (no directory to change to)                 | `pwd` stands for `print working directory`. It is handy for figuring out where you are.                       |

