# $NetBSD: Makefile,v 1.12 2020/01/10 13:32:27 bsiegert Exp $

DISTNAME=	mapstructure-bep-0.0.20180511
PKGNAME=	go-${DISTNAME}
PKGREVISION=	11
MASTER_SITES=	${MASTER_SITE_GITHUB:=bep/}
CATEGORIES=	devel
GITHUB_TAG=	bb74f1db0675b241733089d5a1faa5dd8b0ef57b
GITHUB_PROJECT=	${PKGBASE:S/^go-//:S/-bep//}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/bep/mapstructure
COMMENT=	Library for decoding generic map values into native structures
LICENSE=	mit

GO_DIST_BASE=	${GITHUB_PROJECT}-${GITHUB_TAG}
GO_SRCPATH=	github.com/bep/mapstructure

.include "../../lang/go/go-package.mk"
.include "../../mk/bsd.pkg.mk"
