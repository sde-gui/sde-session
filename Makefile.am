SUBDIRS = man po

bin_SCRIPTS = startsde openbox-sde

# Currently these paths are hardcoded.
xsessiondir=$(xsesspath)
xsession_DATA = SDE.desktop

defaultsdir=$(sysconfdir)/xdg/sde-session-manager/SDE
defaults_DATA = autostart desktop.conf

desktopdir=$(datadir)/applications
desktop_in_files = sde-logout.desktop.in sde-lock-screen.desktop.in
desktop_DATA = $(desktop_in_files:.desktop.in=.desktop)
@INTLTOOL_DESKTOP_RULE@

wallpapersdir=$(datadir)/sde/wallpapers
wallpapers_DATA= \
	wallpapers/LICENSE.txt \
	wallpapers/ken-cheung-lYMqE22gpXc-unsplash.jpg \
	wallpapers/lloyd-blunk-mH9Mz6piRoc-unsplash.jpg \
	wallpapers/philip-kl6zd_FJtUo-unsplash.jpg

waterlinedir=$(sysconfdir)/xdg/sde/waterline/SDE
waterline_DATA=waterline/config

waterline_paneldir=$(sysconfdir)/xdg/sde/waterline/SDE/panels
waterline_panel_DATA= \
	waterline/panels/panel1.js \
	waterline/panels/panel2.js

openboxdir=$(sysconfdir)/xdg/openbox/SDE
openbox_DATA= \
	openbox/rc.xml \
	openbox/menu.xml

stuurman_desktopdir=$(sysconfdir)/xdg/stuurman-desktop/SDE
stuurman_desktop_DATA= \
	stuurman-desktop/desktop.conf

EXTRA_DIST = \
	autostart \
	desktop.conf \
	SDE.desktop.in.in \
	$(desktop_in_files) \
	startsde.in \
	$(wallpapers_DATA) \
	$(images_DATA) \
	openbox/rc.xml.in \
	openbox/menu.xml \
	openbox-sde.in \
	stuurman-desktop/desktop.conf.in \
	$(waterline_DATA)

CLEANFILES = $(bin_SCRIPTS) SDE.desktop $(desktop_DATA)

