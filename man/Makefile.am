# FIXME: sde-logout.1 should be placed in sde-session-manager
dist_man_MANS = sde-logout.1 startsde.1 openbox-sde.1

EXTRA_DIST = openbox-sde.xml

if ENABLE_REGENERATE_MAN

openbox-sde.1: openbox-sde.xml
	$(XSLTPROC) -nonet http://docbook.sourceforge.net/release/xsl/current/manpages/docbook.xsl $<        

CLEANFILES = openbox-sde.1
else

$(man_MANS):
	@echo ""
	@echo "Error: you need to run configure with '--enable-man'"
	@echo "       in order to regenerate man pages."
	@echo ""
	@false
endif
