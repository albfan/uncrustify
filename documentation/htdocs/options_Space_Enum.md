[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Spaces for enum
---------------

+-----------------------------------------------------------------------+
|     enum FLAGS {                                                      |
|         FLAGS_decimal█=█1                                             |
|     };                                                                |
|                                                                       |
|     enum Status {█Unknown, Success, Error█};                          |
|                                                                       |
|     enum class comment_align_e█:█unsigned int                         |
|     {                                                                 |
|        REGULAR, BRACE, ENDIF,                                         |
|     };                                                                |
+-----------------------------------------------------------------------+

Register
========

  ---------------------------------------------------- ----------------------------------------------------------------------------------
  [sp\_enum\_paren (language C\#)](#sp_enum_paren)     Add or remove space in \'NS\_ENUM (\'
  [sp\_enum\_assign](#sp_enum_assign)                  Add or remove space around assignment \'=\' in enum.
  [sp\_enum\_before\_assign](#sp_enum_before_assign)   Add or remove space before assignment \'=\' in enum. Overrides sp\_enum\_assign.
  [sp\_enum\_after\_assign](#sp_enum_after_assign)     Add or remove space after assignment \'=\' in enum. Overrides sp\_enum\_assign.
  [sp\_enum\_colon](#sp_enum_colon)                    Add or remove space around assignment \':\' in enum.
  [sp\_inside\_braces\_enum](#sp_inside_braces_enum)   Add or remove space inside enum \'{\' and \'}\'.
  ---------------------------------------------------- ----------------------------------------------------------------------------------
