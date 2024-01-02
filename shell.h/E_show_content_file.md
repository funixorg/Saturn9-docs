### `show content file`

```C
void cat(char **cmdnargs) {
  if (!cmdnargs[1]) {
    return;
  }
  
  char *content = VFS_read_path(cmdnargs[1]);
  
  if (content) {
	  printf("%s\n", content);
  }
  else {
	  printf("#{0xff0000}`#{0xb14e4e}%s#{0xff0000}` file not found!\n",
	  cmdnargs[1]);
  }
  
  free(content);
}
