# Command-Line Basics Tutorial

This tutorial introduces the essentials of the command line, focusing on basic commands and their usage, complete with examples and expected outputs.

## First look
When you enter the command line, you will be greeted with something that looks like this:
```bash
gmobot@gmobot-Precision-5820-Tower:/home/current_directory$
```
What does this mean? Here, we see our username (`gmobot`) before the `@`, followed by the name of our computer (`gmobot-Precision-5820-Tower`). Next, after the `:`, we see the path to the directory (folder) we're in right now (`/home/current_directory`) followed at last by the $. You can think of the $ as meaning, "The computer is waiting for you to type something."

## What is the Command Line?

The command line, also known as the terminal or shell, is a text-based interface for interacting with your computer, where you can enter and execute commands.

## Basic Commands

To enter a command, type a command as shown below and then press enter.

### 1. `ls` (List)
Lists the files and directories in the current directory.

**Usage**: `ls`

**Example**:
```bash
$ ls
Desktop  Documents  Downloads  Music  Pictures  Videos
```

### 2. `cd` (Change Directory)
Changes the current working directory.

Note: The tilde symbol (~) is shorthand for your home directory (typically something like /home/users/michael). Your home directory is typically where your Desktop, Documents, Pictures, etc. are found.

**Usage**: `cd [directory]`

**Absolute vs. Relative Paths**:
- **Absolute Path**: Specifies the location from the root directory, e.g., `/home/user/Documents`.
- **Relative Path**: Specifies the location relative to the current directory, e.g., `Documents` when in `/home/user`.

**Navigation Shortcuts**:
- `.` refers to the current directory.
- `..` refers to the parent directory (one level up).

**Examples**:
```bash
$ pwd
/home/user
$ cd Documents
$ pwd
/home/user/Documents
$ cd ..
$ pwd
/home/user
```

### 3. `pwd` (Print Working Directory)
Displays the current directory's absolute path.

**Usage**: `pwd`

**Example**:
```bash
$ pwd
/home/user
```

Note: If a path starts with `/` then that is the path starting with the root directory... the biggest directory (folder) that contains ALL other directories. You can go to your root directory via `cd /` and if you type `pwd` while in `/` (your root directory) then you will only see `/`.

### 4. `ls -lhrt`

We already talked about the `ls` command. Now, we can also add some extra options. Options are indicated after `-` and modify the behavior of a particular command.

Lists files and directories with detailed information with file sizes in human-readable format, sorted by modification time. I find this command very useful for viewing directory contents in an organized way, with all details I might need.

**Usage**: `ls -lhrt`

**Example**:
```bash
$ ls -lhrt
total 8.0K
drwxr-xr-x 2 user user 4.0K Apr  1 12:00 Documents
drwxr-xr-x 2 user user 4.0K Apr  1 12:01 Pictures
```

## Installing Jupyter Lab
Jupyter Lab is a popular interactive development environment.

**Installation Steps**:
Here, we are assuming you are running Ubuntu or another Debian-based Linux distro. Other distros use different package management systems (e.g., yum for Red Hat-based systems, pacman for Arch Linux). Each system has its own package manager due to differences in packaging methods, repository formats, and management philosophies.

Pro-tip: You can copy and paste these commands into the terminal. However, if you're on a Linux-based system, copy and paste can work a little differently from what you're used to, and depends on whether you're copying/pasting to/from the command line, or somewhere else.<br><br>

Copy outside command line: Ctrl+C<br>
Paste outside command line: Ctrl+V<br>
Copy in command line: Ctrl+Shift+C<br>
Paste in command line: Ctrl+Shift+V<br>

1. Update package lists:
   ```bash
   sudo apt update
   ```
2. Begin by updating your package list to ensure you have the latest repository information.
   ```bash
   sudo apt update
   ```
3. Install `pip`, the Python package manager.
   ```bash
   sudo apt install python3-pip
   ```
4. Now using `pip`, install Jupyter Lab... and let's also install the `bash` kernel for Jupyter Lab, which will let us run the `bash` command line kernel inside of Jupyter. `bash` is what we've been using so far in the command line. You can think of it as the typical "programming language" of the command line.
   ```bash
   pip3 install jupyterlab bash_kernel
   ```
5. Add jupyterlab to our `PATH`, which tells the computer where to find this installed software.
   ```bash
   echo "export PATH=\$PATH:$(find ~/.local -name jupyter-lab | sed 's|/jupyter-lab||')" >> ~/.bashrc
   ```
6. One more step...
   ```bash
   source ~/.bashrc
   ```
The command source ~/.bashrc reloads your .bashrc file in the current terminal session. This means it applies any changes you've made to this file without needing to close and reopen the terminal. It's similar to restarting the terminal because both actions make the terminal aware of the latest environment settings, like updated PATH variables or new aliases, but source ~/.bashrc does this instantly in the existing session.

Note: You might be wondering what `sudo` means. With `sudo`, you are calling on administrator priveledges, which are often needed for important or sensitive tasks such as installing files.

## Running Jupyter Lab

**Starting Jupyter Lab**:
```bash
jupyter-lab
```

Depending on your situation, you may either have a browser window automatically pop up with Jupyter Lab, or you will see a link in the Terminal, which you can then copy into the address bar of your browser.
