#Uncrustify                                                           
[![Travis CI Build Status](https://travis-ci.org/uncrustify/uncrustify.svg?branch=master)](https://travis-ci.org/uncrustify/uncrustify/builds)   
[![Coverity Scan Build Status](https://scan.coverity.com/projects/8264/badge.svg)](https://scan.coverity.com/projects/uncrustify)                                                                  
Source Code Beautifier for C, C++, C\#, ObjectiveC, D, Java, Pawn and VALA                                                                
                                                                     
Introduction                                                         
------------                                                         
                                                                     
The goals of this project are simple: Create a highly configurable,  
easily modifiable source code beautifier.                            
                                                                     
Features                                                             
--------                                                             
                                                                     
-   Indent code, aligning on parens, assignments, etc                
-   Align on \'=\' and variable definitions                          
-   Align structure initializers                                     
-   Align \#define stuff                                             
-   Align backslash-newline stuff                                    
-   Reformat comments (a little bit)                                 
-   Fix inter-character spacing                                      
-   Add or remove parens on return statements                        
-   Add or remove braces on single-statement if/do/while/for         
    statements                                                       
-   Supports embedded SQL \'EXEC SQL\' stuff                         
-   Highly configurable - 608 configurable options as of version 0.66
                                                                     
[What it does?](uncrustify.md)
                                                                     
See some example [output](examples/example.c).                       
                                                                     
Configuration                                                        
-------------                                                        
                                                                     
See avaliable [Options](options.md)
                                                                     
Where to get Uncrustify                                              
-----------------------                                              
                                                                     
### Project Websites                                                 
                                                                     
[Sourceforge project web site](http://sourceforge.net/projects/uncrustify/)                  
[Release downloads](http://sourceforge.net/projects/uncrustify/files/)       
[Freshmeat Project](http://freshmeat.net/projects/uncrustify/)      
[Git Hub](http://github.com/uncrustify/uncrustify)                  
                                                                     
### Source Code                                                      
                                                                     
As of release 0.54, the source code is maintained in a               
[Git](http://git-scm.com/) repository.                             
                                                                    
The public Git URL for Sourceforge.net is `git://uncrustify.git.sourceforge.net/gitroot/uncrustify/uncrustify`
                                                                    
The public Git URL for github.com is `git://github.com/uncrustify/uncrustify.git`
                                                                     
### Prebuilt binaries                                                
                                                                     
Windows (i386) :                                                     
[Sourceforge](http://sourceforge.net/project/showfiles.php?group_id=153164)                                                              
SPARC/Solaris 2.5-10 and x86/Solaris 8-10 :                          
[sunfreeware.com](http://sunfreeware.com/)                          
                                                                     
### Universal Indent GUI                                             
                                                                     
[Universal Indent GUI](http://universalindent.sourceforge.net/) is a cross-platform graphical configuration file editor for many code beautifiers, including Uncrustify.                                  
                                                                     
Want to help?                                                        
-------------                                                        
                                                                     
The most helpful way is to try it out and give feedback. Documentation and examples are available in the source tree, so check it out.                                                              
                                                                     
You can find the output from \'uncrustify \--show-config\' [here](config.txt). Here is the [default config file](default.cfg). And one I set up for [Linux](linux.cfg.txt). And here is a [before](examples/c-1.in.c) and [after](examples/c-1.out.c) C source example. That should give you a pretty good idea of what Uncrustify can do.\  
                                                                     
If you find a bug, please do the following:                          
                                                                     
-   Reduce the input source file to the minimum that still has the problem                                                          
-   Use the sourceforget.net bug tracker                             
-   Attach the input source file, the configuration file, and a file that contains the expected output                                
                                                                     
If you want to add a feature, fix a bug, or implement missing functionality, feel free to do so! Patches are welcome! Here are some areas that need attention:                             
-   Test Java support and provide feedback (or patches!)             
-   Test Objective C support and provide feedback (or patches!)      
-   Test Embedded SQL to see what works                              
-   This web page need a (re)design                                  
-   A logo of some sort                                              
-   Examples that can be put on this website to show off what Uncrustify can do                                                
-   Anything else that you want to do to make it better?             
                                                                     
### Project Mailing list                                             
                                                                     
There is one mailing list for Uncrustify.\                           
[uncrustify-developer@lists.sourceforge.net](http://sourceforge.net/mailarchive/forum.php?forum_name=uncrustify-developer) Despite the name, it is for both users and developers.             
                                                                     
Portability                                                          
-----------                                                          
                                                                     
I\'m pretty sure that I\'m not using anything that is OS-specific. The software has been tested on the following operating systems:     
                                                                     
-   Linux                                                            
-   QNX                                                              
-   OS X                                                             
-   FreeBSD, NetBSD, OpenBSD                                         
-   Sun Solaris 9                                                    
-   Windows XP (binary available)                                    
                                                                     
Links                                                                
-----                                                                
                                                                     
-   [Universal Indent GUI](http://universalindent.sourceforge.net/)  
-   Don\'t know what D is? Check out the [D Programming Language website](http://dlang.org/index.html).                           
-   [Linux Links](http://www.linuxlinks.com)                         
                                                                     
Distributions that package Uncrustify                                
-------------------------------------                                
                                                                     
-   [Debian](http://www.debian.org/)                                 
-   [Fedora](http://fedora.redhat.com/)                              
-   [ALT Linux](http://www.altlinux.com/)                            
-   [T2](http://www.t2-project.org/)                                 
-   [MacPorts](http://www.macports.org/)                             
-   [FreeBSD Ports (textproc/uncrustify)](http://www.freebsd.org/cgi/ports.cgi?query=uncrustify)                                                         
-   [OpenBSD Ports (textproc/uncrustify)](http://openports.se/textproc/uncrustify)  
-   Others?                                                          

[\"Support This Project\"](http://sourceforge.net/donate/index.php?group_id=153164)
