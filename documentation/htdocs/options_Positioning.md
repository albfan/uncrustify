[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Positioning
-----------

+-----------------------------------------------------------------------+
|     void Mode( TDistMode dm )                                         |
|     {                                                                 |
|         a = b                                                         |
|         + c;                                                          |
|         ^                                                             |
|         ms_DistMode                                                   |
|             = dm;                                                     |
|         ^                                                             |
|         if ((count > 0)                                               |
|             && (count < MAX_COUNT)) { ... }                           |
|             ^                                                         |
|         b = ( GetDistanceMode()                                       |
|         == dmKM ) ? "km" : "Miles";                                   |
|         ^                                                             |
|         b = ( GetDistanceMode() == dmKM )                             |
|             ? "km"                                                    |
|             : "Miles";                                                |
|             ^                                                         |
|     }                                                                 |
|     {                                                                 |
|         a = B(1                                                       |
|               , 2                                                     |
|               , 3);                                                   |
|               ^                                                       |
|     }                                                                 |
|                                                                       |
|     class GLOX_API ClientBase                                         |
|             : public Class                                            |
|             ^^                                                        |
|             , public OtherClass   // if many lines are wanted         |
|             ^                                                         |
|             , public ThridClass                                       |
|             , public ForthClass                                       |
|             ^                                                         |
|     { }                                                               |
|                                                                       |
|     class foo : public                                                |
|     {                                                                 |
|         void bar_c(int t, int u)                                      |
|             : t(222)                                                  |
|             ^                                                         |
|             , u(88)                                                   |
|             ^                                                         |
|         {}                                                            |
|     }                                                                 |
+-----------------------------------------------------------------------+

Register
========

  ----------------------------------------- -----------------------------------------
  [pos\_arith](#pos_arith)                  [pos\_assign](#pos_assign)
  [pos\_bool](#pos_bool)                    [pos\_class\_colon](#pos_class_colon)
  [pos\_class\_comma](#pos_class_comma)     [pos\_comma](#pos_comma)
  [pos\_compare](#pos_compare)              [pos\_conditional](#pos_conditional)
  [pos\_constr\_colon](#pos_constr_colon)   [pos\_constr\_comma](#pos_constr_comma)
  ----------------------------------------- -----------------------------------------
