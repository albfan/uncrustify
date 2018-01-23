[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Spaces for Parenthesis
----------------------

+-----------------------------------------------------------------------+
|     void f1(█)                                                        |
|     {                                                                 |
|         auto a =                                                      |
|         [=]█(█int *a, Something b█)                                   |
|         {                                                             |
|             // ...                                                    |
|         };                                                            |
|     }                                                                 |
|     void foo(█int key, int value█)                                    |
|     {                                                                 |
|         a = (█b + c█);                                                |
|         a = B(█(c) + (d)█);                                           |
|         return A(█key, value█) + B(█);                                |
|     }                                                                 |
|     }                                                                 |
|     class STDMETHOD                                                   |
|     {                                                                 |
|        STDMETHOD(GetValues)█(BSTR bsName, REFDATA** pData);           |
|     };                                                                |
|     void (__attribute__(█(noreturn)█) ****f) (void);                  |
|                                                                       |
|     char *__attribute__(█(aligned(8)█)█) *f;                          |
|                                                                       |
|     (struct foo)█{...}                                                |
|                                                                       |
|     typedef const char *█(*somefunc_t)(void *barstool);               |
|                                                                       |
|                                                                       |
|                                                                       |
|                                                                       |
|                                                                       |
|     if█(█a█)█{ b = 13; }                                              |
|                                                                       |
|                                                                       |
|                                                                       |
|     █                                                                 |
+-----------------------------------------------------------------------+

