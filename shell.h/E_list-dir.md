### `list-dir

```C
void list_dir(char **cmdnargs) {
  if (!cmdnargs[1]) {
    FileList *flist = VFS_list_dir("/");
    if (!flist) {
      printf("#{0xff0000}`#{0xb14e4e}%s#{0xff0000}` dir not found!\n", "/");
      return;
    }
    
    for (unsigned _i=0; _i<flist->file_count; _i++) {
      printf("%s   ", flist->paths[_i]);
    }
    
    for (unsigned _i=0; _i<flist->dir_count; _i++) {
      printf("%s/   ", flist->dirs[_i]);
    }
    
    printf("\n");
    return;
  }

  FileList *flist = VFS_list_dir(cmdnargs[1]);
  
  if (!flist) {
    printf("#{0xff0000}`#{0xb14e4e}%s#{0xff0000}` dir not found!\n", cmdnargs[1]);
    return;
  }
  
  for (unsigned _i=0; _i<flist->file_count; _i++) {
    printf("%s   ", flist->paths[_i]);
  }
  
  for (unsigned _i=0; _i<flist->dir_count; _i++) {
    printf("%s/   ", flist->dirs[_i]);
  }
  
  printf("\n");
}

```