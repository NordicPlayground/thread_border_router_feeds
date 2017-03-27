include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/uclibc++.mk


PKG_NAME:=nfccommissiond
PKG_VERSION:=0.1.0
PKG_RELEASE:=1
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk

define Package/nfccommissiond
	SECTION:=utils
	CATEGORY:=Utilities
	TITLE:=Thread nfc commissioning daemon
	DEPENDS:=+libc +libpthread +librt
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) ./bin/* $(PKG_BUILD_DIR)/
endef

define Build/Configure

endef

define Build/Compile

endef

define Package/nfccommissiond/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/nfccommissiond $(1)/usr/bin/
endef

$(eval $(call BuildPackage,nfccommissiond))
