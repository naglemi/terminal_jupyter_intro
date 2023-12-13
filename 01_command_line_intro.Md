# Command-Line Basics Tutorial

This tutorial introduces the essentials of the command line, focusing on basic commands and their usage, complete with examples and expected outputs.

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
1. Update package lists:
   ```bash
   sudo apt-get update
   ```
2. Install Jupyter Lab:
   ```bash
   sudo apt-get install jupyter-lab
   ```

## Running Jupyter Lab

**Starting Jupyter Lab**:
```bash
jupyter-lab
```

Depending on your situation, you may either have a browser window automatically pop up with Jupyter Lab, or you will see a link in the Terminal, which you can then copy into the address bar of your browser.
