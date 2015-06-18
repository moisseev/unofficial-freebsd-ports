# $FreeBSD$

PORTNAME=	doveadm-tools
PORTVERSION=	20150618
CATEGORIES=	mail

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	Wrapper scripts set for doveadm(1)

LICENSE=	BSD2CLAUSE

RUN_DEPENDS=	dovecot2>=2.2.0:${PORTSDIR}/mail/dovecot2

NO_BUILD=	yes

USE_GITHUB=	YES
GH_ACCOUNT=	moisseev
GH_PROJECT=	${PORTNAME}
GH_TAGNAME=	314105c51a

PLIST_FILES=	bin/doveadm-expunge \
		bin/doveadm-mdboxrm \
		bin/doveadm-report-quota

.include <bsd.port.mk>
