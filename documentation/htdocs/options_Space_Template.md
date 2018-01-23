[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Spaces for template
-------------------

+-----------------------------------------------------------------------+
|     {                                                                 |
|        template█<█bool a█>█void f();                                  |
|                                                                       |
|        new List█(foo);                                                |
|                                                                       |
|        new List(█);                                                   |
|                                                                       |
|        List<byte>█m;                                                  |
|        template <typename T>█static ...;                              |
|                                                                       |
|        template<typename T> class Foo<Bar<T>█> { };                   |
|     }                                                                 |
+-----------------------------------------------------------------------+

Register
========

  ---------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------
  [sp\_template\_angle](#sp_template_angle)            Add or remove space in \'template \<\' vs \'template\<\'.\
                                                       If set to ignore, sp\_before\_angle is used.

  [sp\_before\_angle](#sp_before_angle)                Add or remove space before \'\<\>\'

  [sp\_inside\_angle](#sp_inside_angle)                Add or remove space inside \'\<\' and \'\>\'

  [sp\_after\_angle](#sp_after_angle)                  Add or remove space after \'\<\>\'

  [sp\_angle\_paren](#sp_angle_paren)                  Add or remove space between \'\<\>\' and \'(\' as found in \'new List\<byte\>(foo);\'

  [sp\_angle\_paren\_empty](#sp_angle_paren_empty)     Add or remove space between \'\<\>\' and \'()\' as found in \'new List\<byte\>();\'

  [sp\_angle\_word](#sp_angle_word)                    Add or remove space between \'\<\>\' and a word as in \'List\<byte\> m;\' or \'template \<typename T\> static \...\'

  [sp\_angle\_shift](#sp_angle_shift)                  Add or remove space between \'\>\' and \'\>\' in \'\>\>\'

  [sp\_permit\_cpp11\_shift](#sp_permit_cpp11_shift)   Permit removal of the space between \'\>\>\' in \'foo\<bar\<int\> \>\' (C++11 only). Default=False.\
                                                       sp\_angle\_shift cannot remove the space without this option.
  ---------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------
