LINE COMMANDS
=============

<PRE>
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
</PRE>

COMMANDS
========

<pre>
/str[/]            Special case of LOCATE when delimiter is slash
&cmd               Execute cmd, then redisplay it; Enter to repeat
?                  Display last command (PF6); ?? for 2 cmds ago, etc.
=                  Re-execute previous command (PF9); == to do twice
=cmd               Execute cmd, then execute previous command
Add [n]            Add n lines below current line; default=1
ALL [t]            Display all lines matching target; omit t to restore [M]
ALter h1 h2 t n p  Change one character to another; see CHANGE syntax   [M]
BAckward [n|*]     Scroll up n screens; default=1 (PF7)
Bottom             Make last line the current line
CANCEL             Like QUIT for all files in ring                      [M]
CAppend txt        Append txt to end of current line                    [M]
CDelete ct         Delete columns from colptr thru ct; default ct=1
CFirst             Move column pointer to beginning of zone
Change/s1/s2/t n p Change string1 to string2 from curline thru target
CInsert txt        Insert text in current line starting at column pointer
CLast              Move column pointer to end of zone
CLocate ct         Locate column target; moves column pointer
CMS [cmscmd]       Execute CMS command; default=CMS subset mode, RETURN
CMSG [txt]         Place text on command line; default=clear command line
COMMAND cmd        Execute command without checking for synonym/macro
COMPress t         Prepare lines for new tab column settings from SET TABS
COpy t1 t2         Copy lines from curline thru target1 to follow target2
COUnt /str/ t      Count number of times string occurs in lines thru target
COVerlay txt       Overlay text in curline at colptr; blanks do not replace
CP [cpcmd]         Execute CP command; default=enter CP READ mode
CReplace txt       Replace text in curline at colptr; blanks do replace
CURsor CMdline c   Place cursor on command line at column c; default=1
CURsor Column      Place cursor on current line at current column
CURsor Home        Toggle cursor from command line to current line (PF12)
CURsor File l c    Place cursor at line/column in file; default c=1
CURsor Screen l c  Place cursor at line/column on screen; default c=1
DELete t           Delete lines from current line thru target; default=1
Down n|*           Advance current line; default=1; same as NEXT
DUPlicat n t       Make n copies of lines from curline thru target; def=1 1
EMSG [[mno]txt]    Alarm and display error message; optional system msg no
EXPand t           Reposition data in lines with tab (x'05') chars
EXTract /o1/o2/... Extract internal XEDIT info; see EXTRACT Operands
FFile [fn ft fm]   Unprotected file and quit (synonym for COMMAND FILE) [S]
FILE               Save file and quit
FILE [fn ft fm]    Save with new name and quit; typically syn for PFILE [S]
Find txt           Search forward for first line starting with text
FINDUp txt         Search backward for first line starting with text
FOward [n|*]       Scroll down n screens; default=1 (PF8)
FUp txt            Alternate name for FINDUP
GET                Insert lines from prior PUT command below current line
GET fn ft fm f n   Insert lines from file; first,numrec; default: = = = 1 *
Help [topic]       Get help: MENU, TASK, commandname, msgno (PF1)       [M]
HEXType t          Display lines in both hex and EBCDIC; default=1      [M]
Input              Leave edit more and enter input mode
Input txt          Insert line of text into file, below current line
Join [ALigned]     Join current line and next line into one line        [M]
Join " Column      Overlay next line starting at column pointer         [M]
Join " CURSOR      Overlay next line starting at cursor position        [M]
Join " c [c ...]   Overlay next line at column c [, and next at ...]    [M]
Join " /str[/...]  Join current line, string, then next line [,...]     [M]
LEft [n]           Move view of columns to left; default=1; 0 to restore
LOAD fn ft fm      Load file into storage; use in PROFILE XEDIT only
Locate t [cmd]     Locate target, then do optional command
LOWercas t         Change uppercase letters to lowercase; default=1
LPrefix [txt]      Simulate writing txt in prefix area of current line
MACRO name         Execute macro (not command); or name w/nonalpha chars
MErge t1 t2 [c]    Combine two sets of lines, overlay 2nd on 1st at colno
MODify keyword     Display SET command key and current value on cmdline [M]
MOve t1 t2         Move lines from curline thru t1 to follow t2
MSG txt            Display a message in the message area
Next [n|*]         Scroll down n lines; default n=1; same as DOWN
NFind txt          Search forward for first line not starting with text
NFINDUp txt        Search backward for first line not starting with text
NFUp txt           Alternate name for NFINDUP
Overlay txt        Replace chars in curline with non-blank chars in text
PARSE c [ADLNSTW]  Parse stacked line for number/string/target etc.     [M]
POWerimp           Enter input mode, type as if screen were one long line
PQUIT              Quit file being edited, but prompt if modified (PF3)
PREServe           Save XEDIT settings until RESTORE
PSAVE fn ft fm     Protected save with new name; prompt if already exists
PURge macro        Purge copy of macro from virtual storage
PUT [t]            Put lines thru target into temp file; def=1; see GET
PUT t fn ft fm     Put lines thru target into file (create or append)
PUTD t [fn ft fm]  Like PUT but also deletes from the file being edited
QQuit              Unprotected (quick) quit of file being edited
Query op           Query option setting; see QUERY Options
QUIT               Quit file being edited; typical syn for PQUIT (PF3)  [S]
QUIT rc            Quit file being edited and return rc (from macros only)
READ               Place info from terminal into console stack; see READ Subcommand
RECover [n|*]      Recover n lines deleted by DELETE, MERGE, PUTD; def=1
REFRESH            Update screen without waiting for input
RENum [start inc]  Renumber line numbers of VSBASIC or FREEFORT file
REPEat t           Advance line & do last command, for each line thru targ
Replace            Replace current line with line(s) entered in input mode
Replace txt        Replace current line with text
RESet              Cancel all pending prefix commands and macros
RESTore            Restore all XEDIT settings saved by PRESERVE
RGTLEFT [n]        Toggle columns viewed right/left (PF10)              [M]
RIght [n]          Move view of columns to right; default=1; 0 to restore
SAVE               Save file being edited
SAVE fn ft fm      Save with new name; typically synonym for PSAVE      [S]
SCHANGE [pfkeyno]  Make CHANGE confirm each occurrence; def=6 (PF5)     [M]
SET option value   Change various XEDIT options; see SET Options
SHift L|R c t      Shift data left/right c columns thru targ; can lose data
SI                 Structured input: adds new lines, indent as previous [M]
SORT t A|D c1 c2   Sort lines thru target asc/descending by column range
SOS opt            Screen operation simulation, for macros; see SOS Operands
SPlit [ALigned]    Split current line into two lines                    [M]
SPlit " Column     Split current line at current column pointer         [M]
SPlit " CURSOR     Split current line at cursor position                [M]
SPlit " c1 c2 ...  Split curline at column c1 [, and at column c2...]   [M]
SPlit " B|A /str1/ Split curline before/after string [, and...]         [M]
SPLTJOIN           Split or join depending on position of cursor (PF11) [M]
STAck t c n        Stack FIFO lines thru target, starting col, number cols
STATus [macro]     Display SET settings [or create macro with them]
SSave fn ft fm     Unprotected save (synonym for COMMAND SAVE)          [S]
TOP                Make "* * * Top of File * * *" line the current line
TRAnsfer opt       Like EXTRACT but stacks responses for EXEC2 &READ
Type t             Display lines thru target; default=1
Up [n|*]           Move current line up n lines; default=1
UPPercas t         Change lowercase letters to uppercase; default=1
VMFDEOPT           Undo changes made by VMFOPT                          [M]
VMFOPT             Optimize EXEC2 &GOTO label statements in a macro     [M]
Xedit              Move to next file in ring
Xedit fn ft fm     Add another file to XEDIT ring, or move to the file
t                  An XEDIT target (see Targets)
ct                 An XEDIT column target
cmd                An XEDIT subcommand
/                  String delimiter (need not be the slash character)
n                  Number of lines (a non-negative integer); * means all
p                  Starting occurrence
h                  A single character or a two-digit hexadecimal number
fn ft fm           File name/type/mode; use = for same as current file
colptr             Column pointer
curline            Current line
(PFn)              By default, command is assigned to this PF key
[M]                This is actually a macro, not a subcommand
[S]                By default, this is actually a synonym, not a subcommand
</pre>
