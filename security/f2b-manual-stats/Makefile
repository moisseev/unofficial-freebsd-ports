PORTNAME=	f2b-manual-stats
PORTVERSION=	20260726
CATEGORIES=	security

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	Persistent pf counter statistics for fail2ban's [manual] jail
WWW=		https://github.com/moisseev/f2b-manual-stats

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		perl5
USE_PERL5=	build run

USE_GITHUB=	YES
GH_ACCOUNT=	moisseev
GH_TAGNAME=	e841e52

NO_BUILD=	yes
NO_ARCH=	yes

PLIST_FILES=	bin/f2b-manual-stats \
		man/man1/f2b-manual-stats.1.gz

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin/
	${MKDIR} ${STAGEDIR}${PREFIX}/man/man1
	pod2man --section=1 --release="${PORTVERSION}" \
		--center="${PORTNAME} manual" \
		${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/man/man1/${PORTNAME}.1
	${GZIP_CMD} ${STAGEDIR}${PREFIX}/man/man1/${PORTNAME}.1

.include <bsd.port.mk>
