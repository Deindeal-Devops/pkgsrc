# $NetBSD: Makefile,v 1.2 2019/12/06 20:22:02 markd Exp $

DISTNAME=	milog
PKGNAME=	tex-${DISTNAME}-1.0
TEXLIVE_REV=	41610

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://ctan.org/pkg/milog
COMMENT=	Fulfilling the documentation duties according to the German minimum wage law
LICENSE=	lppl-1.3c

DEPENDS+=	tex-pgfplots-[0-9]*:../../print/tex-pgfplots

TEXLIVE_UNVERSIONED=	yes
.include "../../print/texlive/package.mk"
.include "../../mk/bsd.pkg.mk"
