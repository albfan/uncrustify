[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Spaces for class
----------------

+-----------------------------------------------------------------------+
|     {                                                                 |
|        class my_class█:█baseclass1, baseclass2                        |
|     {                                                                 |
|     public:                                                           |
|             my_class█(int b)█:█x(b);                                  |
|                                                                       |
|             my_class█() : c(2)                                        |
|             {                                                         |
|             }                                                         |
|     }                                                                 |
+-----------------------------------------------------------------------+

Register
========

  ------------------------------------------------------------- ----------------------------------------------------------------------------------------
  [sp\_after\_class\_colon](#sp_after_class_colon)              Add or remove space after class \':\'
  [sp\_before\_class\_colon](#sp_before_class_colon)            Add or remove space before class \':\'
  [sp\_after\_constr\_colon](#sp_after_constr_colon)            Add or remove space after class constructor \':\'.
  [sp\_before\_constr\_colon](#sp_before_constr_colon)          Add or remove space before class constructor \':\'.
  [sp\_func\_class\_paren](#sp_func_class_paren)                Add or remove space between a constructor/destructor and the open paren.
  [sp\_func\_class\_paren\_empty](#sp_func_class_paren_empty)   Add or remove space between a constructor without parameters or destructor and \'()\'.
  ------------------------------------------------------------- ----------------------------------------------------------------------------------------
