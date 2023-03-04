include $(TOPDIR)/rules.mk

PKG_NAME:=tpws
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://github.com/bol-van/zapret.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=dcd3cc968c3454453870dce6459ce9668df745b8
MAKE_PATH:=tpws

include $(INCLUDE_DIR)/package.mk

define Package/tpws
	SECTION:=net
	CATEGORY:=Network
	TITLE:=tpws
	SUBMENU:=Zapret
 	DEPENDS:=+zlib +libcap
endef

define Build/Prepare
	$(Build/Prepare/Default)
	rm $(PKG_BUILD_DIR)/$(MAKE_PATH)/tpws
endef

define Package/tpws/install
	$(INSTALL_DIR) $(1)/opt/zapret/tpws
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/$(MAKE_PATH)/tpws $(1)/opt/zapret/tpws
endef

$(eval $(call BuildPackage,tpws))
