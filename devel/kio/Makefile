# $NetBSD: Makefile,v 1.34 2019/11/11 07:57:10 markd Exp $

DISTNAME=	kio-${KF5VER}
CATEGORIES=	devel

HOMEPAGE=	https://community.kde.org/Frameworks
COMMENT=	Resource and network access abstraction
LICENSE=	gnu-lgpl-v2.1

.include "../../meta-pkgs/kde/kf5.mk"

USE_TOOLS+=	msgmerge

#CMAKE_ARGS+=	-DKAUTH_DBUS_DIR=${PREFIX}/share/examples/kio

LDFLAGS.SunOS+=	-lsocket

SUBST_CLASSES+=		xdg
SUBST_STAGE.xdg=	pre-configure
SUBST_MESSAGE.xdg=	Install via examples dir.
SUBST_FILES.xdg=	src/core/CMakeLists.txt CMakeLists.txt
SUBST_FILES.xdg+=	src/urifilters/shorturi/CMakeLists.txt
SUBST_SED.xdg=		-e 's:{KDE_INSTALL_CONFDIR}:{KDE_INSTALL_XDG_EX_DIR}:'

MAKE_DIRS+=	${PKG_SYSCONFDIR}/xdg
CONF_FILES+=	${PREFIX}/share/examples/kde-xdg/accept-languages.codes \
		${PKG_SYSCONFDIR}/xdg/accept-languages.codes
CONF_FILES+=	${PREFIX}/share/examples/kde-xdg/kshorturifilterrc \
		${PKG_SYSCONFDIR}/xdg/kshorturifilterrc

# generation of kcookieserver.moc fails when ${PREFIX}/include in the moc include path
SUBST_CLASSES+=		fix-moc
SUBST_STAGE.fix-moc=	post-configure
SUBST_MESSAGE.fix-moc=	Cleaning up MOC includes
SUBST_FILES.fix-moc=	_KDE_build/src/ioslaves/http/kcookiejar/CMakeFiles/kded_kcookiejar_autogen.dir/AutogenInfo.cmake
SUBST_FILES.fix-moc+=	_KDE_build/src/ioslaves/trash/CMakeFiles/kcm_trash_autogen.dir/AutogenInfo.cmake
SUBST_FILES.fix-moc+=	_KDE_build/src/urifilters/ikws/CMakeFiles/kurisearchfilter_autogen.dir/AutogenInfo.cmake
SUBST_FILES.fix-moc+=	_KDE_build/autotests/CMakeFiles/jobremotetest_autogen.dir/AutogenInfo.cmake
SUBST_FILES.fix-moc+=	_KDE_build/src/kcms/kio/CMakeFiles/kcm_kio_autogen.dir/AutogenInfo.cmake
SUBST_SED.fix-moc=	-e 's,;${PREFIX}/include;,;,g'

.include "../../devel/zlib/buildlink3.mk"
.include "../../mk/krb5.buildlink3.mk"
.include "../../archivers/karchive/buildlink3.mk"
.include "../../devel/kbookmarks/buildlink3.mk"
.include "../../devel/kdoctools/buildlink3.mk"
.include "../../security/kwallet/buildlink3.mk"
.include "../../sysutils/solid/buildlink3.mk"
.include "../../x11/kjobwidgets/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../x11/qt5-qtscript/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
