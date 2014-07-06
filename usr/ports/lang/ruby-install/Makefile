# Created by: Akinori MUSHA aka knu <knu@idaemons.org>
# $FreeBSD: head/lang/ruby21/Makefile 355900 2014-05-30 19:20:24Z swills $

PORTNAME=	ruby-install
PORTVERSION=	0.4.3
DISTNAME= v${PORTVERSION}
WRKSRC=		${WRKDIR}/${PORTNAME}-${PORTVERSION}
CATEGORIES=	lang ruby
NO_STAGE=	yes
NO_BUILD= yes
MAKE_CMD= ${GMAKE}
ALL_TARGET= install
MAN1+= ruby-install.1

# https://github.com/postmodern/ruby-install/archive/v0.4.3.tar.gz
MASTER_SITES=	https://github.com/postmodern/ruby-install/archive/

MAINTAINER=	postmodern.mod3@gmail.com
COMMENT?=	Installs Ruby, JRuby, Rubinius, MagLev or MRuby

LICENSE=	MIT

USES=	gmake
RUN_DEPENDS=	bash:${PORTSDIR}/shells/bash curl:${PORTSDIR}/ftp/curl
WRKSRC=	${WRKDIR}/${PORTNAME}-${PORTVERSION}

DOCSDIR_REL= share/doc/${PORTNAME}-${PORTVERSION}

PLIST_SUB+= DOCSDIR_REL=${DOCSDIR_REL}
PLIST_SUB+= PORTNAME=${PORTNAME}
PLIST_SUB+= PORTVERSION=${PORTVERSION}

post-patch:
	@${REINPLACE_CMD} -e 's|share/man/|man/|g;s/DIRS=bin share/& man/' ${WRKSRC}/Makefile
	@mv ${WRKSRC}/share/man ${WRKSRC}/man

.include <bsd.port.mk>
