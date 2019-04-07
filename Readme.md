
--ABOUT--

ViMypager is a plugin which soothes out some kinks when vim is used as pager for mysql.

By default it exhibits the immediate exit feature of the less pager, as described on the Mysql version 5.7 man page :

>>>> The -F and -X options may be used with less to cause it to exit if output fits on one screen, which is convenient when no scrolling is necessary:
>>>> mysql> pager less -n -i -S -F -X


--USAGE--

To setup the plugin in vim, Install using your favorite vim plugin manager, or ":source /path/to/vi/my/pager/vimypager.vim"

To get the plugin working with mysql use the command below anyhere mysql accpets a pager command:

----------------------------------------------------------------------------------------------------
vim -R -c 'set nomod nonu' -c 'silent call vimypager#Run()' -

----------------------------------------------------------------------------------------------------

--Example--

Here is are contents to a sample .my.cnf file which uses vimypager:

[mysql]
prompt=(\\u@\\h) [\\d]>\\_
pager=vim -R -c 'set nomod nonu' -c 'silent call vimypager#Run()' -

