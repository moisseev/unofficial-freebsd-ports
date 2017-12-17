# $FreeBSD$

PORTNAME=	ps2mail
PORTVERSION=	20171217
CATEGORIES=	print

MAINTAINER=	moiseev@mezonplus.ru
COMMENT=	Print-to-email lpd(8) input filter

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	p5-Email-Address>=0:mail/p5-Email-Address \
		p5-Email-Valid>=0:mail/p5-Email-Valid \
		p5-IO-Interactive>=0:devel/p5-IO-Interactive \
		p5-Locale-gettext>=0:devel/p5-Locale-gettext \
		p5-MIME-Lite>=0:mail/p5-MIME-Lite
TEST_DEPENDS=	p5-IPC-Run3>=0:devel/p5-IPC-Run3 \
		p5-IPC-Shareable>=0:devel/p5-IPC-Shareable \
		p5-Text-Template>=0:textproc/p5-Text-Template

# Ghostscript 9.21 is required to run this port
#USES=		ghostscript:run perl5
USES=		gettext perl5
USE_PERL5=	5.14+ run test

USE_GITHUB=	YES
GH_ACCOUNT=	moisseev
GH_TAGNAME=	d4065bb

NO_ARCH=	yes
TEST_TARGET=	test

SUB_FILES=	pkg-message

PLIST_FILES=	libexec/ps2mail \
		"@sample %%ETCDIR%%/ps2mail.conf.sample" \
		"@sample %%ETCDIR%%/ps2mail.newsyslog.conf.sample" \
		etc/newsyslog.conf.d/ps2mail.newsyslog.conf \
		share/locale/ru/LC_MESSAGES/ps2mail.mo

post-install:
	@${MKDIR} ${STAGEDIR}${PREFIX}/etc/newsyslog.conf.d
	${LN} -s ${ETCDIR}/ps2mail.newsyslog.conf ${STAGEDIR}${PREFIX}/etc/newsyslog.conf.d

.include <bsd.port.mk>
