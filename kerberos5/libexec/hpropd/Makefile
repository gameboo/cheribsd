# $FreeBSD$

.include <src.opts.mk>

.if ${MK_CHERI_USE_LLD} == "no"
# linker error
WANT_CHERI=none
.endif

PROG=	hpropd
MAN=	hpropd.8
CFLAGS+=-I${KRB5DIR}/lib/roken -I${KRB5DIR}/lib/krb5 -I${KRB5DIR}/lib/asn1 \
	-I${KRB5DIR}/kdc ${LDAPCFLAGS}
LIBADD=	hdb krb5 roken vers
DPADD=	${LDAPDPADD}
LDADD=	${LDAPLDADD}
LDFLAGS=${LDAPLDFLAGS}

.include <bsd.prog.mk>

.PATH: ${KRB5DIR}/kdc
