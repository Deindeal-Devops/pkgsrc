# $NetBSD: Makefile,v 1.32 2019/08/30 00:34:31 gutteridge Exp $

.include "../../meta-pkgs/xfce4/Makefile.common"

DISTNAME=	xfce4-screenshooter-1.9.6
CATEGORIES=	misc
MASTER_SITES=	http://archive.xfce.org/src/apps/xfce4-screenshooter/1.9/

HOMEPAGE=	http://archive.xfce.org/src/apps/xfce4-screenshooter/1.9/
COMMENT=	Xfce screenshoot application

GNU_CONFIGURE=	yes
USE_LIBTOOL=	yes

.include "../../x11/xfce4-panel/buildlink3.mk"
.include "../../x11/xfce4-exo/buildlink3.mk"
.include "../../net/libsoup/buildlink3.mk"
.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../graphics/hicolor-icon-theme/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
