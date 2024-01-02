# `SHELL_execute_command`

Executes the function of the command starting from the command name

## Syntax

```C
void SHELL_execute_command(
	[in] const char*   command,
	[in] char**        cmdnargs
);
```

## Parameters

`[in] const char* command`

Name of the command you want to execute.

`[in] char **cmdnargs`

Array of arguments, these arguments will be passed to the function.

## Example

```C
SHELL_execute_command("my_custom", ["arg1", "arg2", "arg3"]);
```
