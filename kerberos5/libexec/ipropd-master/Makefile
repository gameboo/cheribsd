# $FreeBSD$

.include <src.opts.mk>

.if ${MK_CHERI_USE_LLD} == "no"
# linker error
WANT_CHERI=none
.endif

PROG=	ipropd-master
MAN=	iprop.8
SRCS=	ipropd_common.c ipropd_master.c kadm5_err.h
CFLAGS+=-I${KRB5DIR}/lib/krb5 -I${KRB5DIR}/lib/asn1 -I${KRB5DIR}/lib/roken \
	-I. ${LDAPCFLAGS}
LIBADD=	kadm5srv hdb krb5 roken vers
DPADD=	${LDAPDPADD}
LDADD=	${LDAPLDADD}
LDFLAGS=${LDAPLDFLAGS}

foo::
	echo ${LIBHX509}

.include <bsd.prog.mk>

.PATH: ${KRB5DIR}/lib/kadm5
