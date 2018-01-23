[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Spaces for assign
-----------------

+-----------------------------------------------------------------------+
|                                                                       |
|     int decimal█=█1;                                                  |
|     normal█+=█2;                                                      |
|                                                                       |
|     int find(size_t idx█=█0);                                         |
|                                                                       |
|     enum FLAGS {                                                      |
|         FLAGS_decimal█=█1,                                            |
|                                                                       |
|     return [█=█](T* t) {  };                                          |
+-----------------------------------------------------------------------+

Register
========

  ---------------------------------------------------- ------------------------------------------------------------------------------------------------
  [sp\_assign](#sp_assign)                             Add or remove space around assignment operator \'=\', \'+=\', etc.
  [sp\_cpp\_lambda\_assign](#sp_cpp_lambda_assign)     Add or remove space around \'=\' in C++11 lambda capture specifications. Overrides sp\_assign.
  [sp\_assign\_default](#sp_assign_default)            Add or remove space around assignment operator \'=\' in a prototype.
  [sp\_before\_assign](#sp_before_assign)              Add or remove space before assignment operator \'=\', \'+=\', etc. Overrides sp\_assign.
  [sp\_after\_assign](#sp_after_assign)                Add or remove space after assignment operator \'=\', \'+=\', etc. Overrides sp\_assign.
  [sp\_enum\_assign](#sp_enum_assign)                  Add or remove space around assignment \'=\' in enum.
  [sp\_enum\_before\_assign](#sp_enum_before_assign)   Add or remove space before assignment \'=\' in enum. Overrides sp\_enum\_assign.
  [sp\_enum\_after\_assign](#sp_enum_after_assign)     Add or remove space after assignment \'=\' in enum. Overrides sp\_enum\_assign.
  ---------------------------------------------------- ------------------------------------------------------------------------------------------------
