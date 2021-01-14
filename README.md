LINE COMMANDS
=============


An       Add n new lines below this line; default=1; same as I command
nA       Add n new lines below this line; default=1; same as I command
Cn       Copy n lines; default=1; use F or P for destination; * means rest
nC       Copy n lines; default=1; use F or P for destination
CC       Copy block of lines; use F or P for destination
Dn       Delete n lines; default=1; * means rest of file
nD       Delete n lines; default=1
DD       Delete block of lines
E        Extend logical line by one more virtual screen line
F        Follow: target for C and M commands
In       Insert n new lines below this line; default=1; same as A command
nI       Insert n new lines below this line; default=1; same as A command
Mn       Move n lines; default=1; use F or P for destination; * means rest
nM       Move n lines; default=1; use F or P for destination
MM       Move block of lines; use F or P for destination
P        Preceding: target for C and M commands
S[+|-]n  Show: in shadow line, show first/last n lines excluded        [SM]
S*       Show: in shadow line, show all lines excluded by X or ALL     [SM]
nS       Show: in shadow line, show first n lines excluded by X or ALL [SM]
SCALE    Display scale line here (like SET SCALE ON n)
SI       Structured input starting on this line (same as SI macro)
TABL     Display tab line here (like SET TABLINE ON n)
Xn       Exclude n lines from display; default=1; * means rest
nX       Exclude n lines from display; default=1
XX       Exclude block of lines from display
"n       Duplicate this line n times; default=1
n"       Duplicate this line n times; default=1
""n      Duplicate block of lines n times; default=1
n""      Duplicate block of lines n times; default=1
/[c]     Make this line the current line; optionally set column pointer
[c]/     Make this line the current line; optionally set column pointer
.name    Assign symbolic name to this line (like SET POINT)
<c       Shift left by c columns on this line; default=1               [SM]
c<       Shift left by c columns on this line; default=1               [SM]
<<c      Shift left by c columns on block of lines; default=1          [SM]
c<<      Shift left by c columns on block of lines; default=1          [SM]
>c       Shift right by c columns on this line; default=1              [SM]
>>c      Shift right by c columns on block of lines; default=1         [SM]
c>>      Shift right by c columns on block of lines; default=1         [SM]
