# $Id$
#
# Copyright 2005 Sun Microsystems, Inc.  All rights reserved.
# 
# Permission to use, copy, modify, distribute, and sell this software and its
# documentation for any purpose is hereby granted without fee, provided that
# the above copyright notice appear in all copies and that both that
# copyright notice and this permission notice appear in supporting
# documentation.
# 
# The above copyright notice and this permission notice shall be included
# in all copies or substantial portions of the Software.
# 
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
# OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
# MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
# IN NO EVENT SHALL THE OPEN GROUP BE LIABLE FOR ANY CLAIM, DAMAGES OR
# OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
# ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
# OTHER DEALINGS IN THE SOFTWARE.
# 
# Except as contained in this notice, the name of the copyright holders shall
# not be used in advertising or otherwise to promote the sale, use or
# other dealings in this Software without prior written authorization
# from the copyright holders.
# 

libmandir = $(mandir)/man$(LIB_MAN_SUFFIX)

libman_SOURCES = \
	libXp.3					\
	XpCancelDoc.3				\
	XpCancelJob.3				\
	XpCancelPage.3				\
	XpCreateContext.3			\
	XpDestroyContext.3			\
	XpEndDoc.3				\
	XpEndJob.3				\
	XpEndPage.3				\
	XpFreePrinterList.3			\
	XpGetAttributes.3			\
	XpGetContext.3				\
	XpGetDocumentData.3			\
	XpGetImageResolution.3			\
	XpGetLocaleHinter.3			\
	XpGetOneAttribute.3			\
	XpGetPageDimensions.3			\
	XpGetPdmStartParams.3			\
	XpGetPrinterList.3			\
	XpGetScreenOfContext.3			\
	XpInputSelected.3			\
	XpPutDocumentData.3			\
	XpQueryExtension.3			\
	XpQueryScreens.3			\
	XpQueryVersion.3			\
	XpRehashPrinterList.3			\
	XpSelectInput.3				\
	XpSetAttributes.3			\
	XpSetContext.3				\
	XpSetImageResolution.3			\
	XpSetLocaleHinter.3			\
	XpStartDoc.3				\
	XpStartJob.3				\
	XpStartPage.3


EXTRA_DIST = $(libman_SOURCES)

CLEANFILES = $(libman_DATA)

libman_DATA = $(libman_SOURCES:man=$(LIB_MAN_SUFFIX))

SED = sed

# Strings to replace in man pages
XORGRELSTRING = @PACKAGE_STRING@
  XORGMANNAME = X Version 11

MAN_SUBSTS = -e 's/__xorgversion__/"$(XORGRELSTRING)" "$(XORGMANNAME)"/'

SUFFIXES = .$(LIB_MAN_SUFFIX) .man

.man.$(LIB_MAN_SUFFIX):
	sed $(MAN_SUBSTS) < $< > $@

