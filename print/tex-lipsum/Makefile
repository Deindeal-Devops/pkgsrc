# $NetBSD: Makefile,v 1.4 2019/12/06 20:21:53 markd Exp $

DISTNAME=	lipsum
PKGNAME=	tex-${DISTNAME}-2.2
TEXLIVE_REV=	49610

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://ctan.org/pkg/lipsum
COMMENT=	Easy access to the Lorem Ipsum dummy text
LICENSE=	lppl-1.3c

DEPENDS+=	tex-latex-bin-[0-9]*:../../print/tex-latex-bin

TEXLIVE_UNVERSIONED=	yes
.include "../../print/texlive/package.mk"
.include "../../mk/bsd.pkg.mk"
