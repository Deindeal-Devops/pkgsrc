# $NetBSD: Makefile,v 1.2 2020/01/13 02:26:55 mef Exp $

R_PKGNAME=	cliapp
R_PKGVER=	0.1.0
CATEGORIES=	devel

MAINTAINER=	pkgsrc-users@NetBSD.org
COMMENT=	Create Rich Command Line Applications
LICENSE=	mit	# + file LICENSE

DEPENDS+=	R-cli>=1.1.0:../../devel/R-cli
DEPENDS+=	R-crayon>=1.3.4:../../devel/R-crayon
DEPENDS+=	R-fansi>=0.4.0:../../devel/R-fansi
DEPENDS+=	R-glue>=1.3.0:../../devel/R-glue
DEPENDS+=	R-withr>=2.1.2:../../devel/R-withr
DEPENDS+=	R-xml2>=1.2.2nb1:../../textproc/R-xml2

TEST_DEPENDS+=	R-progress-[0-9]*:../../sysutils/R-progress
TEST_DEPENDS+=	R-callr-[0-9]*:../../devel/R-callr
TEST_DEPENDS+=	R-covr-[0-9]*:../../devel/R-covr
TEST_DEPENDS+=	R-prettycode-[0-9]*:../../devel/R-prettycode
TEST_DEPENDS+=	R-rstudioapi-[0-9]*:../../math/R-rstudioapi
TEST_DEPENDS+=	R-selectr-[0-9]*:../../textproc/R-selectr

USE_LANGUAGES=	# none

.include "../../math/R/Makefile.extension"
.include "../../sysutils/R-progress/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
