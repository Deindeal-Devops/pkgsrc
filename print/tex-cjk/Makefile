# $NetBSD: Makefile,v 1.4 2019/12/06 20:19:09 markd Exp $

DISTNAME=	cjk
PKGNAME=	tex-${DISTNAME}-4.8.4
TEXLIVE_REV=	36951

MAINTAINER=	rxg@NetBSD.org,hubertf@NetBSD.org
HOMEPAGE=	http://ctan.org/pkg/cjk
COMMENT=	CJK language support
LICENSE=	gnu-gpl-v2

DEPENDS+=	tex-arphic-[0-9]*:../../fonts/tex-arphic
DEPENDS+=	tex-fontspec-[0-9]*:../../fonts/tex-fontspec
DEPENDS+=	tex-garuda-c90-[0-9]*:../../fonts/tex-garuda-c90
DEPENDS+=	tex-graphics-[0-9]*:../../print/tex-graphics
DEPENDS+=	tex-ifxetex-[0-9]*:../../print/tex-ifxetex
DEPENDS+=	tex-latex-[0-9]*:../../print/tex-latex
DEPENDS+=	tex-latex-bin-[0-9]*:../../print/tex-latex-bin
DEPENDS+=	tex-norasi-c90-[0-9]*:../../fonts/tex-norasi-c90
DEPENDS+=	tex-oberdiek-[0-9]*:../../print/tex-oberdiek
DEPENDS+=	tex-uhc-[0-9]*:../../fonts/tex-uhc
DEPENDS+=	tex-ulem-[0-9]*:../../print/tex-ulem
DEPENDS+=	tex-wadalab-[0-9]*:../../fonts/tex-wadalab

TEXLIVE_UNVERSIONED=	yes
.include "../../print/texlive/package.mk"
.include "../../mk/bsd.pkg.mk"
