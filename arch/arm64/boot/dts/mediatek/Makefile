# SPDX-License-Identifier: GPL-2.0
dtb-$(CONFIG_ARCH_MEDIATEK) += auto2712p1v1-ivi-boot.dtb
dtb-$(CONFIG_ARCH_MEDIATEK) += auto2712p1v1-ivi-nand-boot.dtb

ifeq ($(strip $(CONFIG_BUILD_ARM64_DTB_OVERLAY_IMAGE)), y)
dtb-y += $(addsuffix .dtbo, $(notdir $(subst $\",,$(CONFIG_BUILD_ARM64_DTB_OVERLAY_IMAGE_NAMES))))
endif

always          := $(dtb-y) $(dtbo-y)
subdir-y        := $(dts-dirs)
clean-files     := *.dtb *.dtbo
