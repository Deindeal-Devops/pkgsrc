# $NetBSD: Makefile,v 1.20 2020/01/12 20:19:56 ryoon Exp $

DISTNAME=	librime-1.0
PKGREVISION=	15
CATEGORIES=	inputmethod chinese
MASTER_SITES=	http://rimeime.googlecode.com/files/
#MASTER_SITES=	http://dl.bintray.com/lotem/rime/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://rime.im/
COMMENT=	Rime input method engine
LICENSE=	gnu-gpl-v3

WRKSRC=		${WRKDIR}/librime
USE_CMAKE=	yes
USE_TOOLS+=	pkg-config
USE_LANGUAGES=	c c++

PKGCONFIG_OVERRIDE+=	rime.pc.in

.include "options.mk"

.include "../../converters/opencc/buildlink3.mk"
.include "../../databases/kyotocabinet/buildlink3.mk"
.include "../../devel/boost-libs/buildlink3.mk"
.include "../../devel/google-glog/buildlink3.mk"
.include "../../devel/zlib/buildlink3.mk"
.include "../../textproc/yaml-cpp/buildlink3.mk"
.include "../../x11/xorgproto/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
