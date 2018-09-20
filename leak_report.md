# Leak report

Alright so, I got 
==18303== 46 bytes in 6 blocks are definitely lost in loss record 1 of 1
==18303==    at 0x4C2FA50: calloc (vg_replace_malloc.c:711)
==18303==    by 0x400678: strip (check_whitespace.c:41)
==18303==    by 0x4006E3: is_clean (check_whitespace.c:62)
==18303==    by 0x40076B: main (check_whitespace.c:87)

I know that there is the memory for the characters that isn't freed
So, free that I guess
 I'll add a line and try the leack check again
No change


Then there's these three warnings or something that Valgrind gave

Looks like strcmp is missing things

okay I added an if else section, the syntax is probably wrong

Still no changes to valrind

I will try to look at strip

Looks okay to me


