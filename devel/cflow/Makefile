# $NetBSD: Makefile,v 1.13 2019/11/23 06:28:14 mef Exp $

DISTNAME=	cflow-1.6
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_GNU:=cflow/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.gnu.org/software/cflow/
COMMENT=	Code-path flow analyzer for C
LICENSE=	gnu-gpl-v3

GNU_CONFIGURE=		yes
USE_TOOLS+=		yacc lex msgfmt
INFO_FILES=		yes

SUBST_CLASSES+=		emacs
SUBST_MESSAGE.emacs=	Removing cflow Emacs mode
SUBST_STAGE.emacs=	pre-configure
SUBST_FILES.emacs=	Makefile.in
SUBST_SED.emacs=	-e 's| elisp||g'

TEST_TARGET=	check

.include "../../devel/gettext-lib/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
