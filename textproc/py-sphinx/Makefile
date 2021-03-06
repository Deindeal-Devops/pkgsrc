# $NetBSD: Makefile,v 1.69 2019/12/31 10:38:46 adam Exp $

DISTNAME=	Sphinx-2.3.1
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:tl}
CATEGORIES=	textproc python
MASTER_SITES=	${MASTER_SITE_PYPI:=S/Sphinx/}

MAINTAINER=	markd@NetBSD.org
HOMEPAGE=	http://www.sphinx-doc.org/
COMMENT=	Python documentation generator
LICENSE=	modified-bsd

DEPENDS+=	${PYPKGPREFIX}-alabaster>=0.7:../../textproc/py-alabaster
DEPENDS+=	${PYPKGPREFIX}-babel>=1.3:../../devel/py-babel
DEPENDS+=	${PYPKGPREFIX}-docutils>=0.12:../../textproc/py-docutils
DEPENDS+=	${PYPKGPREFIX}-imagesize-[0-9]*:../../graphics/py-imagesize
DEPENDS+=	${PYPKGPREFIX}-jinja2>=2.3:../../textproc/py-jinja2
DEPENDS+=	${PYPKGPREFIX}-packaging-[0-9]*:../../devel/py-packaging
DEPENDS+=	${PYPKGPREFIX}-pygments>=2.0:../../textproc/py-pygments
DEPENDS+=	${PYPKGPREFIX}-pytz-[0-9]*:../../time/py-pytz
DEPENDS+=	${PYPKGPREFIX}-requests>=2.5.0:../../devel/py-requests
DEPENDS+=	${PYPKGPREFIX}-setuptools-[0-9]*:../../devel/py-setuptools
DEPENDS+=	${PYPKGPREFIX}-snowballstemmer>=1.1:../../textproc/py-snowballstemmer
DEPENDS+=	${PYPKGPREFIX}-sphinxcontrib-applehelp-[0-9]*:../../textproc/py-sphinxcontrib-applehelp
DEPENDS+=	${PYPKGPREFIX}-sphinxcontrib-devhelp-[0-9]*:../../textproc/py-sphinxcontrib-devhelp
DEPENDS+=	${PYPKGPREFIX}-sphinxcontrib-jsmath-[0-9]*:../../textproc/py-sphinxcontrib-jsmath
DEPENDS+=	${PYPKGPREFIX}-sphinxcontrib-htmlhelp-[0-9]*:../../textproc/py-sphinxcontrib-htmlhelp
DEPENDS+=	${PYPKGPREFIX}-sphinxcontrib-serializinghtml-[0-9]*:../../textproc/py-sphinxcontrib-serializinghtml
DEPENDS+=	${PYPKGPREFIX}-sphinxcontrib-qthelp-[0-9]*:../../textproc/py-sphinxcontrib-qthelp
DEPENDS+=	${PYPKGPREFIX}-six>=1.5:../../lang/py-six

TEST_DEPENDS+=	${PYPKGPREFIX}-html5lib-[0-9]*:../../textproc/py-html5lib
TEST_DEPENDS+=	${PYPKGPREFIX}-test-[0-9]*:../../devel/py-test
TEST_DEPENDS+=	${PYPKGPREFIX}-test-cov-[0-9]*:../../devel/py-test-cov

USE_LANGUAGES=		# none
USE_TOOLS+=		makeinfo

PYTHON_VERSIONS_INCOMPATIBLE=	27

do-test:
	cd ${WRKSRC} && pytest-${PYVERSSUFFIX} tests

post-install:
	cd ${DESTDIR}${PREFIX}/bin && \
	${MV} sphinx-apidoc sphinx-apidoc-${PYVERSSUFFIX} && \
	${MV} sphinx-autogen sphinx-autogen-${PYVERSSUFFIX} && \
	${MV} sphinx-build sphinx-build-${PYVERSSUFFIX} && \
	${MV} sphinx-quickstart sphinx-quickstart-${PYVERSSUFFIX} || ${TRUE}

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
