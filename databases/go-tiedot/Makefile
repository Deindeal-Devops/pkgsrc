# $NetBSD: Makefile,v 1.3 2020/01/10 13:32:15 bsiegert Exp $

GITHUB_PROJECT=	tiedot
GITHUB_TAG=	${PKGVERSION_NOREV}
DISTNAME=	3.4
PKGNAME=	go-${GITHUB_PROJECT}-${DISTNAME}
PKGREVISION=	2
CATEGORIES=	databases
MASTER_SITES=	${MASTER_SITE_GITHUB:=HouzuoGuo/}
DIST_SUBDIR=	${GITHUB_PROJECT}

MAINTAINER=	ng0@NetBSD.org
HOMEPAGE=	https://github.com/HouzuoGuo/tiedot/
COMMENT=	NoSQL database in Go
LICENSE=	2-clause-bsd

GO_SRCPATH=	github.com/HouzuoGuo/tiedot
GO_DIST_BASE=	tiedot-${PKGVERSION_NOREV}

.include "../../devel/go-jwt-go/buildlink3.mk"
.include "../../lang/go/go-package.mk"
.include "../../mk/bsd.pkg.mk"
