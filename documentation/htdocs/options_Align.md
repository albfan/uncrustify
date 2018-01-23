\#define SUCCESS 0 \^ align\_pp\_define\_gap The minimum space between
label and value of a preprocessor define \#define set\_chunk\_type(pc,
tt) do { \\ LOG\_FUNC\_CALL(); \\ set\_chunk\_type\_real((pc), (tt)); \\
} while (false) align\_nl\_cont = true \#define LOG\_STR(sev, str, len)
\\ do { if (log\_sev\_on(sev)) { log\_str(sev, str, len); } } while (0)
\^ nl\_after\_brace\_close extern struct cp\_data cpd; extern bool
QT\_SIGNAL\_SLOT\_found; extern int QT\_SIGNAL\_SLOT\_level; extern bool
restoreValues; align\_var\_def\_span \^ enum argval\_t { AV\_IGNORE = 0,
AV\_ADD = 1, AV\_REMOVE = 2, AV\_FORCE = 3, /\*\*\< remove + add \*/
AV\_NOT\_DEFINED = 4 /\* to be used with QT, SIGNAL SLOT macros \*/ };
\^ align\_var\_struct\_span UO\_indent\_var\_def\_blk, // indent a
variable def block that appears at the top UO\_indent\_var\_def\_cont,
UO\_indent\_shift, // if a shift expression spans multiple lines, indent
UO\_indent\_min\_vbrace\_open, // min. indent after virtual brace open
and newline UO\_indent\_vbrace\_open\_on\_tabstop, // when identing
after virtual brace open and newline add further spaces to reach next
tabstop align\_right\_cmt\_span
