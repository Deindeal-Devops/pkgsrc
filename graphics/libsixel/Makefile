# $NetBSD: Makefile,v 1.47 2020/01/15 15:01:23 tsutsui Exp $

DISTNAME=		libsixel-1.8.6
CATEGORIES=		graphics
MASTER_SITES=		${MASTER_SITE_GITHUB:=saitoha/}
GITHUB_PROJECT=		libsixel
GITHUB_TAG=		v${PKGVERSION_NOREV}

MAINTAINER=		tsutsui@NetBSD.org
HOMEPAGE=		http://saitoha.github.io/libsixel/
COMMENT=		DEC SIXEL graphics codec encoder/decoder and converter
LICENSE=		mit AND public-domain

GNU_CONFIGURE=		yes
USE_LIBTOOL=		yes
USE_TOOLS+=		pkg-config

CONFIGURE_ARGS+=	--disable-python

PKGCONFIG_OVERRIDE+=	libsixel.pc.in

.include "options.mk"

.include "../../mk/bsd.pkg.mk"
