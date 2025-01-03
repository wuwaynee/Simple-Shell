# Simple Shell

A custom command-line shell implemented in C, designed to mimic basic Unix shell functionalities, including process management, I/O redirection, and pipelines.

## Features
- **Built-in Commands**:
  - `help`: Display available commands.
  - `cd`: Change the working directory.
  - `echo`: Print text to the terminal.
  - `exit`: Terminate the shell.
  - `record`: Show the last 16 commands.
  - `replay`: Replay a previous command using its index (1-16).
  - `mypid`: Display process information:
    - `-i`: Current process ID.
    - `-p`: Parent process ID for a given PID.
    - `-c`: Child process IDs for a given PID.
- **Command Execution**:
  - Single commands.
  - Pipelines with `|`.
  - Input (`<`) and output (`>`) redirection.
  - Background execution (`&`) with PID output for the rightmost process.
- **History Management**:
  - Record the last 16 commands (`record`).
  - Replay previous commands using their index (`replay`).

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/wuwaynee/Simple-Shell.git
   cd Simple-Shell
2. Build the program:
   ```bash
   make 
3. Run the shell:
   ```bash
   ./my_shell

## Notes
- Replay only supports indexes within 1-16.
- Input errors (e.g., invalid pipeline symbols) might not produce detailed error messages.
