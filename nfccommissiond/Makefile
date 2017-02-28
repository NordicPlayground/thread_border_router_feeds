include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/uclibc++.mk

PKG_NAME:=nfccommissiond
PKG_VERSION:=0.1.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/NordicSemiconductor/thread_border_router_nfc_daemon.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=40df3000522b93c5127d8f1bed0d076777b7fa62
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.bz2
CMAKE_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/nfccommissiond
	SECTION:=utils
	CATEGORY:=Utilities
	TITLE:=Thread nfc commissioning daemon
	DEPENDS:=+libc +libpthread +librt
endef

define Package/nfccommissiond/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/daemon/nfccommissiond $(1)/usr/bin/
endef

$(eval $(call BuildPackage,nfccommissiond))
