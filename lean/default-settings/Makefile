#
# Copyright (C) 2021 Lean <coolsnowwolf@gmail.com>
#
# Copyright (C) 2021 ImmortalWrt
# <https://immortalwrt.org>
#
# This is free software, licensed under the GNU General Public License v3.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=default-settings
PKG_VERSION:=2.0
PKG_RELEASE:=$(COMMITCOUNT)

PKG_LICENSE:=GPL-3.0

include $(INCLUDE_DIR)/package.mk

define Package/default-settings-chn
  $(Package/default-settings)
  TITLE+= (Optimize for CHN users)
endef

define Build/Compile
endef

define Package/default-settings-chn/install
	$(INSTALL_DIR) $(1)/etc/uci-defaults
	$(INSTALL_BIN) ./files/99-default-settings-chinese $(1)/etc/uci-defaults/

endef

$(eval $(call BuildPackage,default-settings-chn))
