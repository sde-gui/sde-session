SUBDIRS = man po

bin_SCRIPTS = startsde lxde-logout openbox-sde

# Currently these paths are hardcoded.
xsessiondir=$(xsesspath)
xsession_DATA = LXDE.desktop

defaultsdir=$(sysconfdir)/xdg/lxsession/LXDE
defaults_DATA = autostart desktop.conf

desktopdir=$(datadir)/applications
desktop_in_files = lxde-logout.desktop.in lxde-screenlock.desktop.in
desktop_DATA = $(desktop_in_files:.desktop.in=.desktop)
@INTLTOOL_DESKTOP_RULE@

wallpapersdir=$(datadir)/lxde/wallpapers
wallpapers_DATA= \
	wallpapers/LICENSE.txt \
	wallpapers/ken-cheung-lYMqE22gpXc-unsplash.jpg \
	wallpapers/lloyd-blunk-mH9Mz6piRoc-unsplash.jpg \
	wallpapers/philip-kl6zd_FJtUo-unsplash.jpg

imagesdir=$(datadir)/lxde/images
images_DATA= \
	images/logout-banner.png \
	images/lxde-icon.png

lxpaneldir=$(sysconfdir)/xdg/lxpanel/LXDE
lxpanel_DATA=lxpanel/config

lxpanel_paneldir=$(sysconfdir)/xdg/lxpanel/LXDE/panels
lxpanel_panel_DATA=lxpanel/panel

openboxdir=$(sysconfdir)/xdg/openbox/LXDE
openbox_DATA= \
	openbox/rc.xml \
	openbox/menu.xml

pcmanfmdir=$(sysconfdir)/xdg/pcmanfm/LXDE
pcmanfm_DATA= \
	pcmanfm/pcmanfm.conf

EXTRA_DIST = \
	autostart \
	desktop.conf \
	LXDE.desktop.in.in \
	$(desktop_in_files) \
	startsde.in \
	$(wallpapers_DATA) \
	$(images_DATA) \
	openbox/rc.xml.in \
	openbox/menu.xml \
	openbox-sde.in \
	pcmanfm/pcmanfm.conf.in \
	$(lxpanel_DATA) \
	lxpanel/panel.in

CLEANFILES = $(bin_SCRIPTS) LXDE.desktop $(desktop_DATA)

