# $NetBSD: Makefile,v 1.3 2019/11/04 21:43:48 rillig Exp $
#

DISTNAME=	sgrep-1.94a
CATEGORIES=	textproc
MASTER_SITES=	ftp://ftp.cs.helsinki.fi/pub/Software/Local/Sgrep/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.cs.helsinki.fi/u/jjaakkol/sgrep.html
COMMENT=	Tool for searching and indexing text, SGML,XML and HTML files
LICENSE=	gnu-gpl-v2

GNU_CONFIGURE=		yes
# only used for example files
CONFIGURE_ARGS+=	--datadir=${PREFIX}/share/examples/sgrep

INSTALLATION_DIRS+=	share/doc/sgrep

post-install:
	${INSTALL_DATA} ${WRKSRC}/README ${DESTDIR}${PREFIX}/share/doc/sgrep

.include "../../mk/bsd.pkg.mk"
