Brook and Biruk's Simple Shell

This is a simple UNIX command interpreter written as part of the low-level programming and algorithm track at ALX School.

Description

It is a simple UNIX command language interpreter that reads commands from either a file or standard input and executes them.

Invocation

To invoke the simple shell, compile all .c files in the repository and run the resulting executable.


Environment

Upon invocation, shellby receives and copies the environment of the parent process in which it was executed. This environment is an array of name-value strings describing variables in the format NAME=VALUE.


Command Execution

After receiving a command, shellby tokenizes it into words using " " as a delimiter. The first word is considered the command and all remaining words are considered arguments to that command. Shellby then proceeds with the following actions:
1. If the first character of the command is neither a slash (\) nor dot (.), the shell searches for it in the list of shell builtins. If there exists a builtin by that name, the builtin is invoked.
2. If the first character of the command is none of a slash (\), dot (.), nor builtin, shellby searches each element of the PATH environmental variable for a directory containing an executable file by that name.
3. If the first character of the command is a slash (\) or dot (.) or either of the above searches was successful, the shell executes the named program with any remaining given arguments in a separate execution environment.

Authors

Brook Endale
Biruk Tefera

