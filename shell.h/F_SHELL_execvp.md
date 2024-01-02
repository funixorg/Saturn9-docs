# `SHELL_execvp`

Function alterative version of `SHELL_execute_command` with auto-separation of arguments
## Syntax

```C
void SHELL_execvp(
	[in] char**   tokens
);
```

## Parameters

`[in] char** tokens`

**Array of strings** that must contain first element the command and the others its *arguments*

## Example

```C
SHELL_execvp(["my_custom", "arg1", "arg2", "arg3"]);
```
