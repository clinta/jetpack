# Created by: Maciej Pasternacki <maciej@3ofcoins.net>
# $FreeBSD$

PORTNAME=	jetpack
PORTVERSION=	0.0.1.20160416
CATEGORIES=	sysutils

MAINTAINER=	maciej@3ofcoins.net
COMMENT=	App Container runtime

LICENSE=	BSD3CLAUSE

BUILD_DEPENDS=	go>=1.6:lang/go

USE_GITHUB=	yes
GH_ACCOUNT=	3ofcoins
GH_TAGNAME=	b8b413e

USERS=		_jetpack
GROUPS=	_jetpack
USE_RC_SUBR=	jetpack_mds

UID_FILES+=	${MASTERDIR}/UIDs
GID_FILES+=	${MASTERDIR}/GIDs

MAKE_ARGS=	prefix=${LOCALBASE}
USES=		compiler

.include <bsd.port.pre.mk>

# golang assumes that if clang is in use, it is called "clang" and not "cc". If
# it's called "cc", go fails.
.if ${COMPILER_TYPE} == clang
CC=	clang
.endif

.include <bsd.port.post.mk>
