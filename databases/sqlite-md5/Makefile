# $FreeBSD$

PORTNAME=	sqlite-md5
PORTVERSION=	0.0.1
CATEGORIES=	databases

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	MD5 message-digest algorithm library for SQLite

LICENSE=	public
LICENSE_NAME=	Public Domain
LICENSE_TEXT=	The code is public domain.
LICENSE_PERMS=	dist-mirror dist-sell pkg-mirror pkg-sell auto-accept

USE_GITHUB= YES
GH_ACCOUNT= moisseev
GH_TAGNAME= 7ba63df

USE_SQLITE=	yes
USE_LDCONFIG=	yes

OPTIONS_DEFINE=	DOCS

PORTDOCS=	*

.include <bsd.port.options.mk>

PLIST_FILES+=	lib/libsqlitemd5.so

do-install:
	${INSTALL_LIB} ${WRKSRC}/libsqlitemd5.so ${STAGEDIR}${PREFIX}/lib
.if ${PORT_OPTIONS:MDOCS}
	${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/README.md ${STAGEDIR}${DOCSDIR}
.endif

.include <bsd.port.mk>
