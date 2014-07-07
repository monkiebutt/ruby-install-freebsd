# Created by: Barry Allard <barry.allard@gmail.com>
# $FreeBSD: ruby-install/Makefile $

PORTNAME=			ruby-install
PORTVERSION=	0.4.3
CATEGORIES=		lang ruby
MASTER_SITES=	https://github.com/postmodern/ruby-install/archive/
DISTNAME= 		v${PORTVERSION}

MAINTAINER=	postmodern.mod3@gmail.com
COMMENT=	Installs Ruby, JRuby, Rubinius, MagLev or MRuby

LICENSE=MIT

RUN_DEPENDS=	bash:${PORTSDIR}/shells/bash curl:${PORTSDIR}/ftp/curl

USES+= gmake
NO_STAGE=	yes
NO_BUILD= yes
MAKE_CMD= ${GMAKE}
ALL_TARGET= install
MAN1+= ruby-install.1

WRKSRC=	${WRKDIR}/${PORTNAME}-${PORTVERSION}

DOCSDIR_REL= share/doc/${PORTNAME}-${PORTVERSION}

PLIST_SUB+= DOCSDIR_REL=${DOCSDIR_REL}
PLIST_SUB+= PORTNAME=${PORTNAME}
PLIST_SUB+= PORTVERSION=${PORTVERSION}

post-patch:
	@${REINPLACE_CMD} -e 's|share/man/|man/|g;s/DIRS=bin share/& man/' ${WRKSRC}/Makefile
	@$(MV) ${WRKSRC}/share/man ${WRKSRC}/man

.include <bsd.port.mk>
