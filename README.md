# Binary Exploitation 101

This is the repository of the codes used in the sessions for Binary Exploitation 101.
To compile any of the C source files, the following flags for gcc will be useful.

`gcc -z execstack file.c`

This remove the NX bit and allows the execution of shellcodes from the stack.

`gcc -fno-stack-protector file.c`

This removes stack canaries.

If you want to remove ASLR (Address Space Layout Randomization), edit the file
`/proc/sys/kernel/randomize_va_space`

to do that, execute:

```
sudo vi /proc/sys/kernel/randomize_va_space
```

press `r0` and then `:wq`. Then hit `Enter`.

The python scripts will need `pwntools`.

To install the library, run `pip install pwntools`.
