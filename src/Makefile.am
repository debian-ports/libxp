lib_LTLIBRARIES = libXp.la

libXp_la_SOURCES =			\
	XpAttr.c			\
	XpContext.c			\
	XpDoc.c				\
	XpExtUtil.c			\
	XpExtVer.c			\
	XpGetData.c			\
	XpImageRes.c			\
	XpInput.c			\
	XpJob.c				\
	XpLocale.c			\
	XpNotifyPdm.c			\
	XpPage.c			\
	XpPageDim.c			\
	XpPrinter.c			\
	XpPutData.c			\
	XpScreens.c			\
					\
	XpExtUtil.h

libXp_la_LIBADD = @X_LIBS@

INCLUDES = -I$(top_srcdir)/include/X11/extensions

#
# Library version info.  Check the libtool docs for
# instructions on when and how to change this value
#
# bump when the ABI changes
XP_CURRENT=2
# bump for non-ABI changes, reset to zero when CURRENT changes
XP_REVISION=0
# bump when the ABI changes in backward-compatible fashion
XF_AGE=2
libXp_la_LDFLAGS = -version-info ${XP_CURRENT}:${XP_REVISION}:${XP_AGE} -no-undefined
