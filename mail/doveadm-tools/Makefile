PORTNAME=	doveadm-tools
PORTVERSION=	20220610
CATEGORIES=	mail

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	Wrapper scripts set for doveadm(1)

LICENSE=	BSD2CLAUSE

RUN_DEPENDS=	dovecot>=2.2.0:mail/dovecot

FLAVORS=	default full

default_CONFLICTS_INSTALL=	${PORTNAME}-full

full_CONFLICTS_INSTALL=	${PORTNAME}
full_PKGNAMESUFFIX=	-full
full_RUN_DEPENDS+=	p5-IO-Interactive>=0:devel/p5-IO-Interactive \
			p5-IPC-Shareable>=0:devel/p5-IPC-Shareable \
			p5-Mail-Audit-Attach>=0:mail/p5-Mail-Audit-Attach
COMMENT_full=		(with doveadm-rm-attachments)

NO_BUILD=	yes
NO_ARCH=	yes

USE_GITHUB=	YES
GH_ACCOUNT=	moisseev
GH_TAGNAME=	1cc4731

PLIST_FILES=	bin/doveadm-backup \
		bin/doveadm-expunge \
		bin/doveadm-mdboxrm \
		bin/doveadm-report-last-login \
		bin/doveadm-report-quota \
		bin/doveadm-rm-savedbefore \
		bin/dsisck \
		"@sample etc/doveadm-backup.conf.sample"

.if ${FLAVOR:U} == full
PLIST_FILES+=	bin/doveadm-rm-attachments
.endif

post-install:
.if ${FLAVOR:U} != full
	${RM} ${STAGEDIR}${PREFIX}/bin/doveadm-rm-attachments
.endif

.include <bsd.port.mk>
