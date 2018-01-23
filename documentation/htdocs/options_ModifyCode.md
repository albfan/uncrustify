[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Code modifying
--------------

+-----------------------------------------------------------------------+
|     namespace a::b                                                    |
|     {                                                                 |
|     int foo::bar()                                                    |
|     {                                                                 |
|         switch(xx) {                                                  |
|         case 1:                                                       |
|             do { ++i; } while (++cnt < 1000);                         |
|                ^      ^                                               |
|             for (i = 0; i < 5; i++) { bar(i); }                       |
|                                     ^         ^                       |
|             if (a != b) {                                             |
|                         ^                                             |
|                         ^                                             |
|                         ^                                             |
|                x = a;                                                 |
|                if (c == d)                                            |
|                           ^                                           |
|                   y = 5;                                              |
|             }                                                         |
|             ^                                                         |
|             ^                                                         |
|             ^                                                         |
|             while (a == b)                                            |
|                           ^                                           |
|                 c++;                                                  |
|             ^                                                         |
|             if (( a < b) && ( b > c)) {                               |
|                 ^      ^    ^      ^                                  |
|             return (nCount);                                          |
|                    ^      ^                                           |
|             if (a) {                                                  |
|                 foo();;                                               |
|                       ^                                               |
|             };                                                        |
|              ^                                                        |
|             break;                                                    |
|         case 2: {                                                     |
|                 int b;                                                |
|                 b = 2;                                                |
|             }                                                         |
|             ^                                                         |
|             break;                                                    |
|             ^                                                         |
|         default:                                                      |
|             handle_the_rest();                                        |
|             break;                                                    |
|         } // switch                                                   |
|           ^                                                           |
|     } // foo::bar                                                     |
|       ^                                                               |
|     } // namespace a::b                                               |
|       ^                                                               |
|                                                                       |
|     void a()                                                          |
|     {                                                                 |
|         return;                                                       |
|         ^                                                             |
|     }                                                                 |
+-----------------------------------------------------------------------+

Register
========

  -------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------
  [mod\_add\_long\_function\_closebrace\_comment](#mod_add_long_function_closebrace_comment)   [mod\_add\_long\_ifdef\_else\_comment](#mod_add_long_ifdef_else_comment)
  [mod\_add\_long\_ifdef\_endif\_comment](#mod_add_long_ifdef_endif_comment)                   [mod\_add\_long\_namespace\_closebrace\_comment](#mod_add_long_namespace_closebrace_comment)
  [mod\_add\_long\_switch\_closebrace\_comment](#mod_add_long_switch_closebrace_comment)       [mod\_case\_brace](#mod_case_brace)
  [mod\_full\_brace\_do](#mod_full_brace_do)                                                   [mod\_full\_brace\_for](#mod_full_brace_for)
  [mod\_full\_brace\_function](#mod_full_brace_function)                                       [mod\_full\_brace\_if\_chain](#mod_full_brace_if_chain)
  [mod\_full\_brace\_if](#mod_full_brace_if)                                                   [mod\_full\_brace\_nl](#mod_full_brace_nl)
  [mod\_full\_brace\_using](#mod_full_brace_using)                                             [mod\_full\_brace\_while](#mod_full_brace_while)
  [mod\_full\_paren\_if\_bool](#mod_full_paren_if_bool)                                        [mod\_move\_case\_break](#mod_move_case_break)
  [mod\_paren\_on\_return](#mod_paren_on_return)                                               [mod\_pawn\_semicolon](#mod_pawn_semicolon)
  [mod\_remove\_empty\_return](#mod_remove_empty_return)                                       [mod\_remove\_extra\_semicolon](#mod_remove_extra_semicolon)
  [mod\_sort\_import](#mod_sort_import)                                                        [mod\_sort\_include](#mod_sort_include)
  [mod\_sort\_using](#mod_sort_using)                                                          
  -------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------

not yet shown
-------------

mod\_full\_brace\_using\
mod\_add\_long\_ifdef\_endif\_comment\
mod\_add\_long\_ifdef\_else\_comment\
mod\_sort\_include\

only for Pawn
-------------

mod\_full\_brace\_function\
mod\_pawn\_semicolon\

only for Java
-------------

mod\_sort\_import\

only for C\#
------------

mod\_sort\_using\
