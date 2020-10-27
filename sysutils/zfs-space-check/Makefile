# $FreeBSD$

PORTNAME=	zfs-space-check
PORTVERSION=	20201027
CATEGORIES=	sysutils

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	Low space alerting tool for ZFS

LICENSE=	BSD2CLAUSE

USES=		perl5
NO_BUILD=	yes

USE_GITHUB=	YES
GH_ACCOUNT=	moisseev
GH_TAGNAME=	54e4879

PLIST_FILES=	bin/zfs-space-check \
		"@sample etc/zfs-space-check.conf.sample" \
		"@owner nobody" "@group nobody" \
		"@dir /var/db/zfs-space-check"

.include <bsd.port.mk>
