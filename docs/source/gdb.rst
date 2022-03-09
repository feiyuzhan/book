gdb
===================================

1. gcc -g test.c -o test.out
2. gdb ./test.out
3. b(breakpoint) home/xxx/test.c:13
4. r(for run, stop before line 13)
5. n(for next, one step but not step into)
6. Enter(repeat last command)
7. s(for step into)
8. k(kill, kill debugging)
9. info b(show breakpoints)
10. d 1(delete breakpoint 1)
11. c(continue to next breakpoint)
12. bt(back trace, show function call trace)
13. watch(watch point for variable, e.g watch i)
14. info r(show all register)
15. info variables
16. p (for print, show variable value, e.g  p i)
17. layout src(ctrl x + a)
