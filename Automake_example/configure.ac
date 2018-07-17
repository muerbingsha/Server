#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([myServer], [1.0.0], [muerbingsha@126.com])
AC_CONFIG_SRCDIR([include/deng.h])
AC_CONFIG_HEADERS([config.h])
AM_INIT_AUTOMAKE	#[Shark] with aclocal for automake
LT_INIT 		#[Shark] init libtool to  get .so

# Checks for programs.
AC_PROG_CC		#[Shark] check gcc
AC_PROG_CXX		#[Shark] check g++
AC_PROG_RANLIB		#[Shark] get static lib *.a
AC_PROG_LIBTOOL		#[Shark] get dynamic lib *.so
AC_LANG([C++])
AC_SUBST([CC])
AC_SUBSTR([MY_APP_VERSION])

# Checks for libraries.
AC_CHECK_LIB(c, accept4, AC_DEFINE(HAVE_ACCEPT4, 1, [have accept4]))
    AC_CHECK_LIB(c, signalfd, AC_DEFINE(HAVE_SIGNALFD, 1, [have signalfd]))
    AC_CHECK_LIB(c, timerfd_create, AC_DEFINE(HAVE_TIMERFD, 1, [have timerfd]))
    AC_CHECK_LIB(c, eventfd, AC_DEFINE(HAVE_EVENTFD, 1, [have eventfd]))
    AC_CHECK_LIB(c, epoll_create, AC_DEFINE(HAVE_EPOLL, 1, [have epoll]))
    AC_CHECK_LIB(c, poll, AC_DEFINE(HAVE_POLL, 1, [have poll]))
    AC_CHECK_LIB(c, sendfile, AC_DEFINE(HAVE_SENDFILE, 1, [have sendfile]))
    AC_CHECK_LIB(c, kqueue, AC_DEFINE(HAVE_KQUEUE, 1, [have kqueue]))
    AC_CHECK_LIB(c, backtrace, AC_DEFINE(HAVE_EXECINFO, 1, [have execinfo]))
    AC_CHECK_LIB(c, daemon, AC_DEFINE(HAVE_DAEMON, 1, [have daemon]))
    AC_CHECK_LIB(c, mkostemp, AC_DEFINE(HAVE_MKOSTEMP, 1, [have mkostemp]))
    AC_CHECK_LIB(c, inotify_init, AC_DEFINE(HAVE_INOTIFY, 1, [have inotify]))
    AC_CHECK_LIB(c, inotify_init1, AC_DEFINE(HAVE_INOTIFY_INIT1, 1, [have inotify_init1]))
    AC_CHECK_LIB(pthread, pthread_rwlock_init, AC_DEFINE(HAVE_RWLOCK, 1, [have pthread_rwlock_init]))
    AC_CHECK_LIB(pthread, pthread_spin_lock, AC_DEFINE(HAVE_SPINLOCK, 1, [have pthread_spin_lock]))
	AC_CHECK_LIB(pthread, pthread_mutex_timedlock, AC_DEFINE(HAVE_MUTEX_TIMEDLOCK, 1, [have pthread_mutex_timedlock]))
    AC_CHECK_LIB(pthread, pthread_barrier_init, AC_DEFINE(HAVE_PTHREAD_BARRIER, 1, [have pthread_barrier_init]))
    AC_CHECK_LIB(ssl, SSL_library_init, AC_DEFINE(HAVE_OPENSSL, 1, [have openssl]))
    AC_CHECK_LIB(pcre, pcre_compile, AC_DEFINE(HAVE_PCRE, 1, [have pcre]))
    AC_CHECK_LIB(hiredis, redisConnect, AC_DEFINE(HAVE_HIREDIS, 1, [have hiredis]))
    AC_CHECK_LIB(nghttp2, nghttp2_hd_inflate_new, AC_DEFINE(HAVE_NGHTTP2, 1, [have nghttp2]))



# Checks for header files.
AC_CHECK_HEADERS([daemon.h])

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

# [Shark]touch Makefile.am first, autoscan create this
AC_CONFIG_FILES([Makefile
		 src/Makefile
                 test/Makefile])
AC_OUTPUT
