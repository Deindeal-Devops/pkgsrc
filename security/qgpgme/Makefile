# $NetBSD: Makefile,v 1.7 2019/04/03 00:33:05 ryoon Exp $

DISTNAME=	gpgme-1.10.0
PKGNAME=	qgpgme-1.10.0
PKGREVISION=	6
CATEGORIES=	security
MASTER_SITES=	ftp://ftp.gnupg.org/gcrypt/gpgme/
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.gnupg.org/related_software/gpgme/
COMMENT=	Qt bindings for GPGme
LICENSE=	gnu-lgpl-v2.1

USE_TOOLS+=	pkg-config gmake
GNU_CONFIGURE=	yes
USE_LANGUAGES=	c c++

BUILD_DIRS=	lang/qt/src

CONFIGURE_ENV+=	MOC=${QTDIR}/bin/moc

.include "../../security/gpgme/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