Register (part 1)
=================

  ---------------------------------------------------------- -------------------------------------------------------------------------------------------------
  [sp\_cpp\_lambda\_paren](#sp_cpp_lambda_paren)             Add or remove space after the capture specification in C++11 lambda.
  [sp\_inside\_paren](#sp_inside_paren)                      Add or remove space inside \'(\' and \')\'.
  [sp\_cparen\_oparen](#sp_cparen_oparen)                    Add or remove space between back-to-back parens: \')(\' vs \') (\'.
  [sp\_balance\_nested\_parens](#sp_balance_nested_parens)   Whether to balance spaces inside nested parens.
  [sp\_paren\_paren](#sp_paren_paren)                        Add or remove space between nested parens: \'((\' vs \') )\'.
  [sp\_paren\_brace](#sp_paren_brace)                        Add or remove space between \')\' and \'{\'.
  [sp\_ptr\_star\_paren](#sp_ptr_star_paren)                 Add or remove space after a pointer star \'\*\', if followed by an open paren (function types).
  [sp\_before\_sparen](#sp_before_sparen)                    Add or remove space before \'(\' of \'if\', \'for\', \'switch\', \'while\', etc.
  [sp\_inside\_sparen](#sp_inside_sparen)                    )Add or remove space inside if-condition \'(\' and \')\'.
  [sp\_inside\_sparen\_close](#sp_inside_sparen_close)       )Add or remove space before if-condition \')\'. Overrides sp\_inside\_sparen.
  [sp\_inside\_sparen\_open](#sp_inside_sparen_open)         )Add or remove space after if-condition \'(\'. Overrides sp\_inside\_sparen.
  [sp\_after\_sparen](#sp_after_sparen)                      )Add or remove space after \')\' of \'if\', \'for\', \'switch\', and \'while\', etc.
  ---------------------------------------------------------- -------------------------------------------------------------------------------------------------

Register (part 2) TODO
======================

  ------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------
  [sp\_sparen\_brace](#sp_sparen_brace)                         \#(64)Add or remove space between \')\' and \'{\' of \'if\', \'for\', \'switch\', and \'while\', etc.

  [sp\_invariant\_paren](#sp_invariant_paren)                   \#(65)Add or remove space between \'invariant\' and \'(\' in the D language.

  [sp\_after\_invariant\_paren](#sp_after_invariant_paren)      \#(66)Add or remove space after the \')\' in \'invariant (C) c\' in the D language.

  [sp\_sizeof\_paren](#sp_sizeof_paren)                         \#(95)Add or remove space between \'sizeof\' and \'(\'.

  [sp\_func\_proto\_paren](#sp_func_proto_paren)                \#(106)Add or remove space between function name and \'(\' on function declaration.

  [sp\_func\_proto\_paren\_empty](#sp_func_proto_paren_empty)   \#(107)Add or remove space between function name and \'()\' on function declaration without parameters.

  [sp\_func\_def\_paren](#sp_func_def_paren)                    \#(108)Add or remove space between function name and \'(\' on function definition.

  [sp\_func\_def\_paren\_empty](#sp_func_def_paren_empty)       \#(109)Add or remove space between function name and \'()\' on function definition without parameters.

  [sp\_inside\_fparens](#sp_inside_fparens)                     Add or remove space inside function \'()\'.

  [sp\_inside\_fparen](#sp_inside_fparen)                       Add or remove space inside function \'(\' and \')\'.

  [sp\_inside\_tparen](#sp_inside_tparen)                       \#(112)Add or remove space inside the first parens in the function type: \'void (\*x)(\...)\'.

  [sp\_after\_tparen\_close](#sp_after_tparen_close)            \#(113)Add or remove between the parens in the function type: \'void (\*x)(\...)\'.

  [sp\_fparen\_brace](#sp_fparen_brace)                         \#(115)Add or remove space between \')\' and \'{\' of function.

  [sp\_fparen\_dbrace](#sp_fparen_dbrace)                       \#(116)Java: Add or remove space between \')\' and \'{{\' of double brace initializer.

  [sp\_func\_call\_paren](#sp_func_call_paren)                  \#(117)Add or remove space between function name and \'(\' on function calls.

  [sp\_func\_call\_paren\_empty](#sp_func_call_paren_empty)     \#(118)Add or remove space between function name and \'()\' on function calls without parameters.

  [sp\_func\_call\_user\_paren](#sp_func_call_user_paren)       (119)Add or remove space between the user function name and \'(\' on function calls\
                                                                You need to set a keyword to be a user function, like this: \'set func\_call\_user \_\' in the config file.

  [sp\_return\_paren](#sp_return_paren)                         \#(122)Add or remove space between \'return\' and \'(\'.

  [sp\_attribute\_paren](#sp_attribute_paren)                   \#(123)Add or remove space between \'\_\_attribute\_\_\' and \'(\'.

  [sp\_defined\_paren](#sp_defined_paren)                       \#(124)Add or remove space between \'defined\' and \'(\' in \'\#if defined (FOO)\'.

  [sp\_throw\_paren](#sp_throw_paren)                           \#(125)Add or remove space between \'throw\' and \'(\' in \'throw (something)\'.

  [sp\_catch\_paren](#sp_catch_paren)                           \#(127)Add or remove space between \'catch\' and \'(\' in \'catch (something) { }\'\
                                                                If set to ignore, sp\_before\_sparen is used.

  [sp\_version\_paren](#sp_version_paren)                       \#(128)Add or remove space between \'version\' and \'(\' in \'version (something) { }\' (D language)\
                                                                If set to ignore, sp\_before\_sparen is used.

  [sp\_scope\_paren](#sp_scope_paren)                           \#(129)Add or remove space between \'scope\' and \'(\' in \'scope (something) { }\' (D language)\
                                                                If set to ignore, sp\_before\_sparen is used.

  [sp\_super\_paren](#sp_super_paren)                           \#(130)Add or remove space between \'super\' and \'(\' in \'super (something)\'. Default=Remove.

  [sp\_this\_paren](#sp_this_paren)                             \#(131)Add or remove space between \'this\' and \'(\' in \'this (something)\'. Default=Remove.

  [sp\_extern\_paren](#sp_extern_paren)                         \#(183)Control the spacing in \'extern (C)\' (D).

  [sp\_annotation\_paren](#sp_annotation_paren)                 \#(196)Control space between a Java annotation and the open paren.
  ------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------
