# $NetBSD: Makefile,v 1.11 2019/11/18 20:01:03 adam Exp $

DISTNAME=	fs-uae-3.0.2
CATEGORIES=	emulators
MASTER_SITES=	https://fs-uae.net/stable/${PKGVERSION_NOREV}/

MAINTAINER=	adam@NetBSD.org
HOMEPAGE=	https://fs-uae.net/
COMMENT=	FS-UAE Amiga Emulator
LICENSE=	gnu-gpl-v2

USE_LANGUAGES=		c gnu++03
USE_TOOLS+=		msgfmt pkg-config zip
GNU_CONFIGURE=		yes
CONFIGURE_ARGS+=	--with-libmpeg2

NOT_PAX_MPROTECT_SAFE+=	bin/fs-uae

.include "../../mk/bsd.prefs.mk"
.if ${OPSYS} == "Darwin"
#OPENAL_CFLAGS="-framework OpenAL"
.else
.include "../../audio/openal-soft/buildlink3.mk"
.include "../../graphics/MesaLib/buildlink3.mk"
.include "../../graphics/glu/buildlink3.mk"
.include "../../x11/libX11/buildlink3.mk"
.include "../../x11/libXi/buildlink3.mk"
.endif
.include "../../devel/SDL2/buildlink3.mk"
.include "../../devel/glib2/buildlink3.mk"
.include "../../devel/zlib/buildlink3.mk"
.include "../../graphics/freetype2/buildlink3.mk"
.include "../../graphics/glew/buildlink3.mk"
.include "../../graphics/hicolor-icon-theme/buildlink3.mk"
.include "../../graphics/png/buildlink3.mk"
.include "../../multimedia/libmpeg2/buildlink3.mk"
.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../mk/bsd.pkg.mk"
