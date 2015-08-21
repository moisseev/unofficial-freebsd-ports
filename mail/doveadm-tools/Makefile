# $FreeBSD$

PORTNAME=	doveadm-tools
PORTVERSION=	20150821
CATEGORIES=	mail

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	Wrapper scripts set for doveadm(1)

LICENSE=	BSD2CLAUSE

RUN_DEPENDS=	dovecot2>=2.2.0:${PORTSDIR}/mail/dovecot2

NO_BUILD=	yes

USE_GITHUB=	YES
GH_ACCOUNT=	moisseev
GH_TAGNAME=	445019caaa

PLIST_FILES=	bin/doveadm-expunge \
		bin/doveadm-mdboxrm \
		bin/doveadm-report-quota \
		bin/doveadm-backup \
		"@sample etc/doveadm-backup.conf.sample"

.include <bsd.port.mk>
