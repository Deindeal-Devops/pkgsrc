# $NetBSD: Makefile,v 1.22 2019/11/02 21:09:17 rillig Exp $

DISTNAME=	wmmp3-0.12
PKGREVISION=	3
CATEGORIES=	audio
MASTER_SITES=	http://www.dotfiles.com/software/wmmp3/

MAINTAINER=	rxg@NetBSD.org
# HOMEPAGE=	http://www.dotfiles.com/software/wmmp3/
COMMENT=	Front-end for mpg123 in a Window Maker dockapp
LICENSE=	gnu-gpl-v2

DEPENDS+=	mpg123>=0.59.18:../../audio/mpg123

GNU_CONFIGURE=		yes
CONFIGURE_ARGS+=	--x-includes=${X11BASE:Q}/include
CONFIGURE_ARGS+=	--x-libraries=${X11BASE:Q}/lib${LIBABISUFFIX:Q}

INSTALLATION_DIRS=	share/examples

post-patch:
	${MV} ${WRKSRC}/sample.wmmp3 ${WRKSRC}/sample.wmmp3.orig
	${SED} -e 's:/usr/local:'${PREFIX}':g' \
		${WRKSRC}/sample.wmmp3.orig > ${WRKSRC}/sample.wmmp3

post-install:
	${INSTALL_DATA} ${WRKSRC}/sample.wmmp3 \
		${DESTDIR}${PREFIX}/share/examples

.include "../../x11/libXext/buildlink3.mk"
.include "../../x11/libXpm/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
