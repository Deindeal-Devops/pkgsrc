# $NetBSD: Makefile,v 1.2 2020/01/05 12:16:59 nia Exp $

DISTNAME=	herbstluftwm-0.7.2
CATEGORIES=	wm
MASTER_SITES=	https://herbstluftwm.org/tarballs/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://herbstluftwm.org/
COMMENT=	Manual tiling window manager for X11 using Xlib and Glib
LICENSE=	modified-bsd

TOOL_DEPENDS+=	asciidoc-[0-9]*:../../textproc/asciidoc

USE_CMAKE=	yes
USE_TOOLS+=	pkg-config bash:run
USE_LANGUAGES=	c c++

CONFIGURE_DIRS=	build
CMAKE_ARG_PATH=	..

CFLAGS.NetBSD+=	-D_NETBSD_SOURCE

REPLACE_BASH+=	share/dmenu_run_hlwm

pre-configure:
	${MKDIR} -p ${WRKSRC}/build

.include "../../devel/glib2/buildlink3.mk"
.include "../../x11/libXext/buildlink3.mk"
.include "../../x11/libXinerama/buildlink3.mk"
.include "../../x11/libX11/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
