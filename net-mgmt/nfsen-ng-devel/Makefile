PORTNAME=	nfsen-ng
PORTVERSION=	0.3.1.a1.20240420
DISTVERSIONPREFIX=	v
CATEGORIES=	net-mgmt
PKGNAMESUFFIX=	-devel${PHP_PKGNAMESUFFIX}

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	Web based frontend for nfdump netflow collector dev version
WWW=		https://github.com/mbolli/nfsen-ng

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PHP_PKGNAMEPREFIX}pecl-rrd>0:databases/pecl-rrd@${PHP_FLAVOR} \
		nfdump>=0:net-mgmt/nfdump

USES=		php:flavors
USE_RC_SUBR=	nfsen-ng

CONFLICTS_INSTALL=	nfsen-ng

WWWDIR?=	${PREFIX}/www/${PORTNAME}

NO_BUILD=	yes
NO_ARCH=	yes

SUB_FILES=	pkg-message

USE_GITHUB=	YES
GH_ACCOUNT=	mbolli
GH_TAGNAME=	cb3d819

post-patch:
	@${REINPLACE_CMD} -e 's|^#!/usr/bin/env php$$|#!${PREFIX}/bin/php|' ${WRKSRC}/backend/cli.php
	@${REINPLACE_CMD} -e 's|^#!/usr/bin/php$$|#!${PREFIX}/bin/php|' ${WRKSRC}/backend/listen.php
	@${REINPLACE_CMD} -e 's|'/usr/bin/nfdump'|${PREFIX}/bin/nfdump|' ${WRKSRC}/backend/settings/settings.php.dist

do-install:
	${MKDIR} ${STAGEDIR}${WWWDIR}
	cd ${WRKSRC} && ${COPYTREE_SHARE} \* ${STAGEDIR}${WWWDIR}
	${MKDIR} ${STAGEDIR}${WWWDIR}/backend/datasources/data
	cd ${STAGEDIR}${WWWDIR}/backend/settings && \
		${MV} settings.php.dist settings.php.sample

.include <bsd.port.mk>
