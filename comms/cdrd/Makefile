# $FreeBSD$

PORTNAME=	cdrd
PORTVERSION=	0.0.1
CATEGORIES=	comms

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	Simple CDR/SMDR logger daemon

LICENSE=	BSD2CLAUSE

NO_BUILD=	yes

USE_GITHUB=	YES
GH_ACCOUNT=	moisseev
GH_TAGNAME=	6f69a24

USE_RC_SUBR=	cdrd

PORTDOCS=	FAQ LICENSE README.md

OPTIONS_DEFINE=	DOCS

PLIST_FILES=	bin/cdrd \
		%%ETCDIR%%/cdrd.conf.default \
		"@sample %%ETCDIR%%/cdrd.conf.sample" \
		man/man1/cdrd.1.gz \
		"@dir /var/log/cdrd" \
		"@dir /var/run/cdrd"

post-install:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${PORTDOCS:S|^|${WRKSRC}/|} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
