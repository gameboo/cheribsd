#	@(#)Makefile	8.6 (Berkeley) 5/8/95
# $FreeBSD$

# broken: bad address
WANT_CHERI=none

PACKAGE=runtime
PROG=	mount
SRCS=	mount.c mount_fs.c getmntopts.c vfslist.c
MAN=	mount.8 mount.conf.8
# We do NOT install the getmntopts.3 man page.

LIBADD=	util

WANT_DUMP=	yes

.include <bsd.prog.mk>
