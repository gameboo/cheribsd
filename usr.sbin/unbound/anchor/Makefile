# $FreeBSD$

.include <src.opts.mk>

.if ${MK_CHERI_USE_LLD} == "no"
# linker error
WANT_CHERI=none
.endif

# Vendor sources and generated files
LDNSDIR= ${SRCTOP}/contrib/ldns
UNBOUNDDIR= ${SRCTOP}/contrib/unbound
EXPATDIR= ${SRCTOP}/contrib/expat

.PATH: ${UNBOUNDDIR} ${UNBOUNDDIR}/smallapp ${UNBOUNDDIR}/doc

PROG=	unbound-anchor
SRCS=	unbound-anchor.c
CFLAGS+=	-I${UNBOUNDDIR} -I${LDNSDIR} -I${EXPATDIR}/lib
LIBADD=	unbound bsdxml ssl crypto pthread
MAN=	unbound-anchor.8

.include <bsd.prog.mk>
