#	$OpenBSD: Makefile,v 1.68 2012/01/16 08:42:38 schwarze Exp $

.include <bsd.own.mk>

CFLAGS+=-DVERSION=\"1.12.0\"
CFLAGS+=-W -Wall -Wstrict-prototypes

.if ${COMPILER_VERSION:L} == "gcc3" || ${COMPILER_VERSION:L} == "gcc4" 
CFLAGS+=-Wno-unused-parameter
.endif

LDADD= -ldb

SRCS=	roff.c tbl.c tbl_opts.c tbl_layout.c tbl_data.c eqn.c mandoc.c read.c
SRCS+=	mdoc_macro.c mdoc.c mdoc_hash.c \
	mdoc_argv.c mdoc_validate.c lib.c att.c \
	arch.c vol.c msec.c st.c
SRCS+=	man_macro.c man.c man_hash.c man_validate.c
SRCS+=	main.c mdoc_term.c chars.c term.c tree.c man_term.c eqn_term.c
SRCS+=	mdoc_man.c
SRCS+=	html.c mdoc_html.c man_html.c out.c eqn_html.c
SRCS+=	term_ps.c term_ascii.c tbl_term.c tbl_html.c
SRCS+=	manpath.c mandocdb.c apropos_db.c apropos.c

PROG=	mandoc

MAN=	mandoc.1

.include <bsd.prog.mk>
