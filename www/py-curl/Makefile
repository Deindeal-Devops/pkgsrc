# $NetBSD: Makefile,v 1.66 2020/01/12 20:20:49 ryoon Exp $

DISTNAME=	pycurl-7.43.0.3
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:S/py//}
PKGREVISION=	1
CATEGORIES=	www python
MASTER_SITES=	${MASTER_SITE_GITHUB:=pycurl/}
GITHUB_PROJECT= pycurl
GITHUB_TAG=	REL_7_43_0_3

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://pycurl.io/
COMMENT=	Python module interface to the cURL library
LICENSE=	gnu-lgpl-v2.1 OR mit

PYSETUPARGS=	--with-openssl
MAKE_FLAGS+=	PYTHON=${PYTHONBIN}

pre-build:
	cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${MAKE} ${MAKE_FLAGS}

BUILDLINK_API_DEPENDS.curl+=	curl>=7.19.0
.include "../../www/curl/buildlink3.mk"
.include "../../lang/python/distutils.mk"
.include "../../mk/bsd.pkg.mk"
