# This is where I will be pasting the shell commands and the outputs:
I am starting from week 4:
# Week 4:
  tanish@tanish:~$ help
GNU bash, version 5.2.37(1)-release (x86_64-pc-linux-gnu)
These shell commands are defined internally.  Type `help' to see this list.
Type `help name' to find out more about the function `name'.
Use `info bash' to find out more about the shell in general.
Use `man -k' or `info' to find out more about commands not in this list.

A star (*) next to a name means that the command is disabled.

 job_spec [&]                              history [-c] [-d offset] [n] or histor>
 (( expression ))                          if COMMANDS; then COMMANDS; [ elif COM>
 . filename [arguments]                    jobs [-lnprs] [jobspec ...] or jobs -x>
 :                                         kill [-s sigspec | -n signum | -sigspe>
 [ arg... ]                                let arg [arg ...]
 [[ expression ]]                          local [option] name[=value] ...
 alias [-p] [name[=value] ... ]            logout [n]
 bg [job_spec ...]                         mapfile [-d delim] [-n count] [-O orig>
 bind [-lpsvPSVX] [-m keymap] [-f filena>  popd [-n] [+N | -N]
 break [n]                                 printf [-v var] format [arguments]
 builtin [shell-builtin [arg ...]]         pushd [-n] [+N | -N | dir]
 caller [expr]                             pwd [-LP]
 case WORD in [PATTERN [| PATTERN]...) C>  read [-ers] [-a array] [-d delim] [-i >
 cd [-L|[-P [-e]] [-@]] [dir]              readarray [-d delim] [-n count] [-O or>
 command [-pVv] command [arg ...]          readonly [-aAf] [name[=value] ...] or >
 compgen [-abcdefgjksuv] [-o option] [-A>  return [n]
 complete [-abcdefgjksuv] [-pr] [-DEI] [>  select NAME [in WORDS ... ;] do COMMAN>
 compopt [-o|+o option] [-DEI] [name ...>  set [-abefhkmnptuvxBCEHPT] [-o option->
 continue [n]                              shift [n]
 coproc [NAME] command [redirections]      shopt [-pqsu] [-o] [optname ...]
 declare [-aAfFgiIlnrtux] [name[=value] >  source filename [arguments]
 dirs [-clpv] [+N] [-N]                    suspend [-f]
 disown [-h] [-ar] [jobspec ... | pid ..>  test [expr]
 echo [-neE] [arg ...]                     time [-p] pipeline
 enable [-a] [-dnps] [-f filename] [name>  times
 eval [arg ...]                            trap [-lp] [[arg] signal_spec ...]
 exec [-cl] [-a name] [command [argument>  true
 exit [n]                                  type [-afptP] name [name ...]
 export [-fn] [name[=value] ...] or expo>  typeset [-aAfFgiIlnrtux] name[=value] >
 false                                     ulimit [-SHabcdefiklmnpqrstuvxPRT] [li>
 fc [-e ename] [-lnr] [first] [last] or >  umask [-p] [-S] [mode]
 fg [job_spec]                             unalias [-a] name [name ...]
 for NAME [in WORDS ... ] ; do COMMANDS;>  unset [-f] [-v] [-n] [name ...]
 for (( exp1; exp2; exp3 )); do COMMANDS>  until COMMANDS; do COMMANDS-2; done
 function name { COMMANDS ; } or name ()>  variables - Names and meanings of some>
 getopts optstring name [arg ...]          wait [-fn] [-p var] [id ...]
 hash [-lr] [-p pathname] [-dt] [name ..>  while COMMANDS; do COMMANDS-2; done
 help [-dms] [pattern ...]                 { COMMANDS ; }
tanish@tanish:~$ man
What manual page do you want?
For example, try 'man man'.
tanish@tanish:~$ man man
man: can't resolve man7/groff_man.7
tanish@tanish:~$ info
bash: info: command not found
tanish@tanish:~$ cp info
cp: missing destination file operand after 'info'
Try 'cp --help' for more information.
tanish@tanish:~$ info cp
bash: info: command not found
tanish@tanish:~$ whatis man
man (1)              - an interface to the system reference manuals
tanish@tanish:~$ whatis man
man (1)              - an interface to the system reference manuals
tanish@tanish:~$ type type
type is a shell builtin
tanish@tanish:~$ type whatis
whatis is hashed (/usr/bin/whatis)
tanish@tanish:~$ type cp
cp is hashed (/usr/bin/cp)
tanish@tanish:~$ type ls
ls is aliased to `ls --color=auto'
tanish@tanish:~$ which ls
/usr/bin/ls
tanish@tanish:~$ whatis
whatis what?
tanish@tanish:~$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
tanish@tanish:~$ whatis what
what: nothing appropriate.
tanish@tanish:~$ what ls
bash: what: command not found
tanish@tanish:~$ which cd
tanish@tanish:~$ which cd
tanish@tanish:~$ help cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.
    
    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable. If DIR is "-", it is converted to $OLDPWD.
    
    The variable CDPATH defines the search path for the directory containing
    DIR.  Alternative directory names in CDPATH are separated by a colon (:).
    A null directory name is the same as the current directory.  If DIR begins
    with a slash (/), then CDPATH is not used.
    
    If the directory is not found, and the shell option `cdable_vars' is set,
    the word is assumed to be  a variable name.  If that variable has a value,
    its value is used for DIR.
    
    Options:
      -L	force symbolic links to be followed: resolve symbolic
    		links in DIR after processing instances of `..'
      -P	use the physical directory structure without following
    		symbolic links: resolve symbolic links in DIR before
    		processing instances of `..'
      -e	if the -P option is supplied, and the current working
    		directory cannot be determined successfully, exit with
    		a non-zero status
      -@	on systems that support it, present a file with extended
    		attributes as a directory containing the file attributes
    
    The default is to follow symbolic links, as if `-L' were specified.
    `..' is processed by removing the immediately previous pathname component
    back to a slash or the beginning of DIR.
    
    Exit Status:
    Returns 0 if the directory is changed, and if $PWD is set successfully when
    -P is used; non-zero otherwise.
tanish@tanish:~$ help -l
bash: help: -l: invalid option
help: usage: help [-dms] [pattern ...]
tanish@tanish:~$ help cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.
    
    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable. If DIR is "-", it is converted to $OLDPWD.
    
    The variable CDPATH defines the search path for the directory containing
    DIR.  Alternative directory names in CDPATH are separated by a colon (:).
    A null directory name is the same as the current directory.  If DIR begins
    with a slash (/), then CDPATH is not used.
    
    If the directory is not found, and the shell option `cdable_vars' is set,
    the word is assumed to be  a variable name.  If that variable has a value,
    its value is used for DIR.
    
    Options:
      -L	force symbolic links to be followed: resolve symbolic
    		links in DIR after processing instances of `..'
      -P	use the physical directory structure without following
    		symbolic links: resolve symbolic links in DIR before
    		processing instances of `..'
      -e	if the -P option is supplied, and the current working
    		directory cannot be determined successfully, exit with
    		a non-zero status
      -@	on systems that support it, present a file with extended
    		attributes as a directory containing the file attributes
    
    The default is to follow symbolic links, as if `-L' were specified.
    `..' is processed by removing the immediately previous pathname component
    back to a slash or the beginning of DIR.
    
    Exit Status:
    Returns 0 if the directory is changed, and if $PWD is set successfully when
    -P is used; non-zero otherwise.
tanish@tanish:~$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
tanish@tanish:~$ cd Desktop/
tanish@tanish:~/Desktop$ LS
bash: LS: command not found
tanish@tanish:~/Desktop$ ls
'!for-twinkering'   linux-guide.pdf
tanish@tanish:~/Desktop$ cd \!for-twinkering/
tanish@tanish:~/Desktop/!for-twinkering$ ls
days-30  days-60  days-90
tanish@tanish:~/Desktop/!for-twinkering$ cd days-30/
tanish@tanish:~/Desktop/!for-twinkering/days-30$ ls
 linux-guide.pdf  'this is a cool alt.pdf'   this-is-a-cool-alt.pdf   txt
tanish@tanish:~/Desktop/!for-twinkering/days-30$ mkdir --help
Usage: mkdir [OPTION]... DIRECTORY...
Create the DIRECTORY(ies), if they do not already exist.

Mandatory arguments to long options are mandatory for short options too.
  -m, --mode=MODE   set file mode (as in chmod), not a=rwx - umask
  -p, --parents     no error if existing, make parent directories as needed,
                    with their file modes unaffected by any -m option
  -v, --verbose     print a message for each created directory
  -Z                   set SELinux security context of each created directory
                         to the default type
      --context[=CTX]  like -Z, or if CTX is specified then set the SELinux
                         or SMACK security context to CTX
      --help        display this help and exit
      --version     output version information and exit

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Full documentation <https://www.gnu.org/software/coreutils/mkdir>
tanish@tanish:~$ clear
tanish@tanish:~$ apropos partition
proc_partitions (5)  - major and minor numbers of partitions
cfdisk (8)           - display or manipulate a disk partition table
fdisk (8)            - manipulate disk partition table
kernel-install (8)   - Add and remove kernel and initrd images to and from the boo...
parted (8)           - a partition manipulation program
partprobe (8)        - inform the OS of partition table changes
partx (8)            - tell the kernel about the presence and numbering of on-disk...
resizepart (8)       - tell the kernel about the new size of a partition
sfdisk (8)           - display or manipulate a disk partition table
systemd-gpt-auto-generator (8) - Generator for automatically discovering and mount...
tanish@tanish:~$ whatis apropos
apropos (1)          - search the manual page names and descriptions
tanish@tanish:~$ whatis ls -lh
Usage: whatis [OPTION...] KEYWORD...

  -d, --debug                emit debugging messages
  -v, --verbose              print verbose warning messages
  -r, --regex                interpret each keyword as a regex
  -w, --wildcard             the keyword(s) contain wildcards
  -l, --long                 do not trim output to terminal width
  -C, --config-file=FILE     use this user configuration file
  -L, --locale=LOCALE        define the locale for this search
  -m, --systems=SYSTEM       use manual pages from other systems
  -M, --manpath=PATH         set search path for manual pages to PATH
  -s, --sections=LIST, --section=LIST
                             search only these sections (colon-separated)
  -?, --help                 give this help list
      --usage                give a short usage message
  -V, --version              print program version

Mandatory or optional arguments to long options are also mandatory or optional
for any corresponding short options.

Report bugs to cjwatson@debian.org.
tanish@tanish:~$ whatis ls
ls (1)               - list directory contents
tanish@tanish:~$ whatis -v
whatis what?
tanish@tanish:~$ verson
bash: verson: command not found
tanish@tanish:~$ bash man
/usr/bin/man: /usr/bin/man: cannot execute binary file
tanish@tanish:~$ man ls
tanish@tanish:~$ man cp
tanish@tanish:~$ man bash
tanish@tanish:~$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
tanish@tanish:~$ cd Desktop/\!for-twinkering/days-30/;ls
 linux-guide.pdf  'this is a cool alt.pdf'   this-is-a-cool-alt.pdf   txt
tanish@tanish:~/Desktop/!for-twinkering/days-30$ ls
 linux-guide.pdf  'this is a cool alt.pdf'   this-is-a-cool-alt.pdf   txt
tanish@tanish:~/Desktop/!for-twinkering/days-30$ mkdir playgroung-for-fun
tanish@tanish:~/Desktop/!for-twinkering/days-30$ ls
 linux-guide.pdf     'this is a cool alt.pdf'   txt
 playgroung-for-fun   this-is-a-cool-alt.pdf
tanish@tanish:~/Desktop/!for-twinkering/days-30$ cd ../../../
tanish@tanish:~$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
tanish@tanish:~$ type plygrond-cd
bash: type: plygrond-cd: not found
tanish@tanish:~$ cd Desktop/\!for-twinkering/days-30/playgroung-for-fun/
tanish@tanish:~/Desktop/!for-twinkering/days-30/playgroung-for-fun$ cd -
/home/tanish
tanish@tanish:~$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
tanish@tanish:~$ type PG
bash: type: PG: not found
tanish@tanish:~$ alias PG='cd Desktop/\!for-twinkering/days-30/playgroung-for-fun/'
tanish@tanish:~$ PG
tanish@tanish:~/Desktop/!for-twinkering/days-30/playgroung-for-fun$ 
tanish@tanish:~$ type apg
bash: type: apg: not found
tanish@tanish:~$ alias apg='cd ~/Desktop'
tanish@tanish:~$ PG
tanish@tanish:~/Desktop/!for-twinkering/days-30/playgroung-for-fun$ apg
tanish@tanish:~/Desktop$ 
tanish@tanish:~/Desktop$ unalias apg
tanish@tanish:~/Desktop$ PG
bash: cd: Desktop/!for-twinkering/days-30/playgroung-for-fun/: No such file or directory
tanish@tanish:~/Desktop$ cd /
tanish@tanish:/$ ls
bin   etc         initrd.img.old  lost+found  opt   run   sys  var
boot  home        lib             media       proc  sbin  tmp  vmlinuz
dev   initrd.img  lib64           mnt         root  srv   usr  vmlinuz.old
tanish@tanish:/$ PG
bash: cd: Desktop/!for-twinkering/days-30/playgroung-for-fun/: No such file or directory
tanish@tanish:/$ cd home
tanish@tanish:/home$ ls
tanish
tanish@tanish:/home$ cd tanish/
tanish@tanish:~$ PG
tanish@tanish:~/Desktop/!for-twinkering/days-30/playgroung-for-fun$ apg
bash: apg: command not found
tanish@tanish:~/Desktop/!for-twinkering/days-30/playgroung-for-fun$ 
tanish@tanish:~/Desktop/!for-twinkering/days-30/playgroung-for-fun$ cd /
tanish@tanish:/$ PG
bash: cd: Desktop/!for-twinkering/days-30/playgroung-for-fun/: No such file or directory
tanish@tanish:/$ 
**there is a problem in the command now, i will fix it by sun=ing this command now**
tanish@tanish:/$ cd ~/Desktop/
tanish@tanish:~/Desktop$ cd ..
tanish@tanish:~$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
tanish@tanish:~$ cd Desktop/\!for-twinkering/days-30/playgroung-for-fun/
tanish@tanish:~/Desktop/!for-twinkering/days-30/playgroung-for-fun$ cd -
/home/tanish
tanish@tanish:~$ unalias PD
bash: unalias: PD: not found
tanish@tanish:~$ unalias PG
tanish@tanish:~$ PG
bash: PG: command not found
tanish@tanish:~$ alias PG='cd ~/Desktop/\!for-twinkering/days-30/playgroung-for-fun/'
tanish@tanish:~$ CD /
bash: CD: command not found
tanish@tanish:~$ cd /
tanish@tanish:/$ PG
tanish@tanish:~/Desktop/!for-twinkering/days-30/playgroung-for-fun$ cd ~/Downloads/
tanish@tanish:~/Downloads$ PG
tanish@tanish:~/Desktop/!for-twinkering/days-30/playgroung-for-fun$ 
**Now fixed**




tanish@tanish:~/Desktop/!for-twinkering/days-30$ 

