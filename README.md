SET OPTIONS
==========

<pre>
 SET  = str               Put string in the = buffer
 SET  ALT n [p]           Change number of AUTOSAVE/SAVE alterations
[SET] APL ON|OFF          Tell editor and CMS if APL keys are available
[SET] ARBchar OFF|ON [c]  Turn on arbitrary character; define it; default=$
[SET] AUtosave OFF|n [fm] Autosave every n alterations; filemode
[SET] BRKkey OFF|ON key   Set CP BRKKEY key (usually ON PA1)
[SET] CASE Uppercase|Mixed [Respect|Ignore]
                          U/M: do/don't translate all chars to uppercase;
                          R/I: respect/ignore case in target strings
[SET] CMDline On|OFf|Top|Bottom
                          Last two lines, off, second line, last line
[SET] COLOR field|* [color] [exthi] [High|Nohigh] [pss]
                          Define color/highlighting for an area of screen
[SET] COLPtr ON|OFF       Column pointer (typewriter terminals only)
 SET  CTLchar OFF         No control character for reserved lines
 SET  CTLchar c OFF       Reset a specified control character
 SET  CTLchar c Escape    Define escape character (next is a control char)
 SET  CTLchar c Protect|Noprotect [clr] [xhi] [High|Nohigh|Invisible] [pss]
                          Define field type created by char
[SET] CURLine ON|OFF M[+n|-n]
                          Place/remove current line
