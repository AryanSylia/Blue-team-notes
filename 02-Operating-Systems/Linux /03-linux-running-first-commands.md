
# Linux Fundamentals – Running Your First Commands  
**Date:** 9 January 2026

## Task 4: Running Your First Few Commands

This section represents the first practical interaction with a Linux system. The main goal is to introduce the terminal and remove the initial fear that many beginners feel when working without a graphical user interface (GUI).

Linux systems, especially server environments such as Ubuntu Server, are designed to be lightweight and efficient. Because of this, many Linux systems do not include a graphical interface by default. Instead, interaction with the system is performed through the terminal.

---

## Understanding the Terminal

The terminal is a text-based interface that allows users to communicate directly with the operating system by typing commands. While it may appear intimidating at first, the terminal becomes intuitive once commands are broken down and understood individually.

A typical terminal prompt may look like this:

tryhackme@linux1:~$


This prompt provides useful information:

- `tryhackme` indicates the current username
- `linux1` is the system or host name
- `~` represents the home directory
- `$` shows that the user is a standard (non-root) user

Commands are entered after the `$` symbol.

---

## Why Use the Terminal?

Using the terminal allows users to:

- Navigate the file system
- Display file contents
- Create and manage files
- Interact efficiently with the operating system

These skills are essential for working with Linux in real-world environments, especially in server administration and cybersecurity.

---

## First Command: echo

The `echo` command is used to display text in the terminal. It outputs exactly what is provided as input.

Example:

echo Hello
`

Output:

Hello 


If the text contains spaces, it must be enclosed in double quotation marks:

echo "Hello Friend!"


This ensures that the terminal interprets the text as a single string rather than separate arguments.

The `echo` command is commonly used in scripting, testing commands, and displaying variable values.

---

## Second Command: whoami

The `whoami` command displays the username of the currently logged-in user.

Example:

whoami

Output:

tryhackme


This command is important because Linux heavily relies on user permissions. Knowing which user is currently active helps determine what actions are allowed within the system. This becomes especially critical in security-related tasks and privilege management.

---

## Key Takeaways

- Linux systems often rely on the terminal instead of a graphical interface
- The terminal allows precise and efficient interaction with the system
- The `echo` command outputs text to the terminal
- The `whoami` command identifies the current user
- These basic commands help build confidence and familiarity with Linux

This lesson establishes the foundation for more advanced Linux commands and prepares the learner for practical system interaction.




