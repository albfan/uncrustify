[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Spaces for for loop
-------------------

+-----------------------------------------------------------------------+
|     {                                                                 |
|             for (i = 0█;█i < 10█;█i++)                                |
|             {                                                         |
|                     b = i + 1;                                        |
|             }                                                         |
|                                                                       |
|             for (█;█;█)                                               |
|             {                                                         |
|                     b = b + 1;                                        |
|             }                                                         |
|     }                                                                 |
+-----------------------------------------------------------------------+

Register
========

  ----------------------------------------------------------- ----------------------------------------------------------------------------------------------------------
  [sp\_before\_semi\_for](#sp_before_semi_for)                Add or remove space before \';\' in non-empty \'for\' statements.
  [sp\_before\_semi\_for\_empty](#sp_before_semi_for_empty)   Add or remove space before a semicolon of an empty part of a for statement.
  [sp\_after\_semi\_for](#sp_after_semi_for)                  Add or remove space after \';\' in non-empty \'for\' statements. Default=Force.
  [sp\_after\_semi\_for\_empty](#sp_after_semi_for_empty)     Add or remove space after the final semicolon of an empty part of a for statement: for ( ; ; \<here\> ).
  ----------------------------------------------------------- ----------------------------------------------------------------------------------------------------------
