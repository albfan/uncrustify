align\_typedef
--------------

### align\_typedef\_span

The span for aligning single-line typedefs (0=don\'t align)

+-----------------------+-----------------------+-----------------------+
| original\             | align\_typedef\_span= | align\_typedef\_span= |
| align\_typedef\_span= | 1                     | 2                     |
| 0                     |                       |                       |
+-----------------------+-----------------------+-----------------------+
|     typedef int MY_IN |     typedef int MY_IN |     typedef int   MY_ |
| T;                    | T;                    | INT;                  |
|     int a;            |     int a;            |     int a;            |
|     typedef int       |     typedef int   *MY |     typedef int   *MY |
| *MY_INTP;             | _INTP;                | _INTP;                |
|     typedef float  My |     typedef float My_ |     typedef float My_ |
| _Float;               | Float;                | Float;                |
|                       |                       |                       |
|                       |                       |                       |
| *no alignment*        | *The third line is    | *all the lines are    |
|                       | not catch in the      | catched*              |
|                       | span*                 |                       |
+-----------------------+-----------------------+-----------------------+

### align\_typedef\_gap

The minimum space between the type and the synonym of a typedef\
Can be only used if align\_typedef\_span \>= 1

+-----------------------+-----------------------+-----------------------+
| original\             | align\_typedef\_gap=1 | align\_typedef\_gap=3 |
| align\_typedef\_span= |                       |                       |
| 2                     |                       |                       |
+-----------------------+-----------------------+-----------------------+
|     typedef int   MY_ |     typedef int   MY_ |     typedef int     M |
| INT;                  | INT;                  | Y_INT;                |
|     int a;            |     int a;            |     int a;            |
|     typedef int   *MY |     typedef int   *MY |     typedef int     * |
| _INTP;                | _INTP;                | MY_INTP;              |
|     typedef float My_ |     typedef float My_ |     typedef float   M |
| Float;                | Float;                | y_Float;              |
|                       |                       |                       |
|                       |                       |                       |
| *as above*            | *no change*           | *the gap has 3        |
|                       |                       | spaces*               |
+-----------------------+-----------------------+-----------------------+

### align\_typedef\_star\_style

Controls the positioning of the \'\*\' in typedefs.\
0: Align on typedef type, ignore \'\*\'\
1: The \'\*\' is part of type name\
2: The \'\*\' is part of the type, but dangling

+-----------------+-----------------+-----------------+-----------------+
| original        | align\_typedef\ | align\_typedef\ | align\_typedef\ |
|                 | _gap=3\         | _gap=3\         | _gap=3\         |
|                 | align\_typedef\ | align\_typedef\ | align\_typedef\ |
|                 | _star\_style=0  | _star\_style=1  | _star\_style=2  |
+-----------------+-----------------+-----------------+-----------------+
|     typedef int |     typedef int |     typedef int |     typedef int |
|  MY_INT;        |      MY_INT;    |      MY_INT;    |      MY_INT;    |
|     int a;      |     int a;      |     int a;      |     int a;      |
|     typedef int |     typedef int |     typedef int |     typedef int |
|   *    MY_INTP; |  *   MY_INTP;   |      *MY_INTP;  |     *MY_INTP;   |
|     typedef flo |     typedef flo |     typedef flo |     typedef flo |
| at  My_Float;   | at   My_Float;  | at   My_Float;  | at   My_Float;  |
|                 |                 |                 |                 |
|                 |                 |                 |                 |
| *no alignment*  | *the star is    | *the star is    | *the star is    |
|                 | ignored*        | part of type    | part of type    |
|                 |                 | name*           | name, but       |
|                 |                 |                 | dangling*       |
+-----------------+-----------------+-----------------+-----------------+

### align\_typedef\_func

How to align typedef\'d functions with other typedefs\
0: Don\'t mix them at all\
1: align the open paren with the types

+-----------------------------------+-----------------------------------+
| original                          | align\_typedef\_gap=3\            |
|                                   | align\_typedef\_star\_style=1\    |
|                                   | align\_typedef\_func=1            |
+-----------------------------------+-----------------------------------+
|     typedef int MY_INT;           |     typedef int     MY_INT;       |
|     int a;                        |     int a;                        |
|     typedef int  *    MY_INTP;    |     typedef int     *MY_INTP;     |
|     typedef float  My_Float;      |     typedef float   My_Float;     |
|     typedef int      (*foo_t)(voi |     typedef int     (*foo_t)(void |
| d *bar);                          |  *bar);                           |
|     typedef int          (*somefu |     typedef int     (*somefunc_t) |
| nc_t)(void *barstool);            | (void *barstool);                 |
|                                   |                                   |
|                                   |                                   |
| *no alignment*                    |                                   |
+-----------------------------------+-----------------------------------+
