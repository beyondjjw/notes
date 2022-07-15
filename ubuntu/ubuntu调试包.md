# ubuntu调试包
https://www.hiroom2.com/2018/04/27/ubuntu-1804-dbgsym-en/


$ mkdir <package>
$ cd <package>
$ apt source <package>
In case of bash is as below. bash-4.4.18 is a source tree.

$ mkdir ~/bash
$ cd ~/bash
$ apt source bash
$ ls
bash-4.4.18                         bash_4.4.18-2ubuntu1.dsc
bash_4.4.18-2ubuntu1.debian.tar.xz  bash_4.4.18.orig.tar.xz
4 Install GDB
Install gdb.

$ sudo apt install -y gdb
5 Debug package
Run GDB with command and path of source code.

$ gdb <command> --directory /path/to/source
<snip>
(gdb)
In case of bash is as below.

$ gdb bash --directory ~/bash/bash-4.4.18/
<snip>
(gdb) b main
Breakpoint 1 at 0x2fdb0: file .././shell.c, line 368.
(gdb) r
Starting program: /bin/bash
Breakpoint 1, main (argc=1, argv=0x7fffffffe418, env=0x7fffffffe428) at
.././shell.c:368
368     {
(gdb) l
363     int
364     main (argc, argv, env)
365          int argc;
366          char **argv, **env;
367     #endif /* !NO_MAIN_ENV_ARG */
368     {
369       register int i;
370       int code, old_errexit_flag;
371     #if defined (RESTRICTED_SHELL)
372       int saverst;

(gdb) la src