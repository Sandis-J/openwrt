include $(TOPDIR)/rules.mk
 
PKG_NAME:=sdb
PKG_RELEASE:=1
 
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git@github.com:Sandis-J/student-db.git
PKG_SOURCE_DATE:=2025-01-13
PKG_SOURCE_VERSION:=efe2c69
PKG_MIRROR_HASH:=skip

PKG_MAINTAINER:=Sandis Jurciks <sandis.jurciks@gmail.com>
 
include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=RTU
	CATEGORY:=RTU
	DEPENDS:=+libc
	TITLE:=Student database read/write app
endef

define Package/$(PKG_NAME)/description
CLI application which allows to enter student
data and read that afterwise.
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/student_db $(1)/usr/bin/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
