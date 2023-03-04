include $(TOPDIR)/rules.mk

PKG_NAME:=nfqws
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://github.com/bol-van/zapret.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=dcd3cc968c3454453870dce6459ce9668df745b8
MAKE_PATH:=nfq

include $(INCLUDE_DIR)/package.mk

define Package/nfqws
	SECTION:=net
	CATEGORY:=Network
	TITLE:=nfqws
	SUBMENU:=Zapret
 	DEPENDS:=+libnetfilter-queue +libcap +zlib
endef

define Build/Prepare
	$(Build/Prepare/Default)
	rm $(PKG_BUILD_DIR)/$(MAKE_PATH)/nfqws
endef

define Package/nfqws/install
	$(INSTALL_DIR) $(1)/opt/zapret/nfq
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/$(MAKE_PATH)/nfqws $(1)/opt/zapret/nfq
endef

$(eval $(call BuildPackage,nfqws))
