# $NetBSD: Makefile,v 1.16 2020/01/16 08:22:41 adam Exp $

DISTNAME=	six-1.14.0
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	devel lang python
MASTER_SITES=	${MASTER_SITE_PYPI:=s/six/}

MAINTAINER=	nils@NetBSD.org
HOMEPAGE=	https://github.com/benjaminp/six
COMMENT=	Python 2 and 3 compatibility utilities
LICENSE=	mit

TEST_DEPENDS+=	${PYPKGPREFIX}-test-[0-9]*:../../devel/py-test

USE_LANGUAGES=	# none

do-test:
	cd ${WRKSRC} && pytest-${PYVERSSUFFIX}

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
