[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Spaces for byref
----------------

+-----------------------------------------------------------------------+
|                                                                       |
|        bool█&█foo(int█&█idx);                                         |
|                                                                       |
|        MyType█&█MyClass::myMethode() {                                |
|           const MyType& t = getSomewhere();                           |
+-----------------------------------------------------------------------+

Register
========

[sp\_before\_byref](#sp_before_byref)

Add or remove space before a reference sign \'&\'

[sp\_before\_unnamed\_byref](#sp_before_unnamed_byref)

Add or remove space before a reference sign \'&\' that isn\'t followed
by a variable name.\
If set to \'ignore\', sp\_before\_byref is used instead.

[sp\_after\_byref](#sp_after_byref)

Add or remove space after reference sign \'&\', if followed by a word.

[sp\_after\_byref\_func](#sp_after_byref_func)

Add or remove space after a reference sign \'&\', if followed by a func
proto/def.

[sp\_before\_byref\_func](#sp_before_byref_func)

Add or remove space before a reference sign \'&\', if followed by a func
proto/def.
