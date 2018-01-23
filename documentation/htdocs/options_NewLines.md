[Uncrustify](https://github.com/uncrustify/uncrustify): Where do the options work?
==================================================================================

New lines
---------

------------------------------------------------------------------------

[]{#nl_remove_extra_newlines}

    ^
    ^
    void bar_0();  // function definition
              ^^
    void bar_0()   // function declaration
              ^^
    void A::bar_1(int a);
            ^    ^     ^
    void bar_2(int a) ^
        ^     ^     ^
              ^     ^
    {^
    }
    ^
    void bar_3(int x,
               int y)
              ^    ^
    {
        int a = 5; ^
        int b = 7;
            ^
        a = 135;
        list_for_each(item, list) {
                                 ^
        }
        ^
        /* c1
         * c2
         */
        ^
        int x2;
        ^
        /* single comment */
        ^
        // cpp comment
        std::for_each(a, b, [] (int& b) -> foo {
                                                ^
            b+=3; return(b);
        }
    ^

    class foo : public my_Class ^
             ^
    {
        void bar_c(int t, int u) ^
            ^            ^
            : t(222)
            , u(88)
            ^
        {
            ^
            typedef char CHAR;
            ^ ^
            CHAR c;
            int a;
            int b;
            ^
            c = 'a';
            ^
            switch (a) {
                      ^
            case 0:
                b = 1;
                break;
            ^
            case 1: b = 5; break;
                   ^
            case 13: {
                    ^
                b = 15;
                break;
            }
            }
            ^ ^
            do { ^
               do_something();
            } while (!d.isEmpty());
            ^^ ^
            if (a) { ^
                b = 1;
            } else if (c) {
             ^    ^      ^
                b ;
            } else {
                  ^
                b = 3;
            }
            ^ ^
            for (a = 1; a < 5; a++) {
                                  ^
                b = b + a;
            }
            ^
            for (int a = 1; a < 5;
                 a++) {
                     ^
                b = a + 4;
            }
            try {
            ^
                b = 1;
                if (err) {
                    ^
                    throw std::runtime_error(std::string("nextKey: ") + err.asString());
                }
            } catch (const std::exception &exc) {
             ^                                 ^
                b = 3;
            }
            ^
            while (c) {
                 ^
                b ;
            }
            ^
        }
        enum CaseOfOne {
                      ^
            a1,
            b1,
            ^
            // comment
            c1,
            ^
        };
        struct indent_ptr_t ^
       {
            chunk_t *ref;
            ^
            // comment
            int delta;
            ^
        } ipt;
         ^
        ^
        union UnionOfOne {
                        ^
            a1,
            b1,
            ^
            // comment
            c1,
            ^
        };
        ^ ^
        private: // same for protected:, signal: or slots: label
        ^
            int ap;
    };
    ^

    namespace foo {
                 ^
    int foo()
    {
        if (foo) a++; return;
            ^          ^
        if (a)
            return;
        ^
    l123: ^
        int a = 5;
        ^
        if (a > b) {
            c = 7;
        ^
            return a + b;
        }
        std::for_each(a, b, [] (int& b)->foo{ b+=3; return(b); });
                                                                ^
        QUrl dxOffEagle("http://something/newpage.html?[{\"foo: bar\"}]", QUrl::TolerantMode);
                                                                      ^
        ^
        return 0;
        ^

    /* c1
     *
     */
    ^
    void b();
    ^
    void d();
    #define LOG_CONTTEXT() \
                          ^
        LOG_FMT(LCONTTEXT  \
                ,"%s:%d set cont_text to '%s'\n"  \
                ,__func__, __LINE__, cmt.cont_text.c_str())
    template <class T>
    ^
    ItemJob::ItemJob(PlatformDependent *internals, const QNetworkRequest &request)
        : GetJob(internals, request)
    typedef int ia;
    typedef int ib;
    ^
    typedef int ic;
    typedef int id;

------------------------------------------------------------------------

Register
========

  ---------------------------------------------------------------------- ----------------------------------------------------------------------
  [nl\_after\_access\_spec](#nl_after_access_spec)                       [nl\_after\_case](#nl_after_case)
  [nl\_after\_class](#nl_after_class)                                    [nl\_after\_do](#nl_after_do)
  [nl\_after\_for](#nl_after_for)                                        [nl\_after\_func\_body](#nl_after_func_body)
  [nl\_after\_func\_body\_class](#nl_after_func_body_class)              [nl\_after\_func\_proto](#nl_after_func_proto)
  [nl\_after\_if](#nl_after_if)                                          [nl\_after\_label\_colon](#nl_after_label_colon)
  [nl\_after\_return](#nl_after_return)                                  [nl\_after\_semicolon](#nl_after_semicolon)
  [nl\_after\_struct](#nl_after_struct)                                  [nl\_after\_switch](#nl_after_switch)
  [nl\_after\_vbrace\_close](#nl_after_vbrace_close)                     [nl\_after\_vbrace\_open](#nl_after_vbrace_open)
  [nl\_after\_while](#nl_after_while)                                    [nl\_before\_access\_spec](#nl_before_access_spec)
  [nl\_before\_block\_comment](#nl_before_block_comment)                 [nl\_before\_c\_comment](#nl_before_c_comment)
  [nl\_before\_case](#nl_before_case)                                    [nl\_before\_cpp\_comment](#nl_before_cpp_comment)
  [nl\_before\_do](#nl_before_do)                                        [nl\_before\_for](#nl_before_for)
  [nl\_before\_if](#nl_before_if)                                        [nl\_before\_return](#nl_before_return)
  [nl\_before\_return](#nl_before_return)                                [nl\_before\_switch](#nl_before_switch)
  [nl\_before\_throw](#nl_before_throw)                                  [nl\_before\_while](#nl_before_while)
  [nl\_brace\_catch](#nl_brace_catch)                                    [nl\_brace\_else](#nl_brace_else)
  [nl\_brace\_fparen](#nl_brace_fparen)                                  [nl\_brace\_square](#nl_brace_square)
  [nl\_brace\_struct\_var](#nl_brace_struct_var)                         [nl\_brace\_while](#nl_brace_while)
  [nl\_case\_colon\_brace](#nl_case_colon_brace)                         [nl\_catch\_brace](#nl_catch_brace)
  [nl\_class\_brace](#nl_class_brace)                                    [nl\_class\_colon](#nl_class_colon)
  [nl\_collapse\_empty\_body](#nl_collapse_empty_body)                   [nl\_comment\_func\_def](#nl_comment_func_def)
  [nl\_constr\_colon](#nl_constr_colon)                                  [nl\_constr\_init\_args](#nl_constr_init_args)
  [nl\_cpp\_ldef\_brace](#nl_cpp_ldef_brace)                             [nl\_do\_brace](#nl_do_brace)
  [nl\_ds\_struct\_enum\_close\_brace](#nl_ds_struct_enum_close_brace)   [nl\_ds\_struct\_enum\_close\_brace](#nl_ds_struct_enum_close_brace)
  [nl\_ds\_struct\_enum\_close\_brace](#nl_ds_struct_enum_close_brace)   [nl\_ds\_struct\_enum\_cmt](#nl_ds_struct_enum_cmt)
  [nl\_ds\_struct\_enum\_cmt](#nl_ds_struct_enum_cmt)                    [nl\_ds\_struct\_enum\_cmt](#nl_ds_struct_enum_cmt)
  [nl\_else\_brace](#nl_else_brace)                                      [nl\_else\_if](#nl_else_if)
  [nl\_elseif\_brace](#nl_elseif_brace)                                  [nl\_end\_of\_file](#nl_end_of_file)
  [nl\_enum\_brace](#nl_enum_brace)                                      [nl\_fcall\_brace](#nl_fcall_brace)
  [nl\_fdef\_brace](#nl_fdef_brace)                                      [nl\_for\_brace](#nl_for_brace)
  [nl\_func\_decl\_args](#nl_func_decl_args)                             [nl\_func\_decl\_empty](#nl_func_decl_empty)
  [nl\_func\_decl\_end](#nl_func_decl_end)                               [nl\_func\_decl\_end](#nl_func_decl_end)
  [nl\_func\_decl\_end\_single](#nl_func_decl_end_single)                [nl\_func\_decl\_start](#nl_func_decl_start)
  [nl\_func\_decl\_start\_single](#nl_func_decl_start_single)            [nl\_func\_def\_args](#nl_func_def_args)
  [nl\_func\_def\_empty](#nl_func_def_empty)                             [nl\_func\_def\_end\_single](#nl_func_def_end_single)
  [nl\_func\_def\_paren](#nl_func_def_paren)                             [nl\_func\_def\_start](#nl_func_def_start)
  [nl\_func\_paren](#nl_func_paren)                                      [nl\_func\_scope\_name](#nl_func_scope_name)
  [nl\_func\_type\_name](#nl_func_type_name)                             [nl\_func\_type\_name\_class](#nl_func_type_name_class)
  [nl\_func\_var\_def\_blk](#nl_func_var_def_blk)                        [nl\_if\_brace](#nl_if_brace)
  [nl\_max](#nl_max)                                                     [nl\_multi\_line\_cond](#nl_multi_line_cond)
  [nl\_multi\_line\_define](#nl_multi_line_define)                       [nl\_namespace\_brace](#nl_namespace_brace)
  [nl\_remove\_extra\_newlines](#nl_remove_extra_newlines)               [nl\_return\_expr](#nl_return_expr)
  [nl\_start\_of\_file](#nl_start_of_file)                               [nl\_struct\_brace](#nl_struct_brace)
  [nl\_switch\_brace](#nl_switch_brace)                                  [nl\_template\_class](#nl_template_class)
  [nl\_try\_brace](#nl_try_brace)                                        [nl\_typedef\_blk\_end](#nl_typedef_blk_end)
  [nl\_typedef\_blk\_in](#nl_typedef_blk_in)                             [nl\_typedef\_blk\_start](#nl_typedef_blk_start)
  [nl\_union\_brace](#nl_union_brace)                                    [nl\_var\_def\_blk\_end](#nl_var_def_blk_end)
  [nl\_var\_def\_blk\_in](#nl_var_def_blk_in)                            [nl\_var\_def\_blk\_start](#nl_var_def_blk_start)
  [nl\_while\_brace](#nl_while_brace)                                    
  ---------------------------------------------------------------------- ----------------------------------------------------------------------

only for Java
-------------

nl\_after\_annotation\
nl\_between\_annotation\
nl\_paren\_dbrace\_open\

only for D
----------

nl\_after\_square\_assign\
nl\_assign\_square\
nl\_scope\_brace\
nl\_unittest\_brace\
nl\_version\_brace\

only for oc
-----------

nl\_oc\_msg\_args\
nl\_oc\_msg\_leave\_one\_liner\

only for C\#
------------

nl\_around\_cs\_property\
nl\_between\_get\_set\
nl\_after\_try\_catch\_finally\
nl\_brace\_finally\
nl\_finally\_brace\
nl\_getset\_brace\
nl\_property\_brace\

not yet shown
-------------

nl\_after\_brace\_close\
nl\_after\_brace\_open\
template class X { /\* a \*/ }; template class Y { /\* \... \*/ };
nl\_after\_brace\_open\_cmt\
nl\_after\_func\_body\_one\_liner\
nl\_after\_func\_proto\_group\
nl\_after\_multiline\_comment\
nl\_after\_vbrace\_open\_empty\
nl\_brace\_brace\
nl\_class\_init\_args\
nl\_class\_leave\_one\_liners\
nl\_cpp\_lambda\_leave\_one\_liners\
nl\_create\_for\_one\_liner\
nl\_create\_if\_one\_liner\
nl\_create\_while\_one\_liner\
nl\_define\_macro\
nl\_enum\_leave\_one\_liners\
nl\_func\_leave\_one\_liners\
nl\_getset\_leave\_one\_liners\
nl\_if\_leave\_one\_liners\
nl\_squeeze\_ifdef\
nl\_using\_brace\
