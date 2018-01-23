[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Spaces for new/ delete
----------------------

+-----------------------------------------------------------------------+
|     {                                                                 |
|         Foo* foo = new█Foo(a,v);                                      |
|         delete[]█m_used;                                              |
|                                                                       |
|         Foo* foo = new█(█ptr,std::nothrow█)█Foo[];                    |
|     }                                                                 |
+-----------------------------------------------------------------------+

Register
========

  ----------------------------------------------------------------- -------------------------------------------------------------------------------
  [sp\_after\_new](#sp_after_new)                                   Controls the spaces after \'new\', \'delete\' and \'delete\[\]\'.

  [sp\_between\_new\_paren](#sp_between_new_paren)                  Controls the spaces between new and \'(\' in \'new()\'.

  [sp\_after\_newop\_paren](#sp_after_newop_paren)                  Controls the spaces between \')\' and \'type\' in \'new(foo) BAR\'.

  [sp\_inside\_newop\_paren](#sp_inside_newop_paren)                Controls the spaces inside paren of the new operator: \'new(foo) BAR\'.

  [sp\_inside\_newop\_paren\_open](#sp_inside_newop_paren_open)     Controls the space after open paren of the new operator: \'new(foo) BAR\'.\
                                                                    Have precedence of sp\_inside\_newop\_paren.

  [sp\_inside\_newop\_paren\_close](#sp_inside_newop_paren_close)   Controls the space before close paren of the new operator: \'new(foo) BAR\'.\
                                                                    Have precedence of sp\_inside\_newop\_paren.
  ----------------------------------------------------------------- -------------------------------------------------------------------------------
