# $NetBSD: Makefile,v 1.27 2020/01/13 00:57:18 joerg Exp $

.include "../../print/poppler/Makefile.common"

PKGREVISION=	1
PKGNAME=	poppler-includes-${POPPLER_VERS}

COMMENT=	Poppler Xpdf includes (unsupported)

CONFLICTS+=	poppler-0.5.1{,nb*}

NO_BUILD=	yes

CMAKE_ARGS+=	-DENABLE_XPDF_HEADERS=ON

INCDIR=	${DESTDIR}${PREFIX}/include

.include "../../mk/bsd.prefs.mk"

do-install:
	${INSTALL_DATA_DIR} ${INCDIR}
	${INSTALL_DATA_DIR} ${INCDIR}/poppler
	sed -n -f ${FILESDIR}/extract.sed ${WRKSRC}/CMakeLists.txt	\
	  | grep ^poppler/ | { while read f; do				\
	    ${INSTALL_DATA} ${WRKSRC}/"$$f" ${INCDIR}/poppler;		\
	done };
	${INSTALL_DATA} ${WRKSRC}/poppler/poppler-config.h ${INCDIR}/poppler
	for d in goo fofi splash; do					\
	    ${INSTALL_DATA_DIR} ${INCDIR}/poppler/"$$d";		\
	    sed -n -f ${FILESDIR}/extract.sed ${WRKSRC}/CMakeLists.txt	\
	      | grep "^$$d/" | { while read f; do			\
		${INSTALL_DATA} ${WRKSRC}/"$$f" ${INCDIR}/poppler/"$$d";\
	    done };							\
	done
	# do these actually belong here?
	${INSTALL_DATA} ${WRKSRC}/poppler/SignatureInfo.h ${INCDIR}/poppler
	${INSTALL_DATA} ${WRKSRC}/goo/NetPBMWriter.h ${INCDIR}/poppler/goo

BUILDLINK_DEPMETHOD.fontconfig= build
.include "../../fonts/fontconfig/buildlink3.mk"
.include "../../mk/jpeg.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
