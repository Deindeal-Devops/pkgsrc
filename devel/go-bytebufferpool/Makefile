# $NetBSD: Makefile,v 1.3 2020/01/10 13:32:26 bsiegert Exp $

GITHUB_TAG=	v${PKGVERSION_NOREV}
DISTNAME=	go-bytebufferpool-1.0.0
PKGREVISION=	2
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_GITHUB:=valyala/}
GITHUB_PROJECT=	bytebufferpool

MAINTAINER=	ng0@NetBSD.org
HOMEPAGE=	https://github.com/valyala/bytebufferpool/
COMMENT=	Implementation of a pool of byte buffers with anti-memory-waste protection for Go
LICENSE=	mit

GO_SRCPATH=	github.com/valyala/bytebufferpool
GO_DIST_BASE=	bytebufferpool-${PKGVERSION_NOREV}

.include "../../lang/go/go-package.mk"
.include "../../mk/bsd.pkg.mk"
