# Introduction to Linux and the Shell

This chapter provides a foundational overview of Linux and its
**command-line interface** (CLI). We’ll cover each subtopic in detail,
including explanations, examples, and relevant shell commands or scripts
where applicable. Commands will be shown in code blocks for clarity,
assuming you’re using a common shell like Bash unless specified
otherwise. You can copy-paste these into your terminal to try them out.

### What is Linux?

Linux is an open-source operating system (OS) kernel originally created
by Linus Torvalds in 1991 as a free alternative to Unix. At its core,
Linux refers to the kernel—the central component that manages hardware
resources, processes, memory, and device drivers. However, “Linux” is
often used broadly to describe complete OS distributions (distros) that
bundle the kernel with user-space tools, libraries, and applications.

Key characteristics of Linux:

-   **Open-Source**: Licensed under the GNU General Public License
    (GPL), allowing anyone to view, modify, and distribute the source
    code.
-   **Multi-User and Multi-Tasking**: Supports multiple users
    simultaneously and runs multiple processes in parallel.
-   **Portable**: Runs on a wide range of hardware, from servers and
    desktops to embedded devices like smartphones (e.g., Android is
    based on Linux) and supercomputers.
-   **Secure**: Uses a permission-based system and is less prone to
    viruses due to its architecture and community-driven security
    updates.
-   **Free and Customizable**: No licensing fees, and users can tailor
    it to their needs.

Popular Linux distributions include Ubuntu (user-friendly for
beginners), Fedora (cutting-edge features), Debian (stable for servers),
Arch Linux (highly customizable), and CentOS/Rocky Linux
(enterprise-focused). Linux powers over 90% of the world’s top
supercomputers, most web servers (e.g., via Apache or Nginx), and cloud
infrastructure (e.g., AWS, Google Cloud).

To check your Linux version, run:

    uname -a  # Displays kernel version and system info

    cat /etc/os-release

### Difference Between Shell, Terminal, and Kernel

These terms are often confused, but they represent distinct layers in
the Linux ecosystem:

-   **Kernel**: The core of the OS. It acts as a bridge between hardware
    and software, handling low-level tasks like process scheduling,
    memory allocation, file I/O, and device management. The kernel runs
    in “kernel space” (privileged mode) and is loaded into memory at
    boot. Users don’t interact with it directly; it’s invisible unless
    you’re a developer writing drivers or modules. Example: The Linux
    kernel (e.g., version 6.8 as of 2025) manages CPU interrupts and
    hardware abstraction.
-   **Shell**: A command-line interpreter that provides a user interface
    to interact with the kernel and system utilities. It reads user
    input (commands), interprets them, and executes programs or scripts.
    The shell runs in “user space” and can be scripted for automation.
    It’s essentially a programming language for the CLI. Common shells
    include Bash (default on many distros).
-   **Terminal**: A software application that provides access to the
    shell. It’s the “window” or emulator where you type commands.
    Historically, terminals were physical hardware (e.g., teletype
    machines); today, they’re apps like GNOME Terminal, Konsole, or even
    web-based ones. The terminal handles input/output, but the shell
    does the actual processing.

In summary:

-   Kernel: Manages the hardware (brain of the OS).
-   Shell: Interprets commands (command processor).
-   Terminal: Displays the shell (user interface window).

To illustrate:

-   Open a terminal (e.g., via Ctrl+Alt+T on Ubuntu).
-   The prompt (e.g., `user@host:~$`) is provided by the shell.
-   Type `echo $SHELL` to see your current shell path (e.g.,
    `/bin/bash`).

<!-- -->

    ps -p $$  # Shows the process of your current shell (e.g., bash)

### Types of Shells (bash, zsh, sh, ksh, fish)

Shells vary in features, syntax, and usability. Here’s a breakdown of
common ones:

-   **sh (Bourne Shell)**: The original Unix shell from 1977.
    Minimalistic, with basic scripting support. It’s POSIX-compliant
    (standard for portability) and often used for simple scripts. Many
    systems symlink `/bin/sh` to a compatible shell like Dash for speed.
    Pros: Lightweight. Cons: Lacks modern features like tab completion.
-   **bash (Bourne Again SHell)**: Default on most Linux distros (e.g.,
    Ubuntu, Fedora). Extends sh with features like command history, tab
    completion, aliases, and job control. Great for scripting and
    interactive use. Pros: Widely available, powerful scripting (e.g.,
    loops, conditionals). Cons: Can be slower for simple tasks.
-   **ksh (Korn Shell)**: Developed in 1983, it combines features from
    sh and csh (C Shell). Includes advanced scripting like arrays and
    floating-point math. Variants like pdksh or mksh are common. Pros:
    Efficient for programming. Cons: Less popular today.
-   **zsh (Z Shell)**: Extends bash with better autocompletion, themes
    (via Oh My Zsh framework), and plugins. Popular among power users
    (e.g., default on macOS since 2019). Pros: Highly customizable,
    spell correction. Cons: Steeper learning curve. **fish (Friendly
    Interactive SHell)**: Modern, user-friendly shell with
    autosuggestions, syntax highlighting, and web-based config. No need
    for complex scripting syntax. Pros: Beginner-friendly, no
    installation of extra tools needed. Cons: Not POSIX-compliant, so
    some scripts may not run without changes.

To check or change shells:

    echo $SHELL  # Current shell
    chsh -s /bin/zsh  # Change to zsh (requires logout/login)
    cat /etc/shells  # List available shells
