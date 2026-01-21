# minishell project

hey, this is our minishell project. its basically a small version of bash that we wrote in C. we learned alot about processes and file descriptors while making this.
it works like a real shell, you can type comands and it executes them. we used a tree structure for parsing which was kinda hard but it works good now.

## features

we implimented all the mandatory stuff asked in the subject:

* **prompt**: shows a prompt when waiting for a new comand.
* **history**: working history so you can use up/down arrows.
* **system excutables**: searches for binaries in the $PATH or absolute path.
* **signals**: handles `ctrl-C`, `ctrl-D` and `ctrl-\` like bash does.
* **parsing**: handles single quotes `'` (literal) and double quotes `"` (interprets $).
* **pipes**: you can use `|` to pipe commands together.
* **rederections**:
    * `<` redirects input.
    * `>` redirects output.
    * `>>` redirects output in append mode.
    * `<<` heredoc (reads input until a delimiter).
* **enviroment varibles**: handles `$VAR` expansion and `$?` for exit status.

### builtins
we made our own versions of these comands:
* `echo` (with -n option)
* `cd` (changes dircetory)
* `pwd` (print working directory)
* `export` (add varibles to env)
* `unset` (remove varibles)
* `env` (print enviroment)
* `exit` (exits the shell)

## bonus part

we also did the bonus part:

* **logic operators**: supports `&&` and `||`.
* **wildcards**: the `*` works for the current directory.
* **priority**: handles parenthesis `()` for priority in logic operations.

## instalation

its easy to run. first make sure you have `readline` installed.

1. clone the repo.
2. compile it with make:
```bash
make
```
3. run the executable:
```bash
./minishell
```

## cleaning up

if you want to remove the object files you can run `make clean`. if you want to remove everything including the program run `make fclean`

## authors

    *zelkalai*
    *ayel-mou*
