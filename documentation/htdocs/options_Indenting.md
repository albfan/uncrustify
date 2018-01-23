[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

Indenting
---------

+-----------------------------------------------------------------------+
|     // indent_with_tabs     = 0 spaces only                           |
|     // indent_cmt_with_tabs = false                                   |
|     int foo::bar()                                                    |
|     {                                                                 |
|         int a;                                                        |
|     ^^^^                                                              |
|         double a_very_long_variable = test (foobar1,                  |
|             foobar5);                                                 |
|         ^^^^                                                          |
|     }                                                                 |
+-----------------------------------------------------------------------+
|     class Test                                                        |
|     {                                                                 |
|      private:                                                         |
|     ^                                                                 |
|        int a;                                                         |
|     }                                                                 |
+-----------------------------------------------------------------------+

Register
========

[indent\_columns](#indent_columns)

[indent\_continue](#indent_continue)

[indent\_with\_tabs](#indent_with_tabs)

[indent\_cmt\_with\_tabs](#indent_cmt_with_tabs)

[indent\_align\_string](#indent_align_string)

[indent\_xml\_string](#indent_xml_string)

[indent\_brace](#indent_brace)

[indent\_braces](#indent_braces)

[indent\_braces\_no\_func](#indent_braces_no_func)

[indent\_braces\_no\_class](#indent_braces_no_class)

[indent\_braces\_no\_struct](#indent_braces_no_struct)

[indent\_brace\_parent](#indent_brace_parent)

[indent\_paren\_open\_brace](#indent_paren_open_brace)

[indent\_namespace](#indent_namespace)

[indent\_namespace\_single\_indent](#indent_namespace_single_indent)

[indent\_namespace\_level](#indent_namespace_level)

[indent\_namespace\_limit](#indent_namespace_limit)

[indent\_extern](#indent_extern)

[indent\_class](#indent_class)

[indent\_class\_colon](#indent_class_colon)

[indent\_class\_on\_colon](#indent_class_on_colon)

[indent\_constr\_colon](#indent_constr_colon)

[indent\_ctor\_init\_leading](#indent_ctor_init_leading)

[indent\_ctor\_init](#indent_ctor_init)

[indent\_else\_if](#indent_else_if)

[indent\_var\_def\_blk](#indent_var_def_blk)

[indent\_var\_def\_cont](#indent_var_def_cont)

[indent\_shift](#indent_shift)

[indent\_func\_def\_force\_col1](#indent_func_def_force_col1)

[indent\_func\_call\_param](#indent_func_call_param)

[indent\_func\_def\_param](#indent_func_def_param)

[indent\_func\_proto\_param](#indent_func_proto_param)

[indent\_func\_class\_param](#indent_func_class_param)

[indent\_func\_ctor\_var\_param](#indent_func_ctor_var_param)

[indent\_template\_param](#indent_template_param)

[indent\_func\_param\_double](#indent_func_param_double)

[indent\_func\_const](#indent_func_const)

[indent\_func\_throw](#indent_func_throw)

[indent\_member](#indent_member)

[indent\_sing\_line\_comments](#indent_sing_line_comments)

[indent\_relative\_single\_line\_comments](#indent_relative_single_line_comments)

[indent\_switch\_case](#indent_switch_case)

[indent\_case\_shift](#indent_case_shift)

[indent\_case\_brace](#indent_case_brace)

[indent\_col1\_comment](#indent_col1_comment)

[indent\_label](#indent_label)

[indent\_access\_spec](#indent_access_spec)

[indent\_access\_spec\_body](#indent_access_spec_body)

[indent\_paren\_nl](#indent_paren_nl)

[indent\_paren\_close](#indent_paren_close)

[indent\_comma\_paren](#indent_comma_paren)

[indent\_bool\_paren](#indent_bool_paren)

[indent\_first\_bool\_expr](#indent_first_bool_expr)

[indent\_square\_nl](#indent_square_nl)

[indent\_preserve\_sql](#indent_preserve_sql)

[indent\_align\_assign](#indent_align_assign)

[indent\_min\_vbrace\_open](#indent_min_vbrace_open)

[indent\_vbrace\_open\_on\_tabstop](#indent_vbrace_open_on_tabstop)

[use\_indent\_continue\_only\_once](#use_indent_continue_only_once)

not yet shown
-------------

only for Pawn
-------------

only for Java
-------------

only for objective C
--------------------

indent\_oc\_msg\_colon\
indent\_oc\_msg\_prioritize\_first\_colon\
indent\_oc\_block\_msg\_xcode\_style\
indent\_oc\_block\_msg\_from\_keyword\
indent\_oc\_block\_msg\_from\_colon\
indent\_oc\_block\_msg\_from\_caret\
indent\_oc\_block\_msg\_from\_brace\
