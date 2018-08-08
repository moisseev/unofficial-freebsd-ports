# $FreeBSD$

PORTNAME=	multiwol
PORTVERSION=	20180808
CATEGORIES=	net

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	Perl CGI script for power up computers remotely (WoL)

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	p5-CGI>=0:www/p5-CGI \
		p5-IO-Interface>=0:net/p5-IO-Interface \
		p5-Locale-gettext>=0:devel/p5-Locale-gettext \
		p5-Net-ARP>=0:net/p5-Net-ARP \
		p5-Net-Wake>=0:net/p5-Net-Wake

USES=		gettext perl5
USE_PERL5=	5.14+ run

USE_GITHUB=	YES
GH_ACCOUNT=	moisseev
GH_TAGNAME=	ba8f055

NO_BUILD=	yes
NO_ARCH=	yes

PLIST_FILES=	"@(,,0755) ${WWWDIR}/multiwol.pl" \
		${WWWDIR}/locale/ru/LC_MESSAGES/multiwol.mo \
		${WWWDIR}/locale/ru/LC_MESSAGES/multiwol.po \
		${WWWDIR}/static/multiwolico.png \
		${WWWDIR}/static/multiwolico48.png \
		"@sample ${WWWDIR}/multiwol.conf.sample" \
		"@dir(${WWWOWN},${WWWGRP},) ${WWWDIR}"

do-install:
	cd ${WRKSRC}/multiwol && ${COPYTREE_SHARE} . ${STAGEDIR}${WWWDIR} "! -name ChangeLog"

.include <bsd.port.mk>
