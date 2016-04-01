# Created by: Barry Allard <barry.allard@gmail.com>
# $FreeBSD: ruby-install/Makefile $

PORTNAME=	ruby-install
PORTVERSION=	0.6.0
DISTVERSIONPREFIX=	v
CATEGORIES=	lang ruby

MAINTAINER=	postmodern.mod3@gmail.com
COMMENT=	Installs Ruby, JRuby, Rubinius, MagLev or MRuby

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

RUN_DEPENDS=	bash:${PORTSDIR}/shells/bash curl:${PORTSDIR}/ftp/curl

USE_GITHUB=	yes
GH_ACCOUNT=	postmodern

NO_BUILD=	yes

post-stage:
	${CP} ${WRKSRC}/share/man/man1/ruby-install.1 ${STAGEDIR}${PREFIX}/man/man1
	${GZIP_CMD} ${STAGEDIR}${PREFIX}/man/man1/ruby-install.1

.include <bsd.port.mk>
