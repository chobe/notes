## Make
http://www.gnu.org/software/make/manual/make.html

## Good tutorial
http://c.learncodethehardway.org/book/index.html

## The Better String Library 
https://github.com/websnarf/bstrlib  

## Install Autotools  
aptitude install build-essential g++ automake autoconf gnu-standards autoconf-doc libtool gettext autoconf-archive  

## Autoconf
1. Write your program, keeping portability in mind. Create "Makefile.in".  
2. Run "autoscan".  
3. Rename "configure.scan" to "configure.ac"  
4. Run "autoheader".  
5. Run "autoconf".  
6. "./configure".  
7. Check "config.h". If necessary, modify source and repeat from step #2.  
8. And lastly, compile!  

## Automake  
1. Create "Makefile.am".  
2. Run "automake".  
3. Fix error messages.  
4. Run "aclocal".  
5. Autoconf everything.  
6. Configure, compile, and enjoy!   

## Autoconf and Automake  
1. Create your sources. (Be sure to have a simple "Makefile" to help Autoconf autodetect things better.)  
2. Run "autoscan" to generate "configure.scan".  
3. Rename "configure.scan" to "configure.ac".  
4. Run "autoheader" to generate "config.h.in".  
5. Make your source portable by looking at "config.h.in". (We previously did this at a later step by reading "config.h", but we can do it in this step by referring to "config.h.in" instead.)  
6. Create "Makefile.am".  
7. Run "automake".  
8. Fix errors and run "automake" again.  
9. Run "aclocal".  
10. Run "autoconf".  
11. Configure, make, and run!  
