# $NetBSD: Makefile,v 1.34 2019/12/31 12:27:03 wiz Exp $
#
# history: upstream renamed 0.11 to 0.1.1;
# we have to use the old-style convention so that version compares work.

VER=		0.9.3
DISTNAME=	libssh-${VER}
PKGNAME=	libssh-0.93
CATEGORIES=	security
MASTER_SITES=	https://www.libssh.org/files/${VER:R}/
EXTRACT_SUFX=	.tar.xz

MAINTAINER=	is@NetBSD.org
HOMEPAGE=	http://www.libssh.org/
COMMENT=	SSHv2+v1 protocol library
LICENSE=	2-clause-bsd

USE_CMAKE=		yes
USE_LANGUAGES=		c c++
PKGCONFIG_OVERRIDE+=	libssh.pc.cmake
TEST_TARGET=		test

CONFIGURE_DIRS=		${WRKDIR}/build
CMAKE_ARG_PATH=		${WRKSRC}
CMAKE_ARGS+=		-DUNIT_TESTING=ON

LDFLAGS.SunOS+=		-lnsl -lsocket

BUILDLINK_TRANSFORM+=	rm:-Werror=strict-overflow

.include "options.mk"

post-extract:
	${MKDIR} ${WRKDIR}/build

.include "../../devel/argp/buildlink3.mk"
.include "../../devel/cmocka/buildlink3.mk"
.include "../../devel/zlib/buildlink3.mk"
.include "../../mk/krb5.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
