# $FreeBSD$

PORTNAME=	doveadm-tools
PORTVERSION=	20180618
CATEGORIES=	mail

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	Wrapper scripts set for doveadm(1)

LICENSE=	BSD2CLAUSE

RUN_DEPENDS=	dovecot>=2.2.0:mail/dovecot

NO_BUILD=	yes
NO_ARCH=	yes

USE_GITHUB=	YES
GH_ACCOUNT=	moisseev
GH_TAGNAME=	9c5e712

PLIST_FILES=	bin/doveadm-backup \
		bin/doveadm-expunge \
		bin/doveadm-mdboxrm \
		bin/doveadm-report-last-login \
		bin/doveadm-report-quota \
		bin/doveadm-rm-savedbefore \
		bin/dsisck \
		"@sample etc/doveadm-backup.conf.sample"

.include <bsd.port.mk>
