# $NetBSD: Makefile,v 1.2 2020/01/12 20:19:57 ryoon Exp $

DISTNAME=	wandio-4.2.2
PKGREVISION=	1
CATEGORIES=	misc
MASTER_SITES=	https://research.wand.net.nz/software/wandio/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://research.wand.net.nz/software/libwandio.php
COMMENT=	Library for reading from and writing to files
LICENSE=	gnu-lgpl-v3

CONFLICTS=	libtrace<4.0.0

USE_LANGUAGES=	c c++
USE_LIBTOOL=	yes
GNU_CONFIGURE=	yes

.include "../../archivers/bzip2/buildlink3.mk"
.include "../../archivers/lz4/buildlink3.mk"
.include "../../archivers/lzo/buildlink3.mk"
.include "../../archivers/xz/buildlink3.mk"
.include "../../archivers/zstd/buildlink3.mk"
.include "../../devel/zlib/buildlink3.mk"
.include "../../www/curl/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
