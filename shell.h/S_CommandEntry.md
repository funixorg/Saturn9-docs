# `CommandEntry`

Entry point of the command and where the *command name* and its *callback* function are stored
## Syntax

```C
struct CommandEntry {
    const char*    command;
    void           (*function)();
} command;
```

## Members

`command`

The name of the command, what will be written in the shell to execute it

`(*function)()`

Command execution function when executed by the function