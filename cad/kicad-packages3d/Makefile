# $NetBSD: Makefile,v 1.2 2019/08/29 15:36:40 bouyer Exp $
#

V=		5.1.4
DISTNAME=	kicad-packages3d-${V}
CATEGORIES=	cad
MASTER_SITES=	${MASTER_SITE_GITHUB:=KiCad/}
GITHUB_TAG=	${PKGVERSION_NOREV}
EXTRACT_USING=	bsdtar

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://kicad-pcb.org/
COMMENT=	3D models for rendering and the MCAD software
LICENSE=	cc-by-sa-v4.0
WRKSRC=		${WRKDIR}/kicad-packages3D-${V}

USE_CMAKE=	yes

.include "../../mk/bsd.prefs.mk"
.include "../../mk/bsd.pkg.mk"
