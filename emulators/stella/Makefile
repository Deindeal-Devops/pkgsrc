# $NetBSD: Makefile,v 1.51 2019/11/10 21:54:58 nia Exp $

DISTNAME=	stella-6.0.2-src
PKGNAME=	${DISTNAME:S/-src//1}
CATEGORIES=	emulators
MASTER_SITES=	${MASTER_SITE_GITHUB:=stella-emu/}
GITHUB_RELEASE=	${PKGVERSION_NOREV}
EXTRACT_SUFX=	.tar.xz

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://stella-emu.github.io/
COMMENT=	Multi-platform Atari 2600 VCS emulator
LICENSE=	gnu-gpl-v2

WRKSRC=		${WRKDIR}/${PKGNAME_NOREV}
USE_LANGUAGES=	c c++14
USE_TOOLS+=	gmake

# c++14
GCC_REQD+=	5

UNLIMIT_RESOURCES=	datasize

HAS_CONFIGURE=		YES
CONFIGURE_ARGS+=	--prefix=${PREFIX}

.include "../../devel/SDL2/buildlink3.mk"
.include "../../devel/zlib/buildlink3.mk"
.include "../../graphics/hicolor-icon-theme/buildlink3.mk"
.include "../../graphics/png/buildlink3.mk"
.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../mk/pthread.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
