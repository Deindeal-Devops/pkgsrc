# $NetBSD: Makefile,v 1.99 2019/04/07 22:02:20 wiz Exp $

DISTNAME=	gc-8.0.4
PKGNAME=	${DISTNAME:S/gc/boehm-gc/}
CATEGORIES=	devel
MASTER_SITES=	http://www.hboehm.info/gc/gc_source/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.hboehm.info/gc/
COMMENT=	Garbage collection and memory leak detection for C and C++

USE_TOOLS+=		gmake pkg-config
USE_LANGUAGES=		c c++
USE_LIBTOOL=		YES
GNU_CONFIGURE=		YES
CONFIGURE_ARGS+=	--enable-cplusplus
CONFIGURE_ARGS+=	--datadir=${PREFIX}/share/doc
PKGCONFIG_OVERRIDE=	bdw-gc.pc.in
INSTALLATION_DIRS=	${PKGMANDIR}/man3

TEST_TARGET=		check

.include "../../mk/bsd.prefs.mk"

.if !empty(MACHINE_PLATFORM:MDarwin-10.6.*)
CFLAGS+=		-D_XOPEN_SOURCE
.endif

.include "options.mk"

post-install:
	${INSTALL_MAN} ${WRKSRC}/doc/gc.man ${DESTDIR}${PREFIX}/${PKGMANDIR}/man3/gc.3

# historical pkgsrc test target, can be removed in one of the next updates
.PHONY: manual-do-test
manual-do-test:
	cd ${WRKSRC} && \
	${RM} -f gctest && ${MAKE_PROGRAM} gctest && ./gctest && \
	${RM} -f test_cpp && ${MAKE_PROGRAM} test_cpp && ./test_cpp 10

.include "../../devel/libatomic_ops/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
