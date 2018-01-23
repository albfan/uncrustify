[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Spaces for operator
-------------------

+-----------------------------------------------------------------------+
|     {                                                                 |
|        bool operator█()█(T1 const t1, T2 const t2)                    |
|        {                                                              |
|           ...                                                         |
|        }                                                              |
|        unc_text operator =█()                                         |
|        {                                                              |
|           ...                                                         |
|        }                                                              |
|     }                                                                 |
+-----------------------------------------------------------------------+

Register
========

  ----------------------------------------------------------------- ---------------------------------------------------------------------------------------------
  [sp\_after\_operator](#sp_after_operator)                         Add or remove space between \'operator\' and operator sign.

  [sp\_after\_operator\_sym](#sp_after_operator_sym)                Add or remove space between the operator symbol and the open paren, as in \'operator ++(\'.

  [sp\_after\_operator\_sym\_empty](#sp_after_operator_sym_empty)   Add or remove space between the operator symbol and the open paren when the operator\
                                                                    has no arguments, as in \'operator \*()\'.\
                                                                    Have precedence of sp\_after\_operator\_sym.
  ----------------------------------------------------------------- ---------------------------------------------------------------------------------------------
