PORTNAME=	zfs-space-check
PORTVERSION=	20210610
CATEGORIES=	sysutils

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	Low space alerting tool for ZFS

LICENSE=	BSD2CLAUSE

USES=		perl5
NO_BUILD=	yes

USE_GITHUB=	YES
GH_ACCOUNT=	moisseev
GH_TAGNAME=	ff2dd56

PLIST_FILES=	bin/zfs-space-check \
		"@sample etc/zfs-space-check.conf.sample" \
		"@owner nobody" "@group nobody" \
		"@dir /var/db/zfs-space-check"

.include <bsd.port.mk>
