# $NetBSD: Makefile,v 1.32 2019/12/11 10:28:58 adam Exp $

DISTNAME=	icalendar-4.0.4
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	time python
MASTER_SITES=	${MASTER_SITE_PYPI:=i/icalendar/}

MAINTAINER=	mj@turner.org.za
HOMEPAGE=	https://github.com/collective/icalendar
COMMENT=	Python parser/generator for iCalendar files, as per RFC2445
LICENSE=	2-clause-bsd

DEPENDS+=	${PYPKGPREFIX}-dateutil-[0-9]*:../../time/py-dateutil
DEPENDS+=	${PYPKGPREFIX}-pytz-[0-9]*:../../time/py-pytz

USE_LANGUAGES=	# none

post-install:
	cd ${DESTDIR}${PREFIX}/bin && \
	${MV} icalendar icalendar-${PYVERSSUFFIX} || ${TRUE}

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
