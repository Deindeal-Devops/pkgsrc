# $NetBSD: Makefile,v 1.41 2019/12/21 14:41:32 nia Exp $

DISTNAME=	hexchat-2.14.3
CATEGORIES=	chat
MASTER_SITES=	https://dl.hexchat.net/hexchat/
EXTRACT_SUFX=	.tar.xz

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://hexchat.github.io/
COMMENT=	IRC client based on XChat
LICENSE=	gnu-gpl-v2 AND gnu-lgpl-v2.1 AND mit

USE_LIBTOOL=	yes
USE_TOOLS+=	bison gmake intltool msgfmt msgmerge pkg-config xgettext
USE_LANGUAGES=	c c++

PKGCONFIG_OVERRIDE+=	share/pkgconfig/hexchat-plugin.pc.in

# XXX fails without GNU msgfmt
_TOOLS_USE_PKGSRC.msgfmt=	yes

MESON_ARGS+=		-Dwith-text=true
MESON_ARGS+=		-Dwith-appdata=false

REPLACE_PYTHON+=	plugins/perl/generate_header.py
REPLACE_PYTHON+=	src/common/make-te.py
REPLACE_PYTHON+=	meson_post_install.py

OPSYSVARS+=		SOEXT
SOEXT.Darwin=		dylib
SOEXT.*=		so
PLIST_SUBST+=		SOEXT=${SOEXT}

LDFLAGS.SunOS+=		-lsocket -lnsl

.include "options.mk"
.include "../../devel/meson/build.mk"
.include "../../converters/libiconv/buildlink3.mk"
.include "../../devel/glib2/buildlink3.mk"
.include "../../devel/pango/buildlink3.mk"
.include "../../lang/python/pyversion.mk"
.include "../../textproc/iso-codes/buildlink3.mk"
.include "../../textproc/libxml2/buildlink3.mk"
.include "../../mk/dlopen.buildlink3.mk"
.include "../../mk/pthread.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
