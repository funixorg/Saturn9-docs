# `SHELL_add_command`

Adds the values to the `command_array` (type: `CommandEntry`):
- `const char* command` into `command`
- `void (*function)()` into `function`

## Syntax

```C
void SHELL_add_command(
	[in] const char*   command,
	[in] void          (*function)())
);
```

## Parameters

`[in] char* command`

The command name, when typed into the shell, will execute its callback
It has no exception, and duplicate commands can exist.

`[in] void (*function())`

It is the callback function and will be called by these functions: `SHELL_execute_command` or `SHELL_execvp`.

## Remarks

If it is not put the shell will continue the runtime.
It has no exception, and can **put in the same function argument**.

```C
SHELL_add_command("my_custom", custom_function);
SHELL_add_command("my_custom_copy", custom_function);
```

## Notes

In the **callback function**, it will be passed an **array of strings** containing the command *arguments*. You can add `char **args` to get the passed *arguments*

## Example

```C
void custom_function(char **args) {
	for (int i = 0; i < sizeof(cmdnargs); i++) {
		printf("%s\n", cmdnargs[i]);
	}
}

SHELL_add_command("my_custom", custom_function);
```