[SET] DISPlay n1 [n2|*]   Display scope (see SET SELECT); default=0 0
[SET] ENTer [BEFORE|AFTER|ONLY|IGNORE] [cmd|NULLKEY|COPYKEY|TABKEY]
[SET] ESCape ON|OFF [c]   Escape char for cmds (typewriter terminals only)
[SET] ETARBCH ON|OFF [c]  Extended arbitrary char for DBCS strings
[SET] ETMODE ON|OFF       Extended mode: recognize DBCS strings?
[SET] FILler [c]          Filler char, when tabs expanded; default=space
[SET] FMode fm            Change filemode (A-Z, and optional 0-6)
[SET] FName fn            Change filename (1-8 chars)
[SET] FType fn            Change filetype (1-8 chars)
[SET] FULLread ON|OFF     Sense null chars in lines; like CMS SET FULLREAD
[SET] HEX ON|OFF          Allow hex in strings and targets (LOCATE/x'FF'/)
[SET] IMage ON|OFF|Canon  Handling of tab and backspace chars during input
[SET] IMPcmscp ON|OFF     Implicit CMS/CP cmd if not recognized by XEDIT
[SET] LASTLorc [str]      Put string in last-locate-or-change buffer
[SET] LINENd ON|OFF [c]   Recognize/specify line-end char (default=#)
[SET] LRecl n|*           Set new logical record length when file saved
[SET] MACRO ON|OFF        On means look for macros before subcommands
[SET] MASK Immed [txt]    Define mask used when new lines are inserted
[SET] MASK Define         Show scale on cmdline, you type new mask over it
[SET] MASK Modify         Show current mask on cmdline, type over to modify
[SET] MSGLine OFF         Message line off; pass msgs to CMS for display
[SET] MSGLine ON M[+n|-n] [p] [Overlay]
                          Specify location of message line; allow up to p
                          lines for messages; optionally overlay file line
                          (use line only if msg to show); default=ON 2 2
[SET] MSGMode ON|OFF [Short|Long]
                          Show messages? (when off, use EXTRACT/LASTMSG/)
[SET] NONDisp [c]         Nondisplayable character surrogate (usually=")
[SET] NULls ON|OFF        Replace trailing blanks with nulls (use 3270 Ins)
[SET] NUMber ON|OFF       Number file lines in prefix area (else "=====")
[SET] PAn [BEFORE|AFTER|ONLY|IGNORE] [cmd|NULLKEY|COPYKEY|TABKEY]
[SET] PACK ON|OFF Compress file records when file is saved
[SET] PENDing OFF         Remove pending cmd from prefix area of curline
[SET] PENDing ERROR str   Write "?str" in prefix area of curline
[SET] PENDing ON str      Write "str" in prefix area of curline
[SET] PENDing BLOCK str   Write "str" (block cmd) in prefix area of curline
[SET] PFn [BEFORE|AFTER|ONLY|IGNORE] [cmd|NULLKEY|COPYKEY|TABKEY]
[SET] Point .str [OFF]    Define or delete symbolic name for current line
[SET] PREfix OFF          Remove prefix area from screen
[SET] PREfix ON|Nulls [Left|Right]
                          Enable prefix area; Nulls allows insert
[SET] PREfix Synonym syn cmd
                          Define a prefix synonym for prefix area
[SET] RANge t1 t2         Set line range; all cmds operate just w/in range
[SET] RECFm F|V|FP|VP     Change record format (fixed/variable; packed)
[SET] REMOte ON|OFF       Compress data transmission; see CMS SET REMOTE
[SET] RESERved M[+n|-n] [color] [exthi] [pss] High|Nohigh [text]
                          Reserve n lines (not used for file display)
[SET] RESERved M[+n|-n] Off
                          Un-reserve n lines
[SET] SCALe ON|OFF M[+n|-n]
                          Place/remove scale line; default=ON M+1
[SET] SCOPE Display|All   Act on lines within SET DISPLAY scope; or all
[SET] SCReen n [Horizontal|Vertical]
                          Split screen evenly into n logical screens
[SET] SCReen Size s1 s2 ... sn
                          Split screen horizontally; minimum 5 lines each
[SET] SCReen Width w1 w2 ... wn
                          Split screen vertically; minimum 20 columns each
[SET] SCReen Define s1 w1 h1 v1 ... sn wn hn vn
                          S=lines, W=width, H/V=line/column of upper-left
[SET] SELect [+|-]n [t|1] Assign selection level n to curline thru target
[SET] SERial OFF          Don't update serial area when file saved
[SET] SERial ON|ALL|str [inc [start]]
                          Add serial id to last 8 columns of each file line
[SET] SHADow ON|OFF       Show shadow lines when excluded by SELECT/DISPLAY
[SET] SIDcode [str]       Insert string in every line of an update file
[SET] SPAN OFF            Strings must be on one line to match target
[SET] SPAN ON [Blank|Noblank [n|*]]
                          Concatenate lines when matching target strings;
                          trailing blanks are ignored; BLANK acts as if one
                          blank between lines; n specifies number of lines
                          string can span; default=OFF BLANK 2
[SET] SPILL OFF|ON|WORD   Truncate or spill lines when too long
[SET] STAY OFF|ON         OFF=go to EOF if target not found; ON=stay put
[SET] STReam ON|OFF       Search OFF=curline or ON=entire file for col targ
[SET] SYNonym ON|OFF      Look for synonyms?
[SET] SYNonym [LINEND c] syn [n] cmd
                          Assign synonym to command; use linend char for
                          multiple commands; n=minimum abbreviation chars
[SET] SYNonym [LINEND c] syn [n [fmt1 ... fmtn]] cmd [&1 ... &n]
                          Assign synonym with different operand order than
                          command; fmtn indicates operand formats (& &/ &.
                          &*); &n indicates relative order
[SET] TABLine ON|OFF M[+n|-n]
                          Place/remove tab line; default=OFF -3
[SET] TABS c1 c2 ... cn   Set logical tabs stops; up to 28
[SET] TERMinal Typewriter|Display
                          Use T to force display terminal into line mode
[SET] TEXT ON|OFF         Tell editor and CMS if text keys are available
[SET] TOFEOF ON|OFF       Show top-of-file and end-of-file notice lines
[SET] TRANSLat OFF|c1 c2 c1 c2...
                          Lower/upper translation for non-US terminals
[SET] TRunc n|*           Define truncation column
[SET] VARblank ON|OFF     Make target like /a b/ match text like "a     b"
[SET] Verify ON|OFF       Display all lines changed by subcommands
[SET] Verify [Hex] s1 e1 [Hex] s2 e2 ...
                          Columns numbers (start/end pairs) to display
[SET] WRap ON|OFF         Wrap around past EOF when LOCATE/FIND/etc.
[SET] Zone zone1 zone2|*  Define columns to search for targets

</pre>


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

QUERY Options Available
=======================

<pre>
=           Display the string in the = buffer (last executed command)
ACTion      ON if any action other than displaying or scrolling; else OFF
ALT         Number of alterations to file since last AUTOSAVE and SAVE
APL         APL setting: ON or OFF
ARBchar     Arbitrary character setting: ON or OFF; and the arbchar
AUtosave    AUTOSAVE count, file id, and number of alterations
BASEft      Base filetype specified by XEDIT command or LOAD subcommand
BRKkey      OFF; or ON and the PF or PA key currently set to be the BRKKEY
CASE        Case setting: U=upper or M=mixed; and R=respect or I=ignore
CMDline     Command line setting: ON, OFF, TOP, or BOTTOM
COLOR *|fld Color settings for all or one field (see SET COLOR for fields)
COLPtr      Column pointer display for typewriter terminals: ON or OFF
COLumn      Column number of the column pointer
CTLchar     Display escape character and all control characters
CTLchar c   Display the attributes of one control character
CURLine     Line number of current line
CURSor      Position of cursor on screen (row,col) and in file (line,col)
DISPLay     Range of selection levels included in display
EDIRName    Name of SFS directory containing file when it was first loaded
EFMode      Two-character filemode of file when it was first loaded
EFName      Eight-character filename of file when it was first loaded
EFType      Eight-character filetype of file when it was first loaded
ENTer       BEFORE, AFTER, ONLY, or IGNORE; and the enter key definition
EOF         End of file: ON if line pointer at EOF (or EORange); else OFF
EOL         End of line: ON if column pointer at zone2+1; else OFF
ESCape      ON or OFF; and the escape character
ETARBCH     ON or OFF; and the extended arbitrary character
ETMODE      Extended mode (DBCS): ON or OFF
FILler      Display the filler character
FMode       Display the two-character filemode
FName       Display the eight-character filename
FType       Display the eight-character filetype
FULLread    Sense null characters: ON or OFF
HEX         Allow hex in strings and targets: ON or OFF
IMage       Tab and backspace handing during input: ON, OFF, or CANON
IMPcmscp    Implicit CMS/CP: ON or OFF
LASTLorc    Display contents of last-locate-or-change buffer
LASTmsg     Display last message issued by editor
LENgth      Length of current line (col 1 thru trunc, excl trail blanks)
LIBName     Display library filename when MEMBER is ON
LIBType     Display library filetype when MEMBER is ON
LIne        Current line number, relative to beginning of file
LINENd      ON or OFF; and the line-end character
LRecl       Logical record length of the file
LScreen     Logical screen info (six integers): number of lines/columns in
              logical screen; line/column numbers of top-left corner of
              logical on virtual; number of lines/columns in virtual screen
MACRO       Look for macros before subcommands: ON or OFF
MASK        Display the mask line
MEMber      ON if editing member of a CMS library; or OFF
MSGLine     ON or OFF; location of message line; number lines [; OVERLAY]
MSGMode     ON, LONG, or SHORT (nothing displayed when MSGMODE OFF)
NBFile      Number of files in ring
NONDisp     Non-displayable character surrogate
NULls       Replace trailing blanks with nulls: ON or OFF
NUMber      Number file lines in prefix area: ON or OFF
PA[n|*]     One or all PA key definitions; BEFORE, AFTER, ONLY, or IGNORE
PACK        Compress file records when file is saved: ON or OFF
PENDing [BLOCK] [OLDNAME] name|*
            First entry in pending list with name, or all entries
            Response: Line n: 'name',Oldname='name',OP1='x',OP2='y',OP3='z'
PF[n|*]     One or all PF key definitions; BEFORE, AFTER, ONLY, or IGNORE
Point [*]   Display names associated with current line; * means all lines
PREfix      Prefix area display state: ON, OFF, or NULLS; LEFT or RIGHT
PREfix Synonym name|*
            Definition of specified synonym; or all synonym definitions
RANge       Line numbers of top and bottom of range
RECFm       Record format: F, V, FP, or VP
REMote      Compress data transmission: ON or OFF
RESERved    Line numbers of reserved screen lines
RING        Number of files being edited; fileid line for each
SCALe       ON or OFF; position of scale line on screen
SCOPE       Act on lines within SET DISPLAY scope: DISPLAY or ALL
SCReen      SIZE, WIDTH, or DEFINE; sizes of screens
SELect      Selection level of current line; maximum level for the file
Seq8        NOSEQ8 option: ON or OFF
SERial      Serial identification; increment value; starting value
SHADow      Show shadow lines: ON or OFF
SIDcode     Eight-character SIDCODE string
SIZe        Number of records in file being edited
SPAN        ON or OFF; B(=blank) or N(=noblank); number of lines
SPILL       Spill or truncate lines when too long: ON, OFF, or WORD
STAY        Stay put if target not found: ON or OFF
STReam      Search entire file for column targets: ON or OFF
SYNonym     Look for synonyms: ON or OFF
SYNonym name|*
            Synonym name, minimum abbreviation, and definition
TABLine     ON or OFF; position of tab line on screen
TABS        Tab column numbers
TARGet      Line/column of first char; line/column of last char
TERMinal    Type of terminal: DISPLAY or TYPEWRITER
TEXT        Text keys available: ON or OFF
TOF         At top-of-file: ON or OFF
TOFEOF      Show TOF and EOF notice lines: ON or OFF
TOL         At top-of-line: ON or OFF
TRANSlat    Lower/upper translation for non-US terminals: ON or OFF
TRunc       Truncation column number
UNIQueid    Unique identifier associated with file (see AUTOSAVE)
UNTil       File type up through which file updates were applied
UPDate      UPDATE option: ON or OFF
VARblank    Make target like /a b/ match text like "a     b": ON of OFF
Verify      ON or OFF; verification column numbers
VERShift    n or -n: relative position of screen over file (see LEFT/RIGHT)
WIDTH       WIDTH option value from XEDIT command or LOAD subcommand
WRap        Wrap around past EOF when LOCATE/FIND/etc.: ON or OFF
Zone        Left and right zone column numbers
</pre>
