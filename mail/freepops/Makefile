# $NetBSD: Makefile,v 1.44 2020/01/12 20:20:30 ryoon Exp $
#

DISTNAME=	freepops-0.2.9
PKGREVISION=	18
CATEGORIES=	mail
MASTER_SITES=	${MASTER_SITE_SOURCEFORGE:=freepops/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.freepops.org/
COMMENT=	POP3 gateway to AOL, Gmail, Hotmail, Juno, Yahoo, etc
LICENSE=	gnu-gpl-v2

MAKE_JOBS_SAFE=		no
LUA_VERSIONS_ACCEPTED=	51

.include "../../mk/bsd.prefs.mk"

USE_LANGUAGES=		c c++
USE_TOOLS+=		bash:run bison gmake patch pkg-config tar
.if ${OPSYS} != "NetBSD"
USE_TOOLS+=		gsed
.endif
USE_LIBTOOL=		yes
REPLACE_BASH=		configure.sh
HAS_CONFIGURE=		yes
CONFIGURE_SCRIPT=	configure.sh
CONFIGURE_ARGS=		pkgsrc
LDFLAGS+=		-lintl		# directly link, req. by ld 2.22
LDFLAGS.SunOS+=		-lsocket -lnsl -lresolv

PKG_SYSCONFSUBDIR=	freepops
EGDIR=			${PREFIX}/share/examples/${PKGBASE}
CONF_FILES=		${EGDIR}/config.lua ${PKG_SYSCONFDIR}/config.lua
OWN_DIRS+=		${VARBASE}/lib/${PKGBASE}/lua_unofficial
OWN_DIRS+=		${VARBASE}/lib/${PKGBASE}/lua_updates
OWN_DIRS+=		${VARBASE}/lib/${PKGBASE}/lua_updates/lxp
OWN_DIRS+=		${VARBASE}/lib/${PKGBASE}/lua_updates/browser
OWN_DIRS+=		${VARBASE}/lib/${PKGBASE}/lua_updates/soap

SUBST_CLASSES+=		paths
SUBST_STAGE.paths=	do-configure
SUBST_FILES.paths=	config.h doc/freepopsd.1 src/freepops.h
SUBST_FILES.paths+=	src/lua/freepops.lua
SUBST_VARS.paths=	PREFIX
SUBST_VARS.paths+=	PKG_SYSCONFDIR
SUBST_VARS.paths+=	VARBASE
SUBST_MESSAGE.paths=	Adjusting paths.

BUILD_DEFS+=		VARBASE

RCD_SCRIPTS=			freepopsd
FREEPOPSD_USER?=		freepops
FREEPOPSD_GROUP?=		freepops
PKG_GROUPS=			${FREEPOPSD_GROUP}
PKG_USERS=			${FREEPOPSD_USER}:${FREEPOPSD_GROUP}
PKG_GECOS.${FREEPOPSD_USER}=	freepopsd POP3 user
FILES_SUBST+=			FREEPOPSD_USER=${FREEPOPSD_USER:Q}
FILES_SUBST+=			FREEPOPSD_GROUP=${FREEPOPSD_GROUP:Q}
PKG_GROUPS_VARS+=		FREEPOPSD_GROUP
PKG_USERS_VARS+=		FREEPOPSD_USER

.include "../../devel/gettext-lib/buildlink3.mk"
.include "../../lang/lua/buildlink3.mk"
.include "../../security/openssl/buildlink3.mk"
.include "../../textproc/expat/buildlink3.mk"
.include "../../www/curl/buildlink3.mk"
.include "../../mk/pthread.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
