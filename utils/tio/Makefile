#
# Copyright (C) 2017-2018 Daniel Engberg <daniel.engberg.lists@pyret.net>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=tio
PKG_VERSION:=1.31
PKG_RELEASE:=1
PKG_MAINTAINER:=
PKG_LICENSE:=GPL-2.0+
PKG_LICENSE_FILES:=COPYING

PKG_SOURCE_URL:=https://github.com/$(PKG_NAME)/$(PKG_NAME)/releases/download/v$(PKG_VERSION)/
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.xz
PKG_HASH:=4e72825914dac77c4587c0772accbd7a1292d5c5895bd49ad1477707b3203e42

PKG_FIXUP:=autoreconf

include $(INCLUDE_DIR)/package.mk

define Package/tio
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A simple TTY terminal I/O application
  URL:=https://tio.github.io/
  SUBMENU:=Terminal
endef

define Package/tio/description
  A small and simple TTY terminal I/O application
endef

define Package/tio/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/tio $(1)/usr/sbin/
endef

$(eval $(call BuildPackage,tio))
