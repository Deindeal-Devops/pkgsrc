# $NetBSD: Makefile,v 1.32 2019/09/16 19:24:55 adam Exp $

DISTNAME=	qtwebchannel-everywhere-src-${QTVERSION}
PKGNAME=	qt5-qtwebchannel-${QTVERSION}
COMMENT=	Qt5 WebChannel module

MAKE_ENV+=		QTDIR=${QTDIR}
INSTALL_ENV+=		INSTALL_ROOT=${DESTDIR}
INSTALLATION_DIRS+=	lib/pkgconfig

.include "../../x11/qt5-qtbase/Makefile.common"

post-install:
.for i in Qt5WebChannel.pc
	cd ${DESTDIR}${PREFIX}/lib/pkgconfig && \
	${LN} -f -s ${QTPREFIX}/lib/pkgconfig/${i} ${i}
.endfor

.include "../../x11/qt5-qtdeclarative/buildlink3.mk"
.include "../../x11/qt5-qtwebsockets/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
