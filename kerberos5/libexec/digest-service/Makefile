# $FreeBSD$

.include <src.opts.mk>

.if ${MK_CHERI_USE_LLD} == "no"
# linker error
WANT_CHERI=none
.endif

PROG=	digest-service
MAN=
CFLAGS+=	-I${KRB5DIR}/kdc \
		-I${KRB5DIR}/lib/asn1 \
		-I${KRB5DIR}/lib/krb5 \
		-I${KRB5DIR}/lib/ipc \
		-I${KRB5DIR}/lib/wind \
		-I${KRB5DIR}/lib/roken
LIBADD=	hdb kdc heimipcs krb5 roken asn1 crypto vers heimntlm
LDFLAGS=${LDAPLDFLAGS}

.include <bsd.prog.mk>

.PATH: ${KRB5DIR}/kdc
