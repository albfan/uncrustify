[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Spaces
------

You want to \"add/ force/ ignore/ remove\" a

-   [space for assign](options_Space_Assign.md)
-   [space for byref](options_Space_Byref.md)
-   [space for case](options_Space_Case.md)
-   [space for cast](options_Space_Cast.md)
-   [space for class](options_Space_Class.md)
-   [space for comma](options_Space_Comma.md)
-   [space for enum](options_Space_Enum.md)
-   [space for for loop](options_Space_For.md)
-   [space for new/ delete](options_Space_New.md)
-   [space for operator](options_Space_Operator.md)
-   [space for parenthesis](options_Space_Paren.md)
-   [space for template](options_Space_Template.md)

at some places.

Some more options\...

+-----------------------------------------------------------------------+
|     // Comments                                                       |
|       ^                                                               |
|     int a;            /* emb cmt */ int b;            // trailing cmt |
|           ^..........^                    ^..........^                |
|                                                                       |
|         union {                                                       |
|             uint maxChars;                                            |
|             uint maxBytes;                                            |
|         } mLength;                                                    |
|         union { int m_size; int m_any; };                             |
|                ^                      ^                               |
|         return { -1, -1, -1 };                                        |
|                 ^          ^                                          |
|                                                                       |
|     class Parser :: ParserPrivate { };                                |
|                 ^  ^               ^                                  |
|     template <typename T> class to { };                               |
|                                     ^                                 |
|     my $all = { };                                                    |
|                ^                                                      |
|     enum FocusEffect { };                                             |
|                       ^                                               |
|     struct error { };                                                 |
|                   ^                                                   |
|     };                                                                |
|                                                                       |
|     #define LOG_FMT (sev, args ...) \                                 |
|                    ^          ^                                       |
|        do { if (log_sev_on(sev)) { log_fmt(sev, ## args); } } while ( |
| 0)                                                                    |
|                                                ^  ^                   |
|     #endif                                                            |
|     #define FS_NOCOW_FL 0x00800000                                    |
|                        ^                                              |
|     #define STRHACK(x) HACKSTR(x)                                     |
|                  ^                                                    |
|     #define wakeUpCaller(cond) \                                      |
|                               ^                                       |
|         if (cond) { \                                                 |
|                    ^                                                  |
|             cond->release(); \                                        |
|                             ^                                         |
|          }                                                            |
|     typedef struct { int val; int sel; } DiceInfo;                    |
|                                         ^                             |
|     void * bar()                                                      |
|         ^ ^                                                           |
|     {                                                                 |
|         int a = 5;                                                    |
|              ^ ^                                                      |
|              ^ ^                                                      |
|         c = a + b;                                                    |
|              ^ ^                                                      |
|         a = ~ b;                                                      |
|              ^                                                        |
|         x = - 5;                                                      |
|              ^                                                        |
|         y = + 7;                                                      |
|              ^                                                        |
|         (-- a);                                                       |
|            ^                                                          |
|         i ++;                                                         |
|          ^                                                            |
|         b = ( a == d ) ? 55 : 88;                                     |
|                       ^ ^  ^ ^                                        |
|                       ^ ^  ^ ^                                        |
|         b = ( a == d ) ? : 88;                                        |
|                         ^                                             |
|         if( ( a || b ) && c ) x = 1;                                  |
|                ^  ^   ^  ^                                            |
|              ^      ^      ^                                          |
|            ^                                                          |
|         c = a > b;                                                    |
|              ^ ^                                                      |
|         int * i;                                                      |
|            ^ ^                                                        |
|            ^                                                          |
|         int * * j;                                                    |
|              ^                                                        |
|         throw (x);                                                    |
|              ^                                                        |
|         try {                                                         |
|            ^                                                          |
|         } catch (const Exception &e) { }                              |
|          ^     ^                                                      |
|         } catch (...) { }                                             |
|          ^     ^                                                      |
|         } catch { }                                                   |
|          ^     ^                                                      |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| []{#sp_before_comma}[]{#sp_after_comma}[]{#sp_before_squares}         |
|                                                                       |
|     int main(int argc , char *argv [])                                |
|                      ^ ^          ^                                   |
|     {                                                                 |
|         int a [2];                                                    |
|              ^                                                        |
|         a[ n ] = 3;                                                   |
|           ^ ^                                                         |
|         const char *names [] =                                        |
|                          ^                                            |
|         {                                                             |
|             "{ False , True }",                                       |
|                     ^ ^                                               |
|             "{ Ignore, Add, Remove, Force }",                         |
|                                                                       |
|         return (-1);                                                  |
|               ^                                                       |
|                                                                       |
|                                                                       |
|     int a ( );                                                        |
|          ^ ^                                                          |
|     int a (int b) {}                                                  |
|          ^       ^                                                    |
|     void ( int a ) ( int b );                                         |
|           ^     ^ ^ ^     ^                                           |
|     static void sockaddr_unmapped(                                    |
|         struct sockaddr *sa __attribute__ ((unused)),                 |
|                                          ^                            |
|         socklen_t *len __attribute__ ((unused)))                      |
|                                     ^                                 |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| []{#sp_template_angle}[]{#sp_before_angle}[]{#sp_inside_angle}[]{#sp_ |
| after_angle}                                                          |
|                                                                       |
|     template < typename T > inline static bool remove(T column)       |
|             ^ ^          ^                                            |
|             ^              ^                                          |
|                                                                       |
| []{#sp_before_byref_func}[]{#sp_after_byref_func}[]{#sp_before_byref} |
| []{#sp_after_byref}[]{#sp_before_unnamed_byref}                       |
|                                                                       |
|     int & a(int & b);                                                 |
|        ^ ^     ^ ^                                                    |
|     int c(int &)                                                      |
|        ^     ^                                                        |
|     {                                                                 |
|         d = aa (& y,& d) ;                                            |
|               ^  ^   ^  ^                                             |
|             e = ee ();                                                |
|                   ^                                                   |
|         if ( a == 5 ) ...                                             |
|           ^                                                           |
|                 ^      ^                                              |
|                 ^      ^                                              |
|                 ...                                                   |
|             if (b) ;                                                  |
|                   ^                                                   |
|         if ( a == 6 ) b = 66;                                         |
|                          ^                                            |
|         if ( a == 7 ) { b = 77; }                                     |
|                          ^                                            |
|             if (! a) {                                                |
|                  ^                                                    |
|                 b = 4;                                                |
|             } else {                                                  |
|              ^    ^                                                   |
|                 b = 5;                                                |
|             }                                                         |
|             for(a = 1 ; a < b ; a++) {                                |
|                      ^       ^                                        |
|                ...                                                    |
|         for( ; ; ) {                                                  |
|                 ^ ^ ^                                                 |
|                ...                                                    |
|         switch (whatIsToDo) ...                                       |
|               ^                                                       |
|         while (start < end) ...                                       |
|              ^                                                        |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| []{#sp_word_brace_ns}                                                 |
|                                                                       |
|     namespace Server {                                                |
|                     ^                                                 |
|     class Cache : public QObject                                      |
|                ^ ^                                                    |
|     Cache::StorageDebugger ()                                         |
|                           ^                                           |
|         : mFile(0)                                                    |
|        ^ ^                                                            |
|     {                                                                 |
|             new service;                                              |
|                ^                                                      |
|             delete service;                                           |
|                   ^                                                   |
|             delete[] buffer;                                          |
|                     ^                                                 |
|             if (this == & other) return * this;                       |
|                          ^               ^                            |
|             switch (a) {                                              |
|             case 1 :                                                  |
|                   ^                                                   |
|                     b= 1;                                             |
|                     break;                                            |
|             case 2 : {                                                |
|                     b = 2;                                            |
|                     break;                                            |
|             }                                                         |
|             default :                                                 |
|                     break;                                            |
|             }                                                         |
|             bool operator () (Entity::Id lhs, Entity::Id rhs) const   |
|             ...          ^  ^                                         |
|                                                                       |
|             a = ( int ) 5.6;                                          |
|                  ^   ^ ^                                              |
|             cpp = int (7);                                            |
|                      ^                                                |
|             len = sizeof (int);                                       |
|                         ^                                             |
|             SomeStruct a = SomeStruct {1, 2, 3};                      |
|                                      ^                                |
|         someFuncCall(SomeStruct {4, 5, 6});                           |
|                                ^                                      |
|             log . foo . bar = 5;                                      |
|                ^ ^   ^ ^                                              |
|         other -> foo -> bar = 123;                                    |
|              ^  ^   ^  ^                                              |
|     }                                                                 |
|     /// doxygen sequence                                              |
|        ^                                                              |
|     ///< doxygen sequence                                             |
|         ^                                                             |
|     //! doxygen sequence                                              |
|        ^                                                              |
|     //!< doxygen sequence                                             |
|         ^                                                             |
|     #if A                                                             |
|     #else /* Comment A */                                             |
|          ^                                                            |
|     #endif /* Comment B */                                            |
|           ^                                                           |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| []{#sp_assign_default}                                                |
|                                                                       |
|     void Initialize( BYTE nDelay = 100 );                             |
|                                 ^ ^                                   |
|     void f1()                                                         |
|     {                                                                 |
|           auto a = [ = ] (int *a, Something & b)                      |
|                     ^ ^ ^                                             |
|                                                                       |
|           list[idx] (param);                                          |
|                    ^                                                  |
|                                                                       |
|     double foo()                                                      |
|     {                                                                 |
|         return( foo(n) );                                             |
|                ^      ^                                               |
|                                                                       |
|                                                                       |
|     Vector2<double> ()                                                |
|                    ^                                                  |
|                                                                       |
|     {                                                                 |
|             List<byte> bob = new List<byte> ();                       |
|                       ^                                               |
|             QVector<QPair<Condition, QString> > mWhenThen;            |
|                                              ^                        |
|                                                                       |
|     template<int i, int ... Indexes, typename IdxHolder, typename ... |
|  Elements>                                                            |
|                        ^                                         ^    |
|     struct index_holder_impl<i, index_holder<Indexes ...>, IdxHolder, |
|  Elements ...>                                                        |
|                                                     ^                 |
|          ^                                                            |
|     {                                                                 |
|         typedef typename index_holder_impl<i + 1, index_holder<Indexe |
| s ... i>, Elements ...>::type type;                                   |
|                                                                       |
|  ^                 ^                                                  |
+-----------------------------------------------------------------------+

Register
========

[sp\_addr](#sp_addr)

[sp\_after\_angle](#sp_after_angle)

[sp\_after\_assign](#sp_after_assign)

[sp\_after\_byref\_func](#sp_after_byref_func)

[sp\_after\_byref](#sp_after_byref)

sp\_inside\_angle

[sp\_after\_cast](#sp_after_cast)

[sp\_after\_class\_colon](#sp_after_class_colon)

[sp\_after\_comma](#sp_after_comma)

[sp\_after\_constr\_colon](#sp_after_constr_colon)

[sp\_after\_dc](#sp_after_dc)

[sp\_after\_new](#sp_after_new)

[sp\_after\_operator](#sp_after_operator)

[sp\_after\_operator\_sym](#sp_after_operator_sym)

[sp\_after\_ptr\_star\_func](#sp_after_ptr_star_func)

[sp\_after\_ptr\_star](#sp_after_ptr_star)

[sp\_after\_semi\_for\_empty](#sp_after_semi_for_empty)

[sp\_after\_semi\_for](#sp_after_semi_for)

[sp\_after\_sparen](#sp_after_sparen)

[sp\_angle\_paren](#sp_angle_paren)

[sp\_angle\_word](#sp_angle_word)

[sp\_arith](#sp_arith)

[sp\_assign\_default](#sp_assign_default)

[sp\_assign](#sp_assign)

[sp\_attribute\_paren](#sp_attribute_paren)

[sp\_balance\_nested\_parens](#sp_balance_nested_parens)

[sp\_before\_angle](#sp_before_angle)

[sp\_before\_assign](#sp_before_assign)

[sp\_before\_byref\_func](#sp_before_byref_func)

[sp\_before\_byref](#sp_before_byref)

[sp\_before\_case\_colon](#sp_before_case_colon)

[sp\_before\_class\_colon](#sp_before_class_colon)

[sp\_before\_comma](#sp_before_comma)

[sp\_before\_constr\_colon](#sp_before_constr_colon)

[sp\_before\_dc](#sp_before_dc)

[sp\_before\_ellipsis(1)](#sp_before_ellipsis_1)

[sp\_before\_ellipsis(2)](#sp_before_ellipsis_2)

[sp\_before\_nl\_cont](#sp_before_nl_cont)

[sp\_before\_ptr\_star\_func](#sp_before_ptr_star_func)

[sp\_before\_ptr\_star](#sp_before_ptr_star)

[sp\_before\_semi\_for\_empty](#sp_before_semi_for_empty)

[sp\_before\_semi\_for](#sp_before_semi_for)

[sp\_before\_semi](#sp_before_semi)

[sp\_before\_sparen](#sp_before_sparen)

[sp\_before\_square](#sp_before_square)

[sp\_before\_squares](#sp_before_squares)

[sp\_before\_tr\_emb\_cmt](#sp_before_tr_emb_cmt)

[sp\_before\_unnamed\_byref](#sp_before_unnamed_byref)

[sp\_before\_ptr\_star](#sp_before_unnamed_ptr_star)

[sp\_between\_ptr\_star](#sp_between_unnamed_ptr_star)

[sp\_bool](#sp_bool)

[sp\_brace\_catch](#sp_brace_catch)

[sp\_brace\_else](#sp_brace_else)

[sp\_brace\_typedef](#sp_brace_typedef)

[sp\_catch\_brace](#sp_catch_brace)

[sp\_catch\_paren](#sp_catch_paren)

[sp\_cmt\_cpp\_doxygen](#sp_cmt_cpp_doxygen)

[sp\_cmt\_cpp\_start](#sp_cmt_cpp_start)

[sp\_compare](#sp_compare)

[sp\_cond\_colon\_after](#sp_cond_colon_after)

[sp\_cond\_colon\_before](#sp_cond_colon_before)

[sp\_cond\_colon](#sp_cond_colon)

[sp\_cond\_question\_after](#sp_cond_question_after)

[sp\_cond\_question\_before](#sp_cond_question_before)

[sp\_cond\_question](#sp_cond_question)

[sp\_cond\_ternary\_short](#sp_cond_ternary_short)

[sp\_cpp\_cast\_paren](#sp_cpp_cast_paren)

[sp\_cpp\_lambda\_assign](#sp_cpp_lambda_assign)

[sp\_defined\_paren](#sp_defined_paren)

[sp\_deref](#sp_deref)

[sp\_else\_brace](#sp_else_brace)

[sp\_endif\_cmt](#sp_endif_cmt)

[sp\_enum\_after\_assign](#sp_enum_after_assign)

[sp\_enum\_assign](#sp_enum_assign)

[sp\_enum\_before\_assign](#sp_enum_before_assign)

[sp\_fparen\_brace](#sp_fparen_brace)

[sp\_func\_call\_paren\_empty](#sp_func_call_paren_empty)

[sp\_func\_call\_paren](#sp_func_call_paren)

[sp\_func\_class\_paren](#sp_func_class_paren)

[sp\_func\_def\_paren](#sp_func_def_paren)

[sp\_func\_proto\_paren](#sp_func_proto_paren)

[sp\_incdec](#sp_incdec)

[sp\_inside\_angle](#sp_inside_angle)

[sp\_inside\_braces\_empty](#sp_inside_braces_empty)

[sp\_inside\_braces\_enum](#sp_inside_braces_enum)

[sp\_inside\_braces](#sp_inside_braces)

[sp\_inside\_braces\_struct](#sp_inside_braces_struct)

[sp\_inside\_fparen](#sp_inside_fparen)

[sp\_inside\_fparens](#sp_inside_fparens)

[sp\_inside\_paren\_cast](#sp_inside_paren_cast)

[sp\_inside\_paren](#sp_inside_paren)

[sp\_inside\_sparen\_close](#sp_inside_sparen_close)

[sp\_inside\_sparen\_open](#sp_inside_sparen_open)

[sp\_inside\_sparen](#sp_inside_sparen)

[sp\_inside\_square](#sp_inside_square)

[sp\_inside\_tparen](#sp_inside_tparen)

[sp\_inv](#sp_inv)

[sp\_macro\_func](#sp_macro_func)

[sp\_macro](#sp_macro)

[sp\_member](#sp_member)

[sp\_not](#sp_not)

[sp\_num\_before\_tr\_emb\_cmt](#sp_num_before_tr_emb_cmt)

[sp\_paren\_paren](#sp_paren_paren)

[sp\_permit\_cpp11\_shift](#sp_permit_cpp11_shift)

[sp\_pp\_concat](#sp_pp_concat)

[sp\_return\_paren](#sp_return_paren)

[sp\_sign](#sp_sign)

[sp\_sizeof\_paren](#sp_sizeof_paren)

[sp\_sparen\_brace](#sp_sparen_brace)

[sp\_special\_semi](#sp_special_semi)

[sp\_square\_fparen](#sp_square_fparen)

[sp\_template\_angle](#sp_template_angle)

[sp\_throw\_paren](#sp_throw_paren)

[sp\_try\_brace](#sp_try_brace)

[sp\_type\_func](#sp_type_func)

[sp\_word\_brace\_ns](#sp_word_brace_ns)

[sp\_word\_brace](#sp_word_brace)

not yet shown
-------------

sp\_after\_for\_colon\
sp\_after\_ptr\_star\_qualifier\
sp\_after\_semi\
sp\_after\_throw\
sp\_after\_type\
sp\_angle\_shift\
sp\_before\_for\_colon\
sp\_before\_pp\_stringify\
sp\_case\_label\
sp\_cparen\_oparen\
sp\_cpp\_lambda\_paren\
sp\_func\_call\_user\_paren\
sp\_paren\_comma\

only for C\#
------------

sp\_after\_mdatype\_commas\
sp\_before\_mdatype\_commas\
sp\_between\_mdatype\_commas\
sp\_between\_new\_paren\
sp\_getset\_brace\

only for D
----------

sp\_before\_template\_paren\
sp\_d\_array\_colon\
sp\_extern\_paren\
sp\_invariant\_paren\
sp\_range\
sp\_scope\_paren\
sp\_version\_paren\

only for Java
-------------

sp\_annotation\_paren\
sp\_fparen\_dbrace\

only for Pawn
-------------

sp\_after\_tag\

only for oc
-----------

sp\_after\_oc\_at\_sel\
sp\_after\_oc\_at\_sel\_parens\
sp\_after\_oc\_block\_caret\
sp\_after\_oc\_colon\
sp\_after\_oc\_dict\_colon\
sp\_after\_oc\_msg\_receiver\
sp\_after\_oc\_property\
sp\_after\_oc\_return\_type\
sp\_after\_oc\_scope\
sp\_after\_oc\_type\
sp\_after\_send\_oc\_colon\
sp\_before\_oc\_block\_caret\
sp\_before\_oc\_colon\
sp\_before\_oc\_dict\_colon\
sp\_before\_send\_oc\_colon\
sp\_enum\_paren\
sp\_inside\_oc\_at\_sel\_parens\
sp\_paren\_brace\
sp\_ptr\_star\_paren\

not C
-----

sp\_brace\_finally\
sp\_finally\_brace\
