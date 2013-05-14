# 
#  fontconfig/conf.d/Makefile.am
# 
#  Copyright © 2005 Keith Packard
# 
#  Permission to use, copy, modify, distribute, and sell this software and its
#  documentation for any purpose is hereby granted without fee, provided that
#  the above copyright notice appear in all copies and that both that
#  copyright notice and this permission notice appear in supporting
#  documentation, and that the name of the author(s) not be used in
#  advertising or publicity pertaining to distribution of the software without
#  specific, written prior permission.  The authors make no
#  representations about the suitability of this software for any purpose.  It
#  is provided "as is" without express or implied warranty.
# 
#  THE AUTHOR(S) DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE,
#  INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS, IN NO
#  EVENT SHALL THE AUTHOR(S) BE LIABLE FOR ANY SPECIAL, INDIRECT OR
#  CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE,
#  DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
#  TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR
#  PERFORMANCE OF THIS SOFTWARE.

DOC_FILES= \
	README

CONF_LINKS = \
	10-base-rendering.conf		\
	15-tt-monospace-fonts.conf		\
	20-fix-cantarell.conf		\
	21-non-tt-rendering.conf		\
	21-tt-rendering.conf		\
	30-non-tt-fonts.conf		\
	30-tt-fonts.conf		\
	35-droid-sans-group.conf		\
	35-droid-serif-group.conf		\
	37-repl-global.conf		\
	38-repl-tt-traced-bitmap.conf		\
	39-repl-corrective.conf		\
	40-nonlatin.conf		\
	45-latin.conf		\
	49-sansserif.conf		\
	50-user.conf		\
	51-local.conf		\
	60-latin.conf		\
	65-non-latin.conf		\
	66-override.conf		\
	67-aliases-wine.conf		\
	70-no-bitmaps.conf		\
	72-embedded-bitmaps.conf		\
	73-ttf-as-bitmap.conf		\
	74-force-autohint.conf		\
	75-qt-subpixel-positioning.conf		\
	76-forced-synthetic.conf		\
	80-selective-rendering.conf		\
	81-final-rendering.conf		\
	82-final-lang-spec.conf		\
	90-no-synthetic.conf		\
	95-reject.conf

EXTRA_DIST = $(templateinf_DATA) $(DOC_FILES)

configdir=$(CONFIGDIR)
config_DATA = $(DOC_FILES)

templateinfdir = $(TEMPLATEINFDIR)
templateinf_DATA =				\
	10-base-rendering.conf		\
	15-tt-monospace-fonts.conf		\
	20-fix-cantarell.conf		\
	21-non-tt-rendering.conf		\
	21-tt-rendering.conf		\
	30-non-tt-fonts.conf		\
	30-tt-fonts.conf		\
	32-tt-traced-bitmap-rendering.conf		\
	35-droid-sans-group.conf		\
	35-droid-serif-group.conf		\
	37-repl-global.conf		\
	38-repl-tt-traced-bitmap.conf		\
	39-repl-corrective.conf		\
	40-nonlatin.conf		\
	45-latin.conf		\
	49-sansserif.conf		\
	50-user.conf		\
	51-local.conf		\
	60-latin.conf		\
	65-non-latin.conf		\
	66-override.conf		\
	67-aliases-wine.conf		\
	70-no-bitmaps.conf		\
	70-yes-bitmaps.conf		\
	71-postscript.conf		\
	72-embedded-bitmaps.conf		\
	73-ttf-as-bitmap.conf		\
	74-force-autohint.conf		\
	75-qt-subpixel-positioning.conf		\
	76-forced-synthetic.conf		\
	80-selective-rendering.conf		\
	81-final-rendering.conf		\
	82-final-lang-spec.conf		\
	90-no-synthetic.conf		\
	95-reject.conf

install-data-hook:
	mkdir -p $(DESTDIR)$(configdir)
	@(echo cd $(DESTDIR)$(configdir);			\
	  cd $(DESTDIR)$(configdir);				\
	  for i in $(CONF_LINKS); do				\
	    echo $(RM) $$i";" ln -s $(templateinfdir)/$$i .;	\
	    $(RM) $$i;						\
	    ln -s $(templateinfdir)/$$i .;				\
	  done)
uninstall-local:
	@(echo cd $(DESTDIR)$(configdir);			\
	  cd $(DESTDIR)$(configdir);				\
	  for i in $(CONF_LINKS); do				\
	    echo $(RM) $$i;					\
	    $(RM) $$i;						\
	  done)

-include $(top_srcdir)/git.mk
