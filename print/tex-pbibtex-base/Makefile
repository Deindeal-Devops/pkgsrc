# $NetBSD: Makefile,v 1.2 2019/12/06 20:23:00 markd Exp $

DISTNAME=	pbibtex-base
PKGNAME=	tex-${DISTNAME}-0.0.2016
TEXLIVE_REV=	40986

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://ctan.org/pkg/pbibtex-base
COMMENT=	Bibliography styles and miscellaneous files for pBibTeX
LICENSE=	modified-bsd

CONFLICTS+=	tex-ptex<=3.2pl36135

post-patch:
	mkdir ${WRKSRC}/texmf-dist
	mv ${WRKSRC}/pbibtex ${WRKSRC}/texmf-dist/pbibtex

TEXLIVE_UNVERSIONED=	yes
.include "../../print/texlive/package.mk"
.include "../../mk/bsd.pkg.mk"
